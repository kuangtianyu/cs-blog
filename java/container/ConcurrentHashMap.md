# ConcurrentHashMap杂谈

## 为什么使用ConcurrentHashMap  

- 在并发编程中使用HashMap可能导致程序死循环，而使用线程安全的HashTable效率又非常低下

### 线程不安全的HashMap

- 在多线程环境下，使用HashMap进行put操作会引起死循环，导致CPU利用率接近100%

- 死循环案例：

  ```java
  final HashMap<String, String> map = new HashMap<String, String>(2);
  Thread t = new Thread(new Runnable() {
      @Override
      public void run() {
          for (int i = 0; i < 10000; i++) {
              new Thread(new Runnable() {
                  @Override
                  public void run() {
                      map.put(UUID.randomUUID().toString(), "");
                  }
              }, "ftf" + i).start();
          }
      }
  }, "ftf");
  t.start();
  t.join();
  ```

  原因：多线程会导致HashMap的Entry链表形成环形数据结构，一旦形成环形数据结构，Entry的next节点永远不为空，就会产生死循环获取Entry

### 效率低下的HashTable

- HashTable容器使用synchronized来保证线程安全，但在激烈的情况下HashTable的效率非常低下，因为当一个线程访问HashTable的同步方法时，其他线程会进入阻塞或轮询状态。所以竞争越激烈效率越低

### ConcurrentHashMap提升并发访问率的方法

- 使用的是锁分段技术
- 访问HashTable的线程都必须竞争同一把锁，加入容器里面有多把锁，每一把锁用于锁容器其中一部分数据，当多线程访问容器里不同数据段的数据时，线程间就不会存在锁竞争，可以有效提高并发访问效率，这就是所分段技术。将数据分成一段一段地存储，然后给每一段数据分配一把锁，当一个线程占用锁访问其中一段数据的时候，其他段的数据也能被其他线程访问

## ConcurrentHashMap的结构

- ConcurrentHashMap是由Segment数组结构和HashEntry数组结构组成。Segment是一种可重入锁（ReentrantLock）；HashEntry则用于存储键值对数据。一个ConcurrentHashMap里包含一个Segment数组。Segment结构是一种数组和链表结构。一个Segment里面包含一个HashEntry数组，每个HashEntry是一个链表结构的元素，每个Segment守护着一个HashEntry数组里面的元素，当对HashEntry数组的数据结构进行修改时，必须首先获得与它对应的Segment锁。如图：

    ![](https://gitee.com/kuangty/blogImage/raw/master/img/currentHashMap.png)

## 定位Segment

- ConcurrentHashMap使用Wang/Jenkins hash的变种算法对元素的hashCode进行一次再散列：

  ```java
  private static int hash(int h) {
      h += (h << 15) ^ 0xffffcd7d;
      h ^= (h >>> 10);
      h += (h << 3);
      h ^= (h >>> 6);
      h += (h << 2) + (h << 14);
      return h ^ (h >>> 16);
  }
  ```

  - 进行再散列的目的是减少散列冲突，是元素能够均匀分布在不同的Segment上，从而提高容器的存取效率

## ConcurrentHashMap的操作

- 三种操作：get操作、put操作和size操作

### get操作

- Segment的get操作实现非常简单高效。先经过一个再散列，然后使用这个散列值通过散列运算定位到Segment，再通过散列算法定位到元素

  ```java
  public V get(Object key) {
      int hash = hash(key.hashCode());
      return segmentFor(hash).get(key, hash);
  }
  ```

- ConcurrentHashMap的get操作相比于HashTable容器的get方法不需要加锁，除非读到的值是空才会加锁重读。它是如何做到的呢? 原因是它的get方法里将要使用的共享变量都定义成volatile类型，如用于统计当前Segement大小的count字段和用于储存值的HashEntry的value。定义成volatile的变量，能够在线程之间保持可见性，保证多个线程读到的是最新的值，但是只能被单线程写（有一种情况可以被多线程写，就是写入的值不依赖与原值）。根据Java内存模型的happen before原则，对volatile字段的写入操作先于读操作，即使两个线程同时修改和获取volatile变量，get操作也能拿到最新的值

  ```java
  transient volatile int count;
  volatile V value;
  ```

### put操作

- 由于put方法里需要对共享变量进行写入操作，所以为了线程安全，在操作共享变量时必须加锁。put方法首先定位到Segment，然后在Segment里面进行插入操作：
  - 第一步：判断是否需要对Segment里的HashEntry数组进行扩容
  - 第二步定位添加元素的位置，然后将其放在HashEntry数组里
- HashEntry数组扩容
  - HashEntry在插入元素前会判断Segment里的HashEntry数组是否超过容量，如果超过容量，再进行扩容。而HashMap是在插入元素之后判断容量是否已经到达阈值，如果到达了阈值就进行扩容，但是很可能扩容之后没有新元素插入，这将会是一次无效的扩容
  - 首先会创建一个容量是原来容量两倍的数组，然后将原数组里的元素进行再散列后插入到新的数组里。为了高效，ConcurrentHashMap不会对整个容器进行扩容，而只是对某个segment进行扩容

### seze操作

- 是不是把所有Segment的count相加就可以得到整个ConcurrentHashMap的大小呢？不是的。理由：虽然在相加时可以获取每个Segment的count的最新值，但是可能累加前使用的count发生了变化，导致统计结果不准确。那么是不是就可以对Segment的put、remove、clean方法加锁就行了呢？其实也不是，这种做法非常低效。于是ConcurrentHashMap采用了下面的做法：ConcurrentHashMap先尝试2次通过不锁住Segment的方式来统计各个Segment大小，如果统计过程中，容器的count发生了变化，则再采用加锁的方式来统计所有Segment的大小
- 如何判断在统计的时候容器是否发生了变化：使用modCount变量，在put、remove和clean方法操作元素前将modCount+1，在统计后比较modCount是否发生变化。发生变化，则可以判断容器发生了变化，反之。



> 参考：《Java并发编程的艺术》