<style>
    h2
    {
      margin-bottom:50px;
      font-size: 1em;
    }
    h2 span
    {
      display:inline-block;
      background: rgb(102, 126, 233);
      color:#ffffff !important;
      padding:  10px  16px;
      border-radius:5px;
      box-shadow: 2px 2px 5px rgb(216, 216, 216);
    }
    .markdown-section
    {
  		padding: 30px 30px 40px 30px !important;
		}
</style>




<br>

<p align="center">
    <img width="320px" src="https://gitee.com/kuangty/blogImage/raw/master/img/wushuaiyu%20.png" >
</p>





</br>
<br>


|          算法          |         操作系统          |        网络&nbsp;        |          数据库          |          Java          |          必备框架          | 微服务                   |          中间件          |         系统设计          | 项目                  |      &nbsp;工具       | 后记                   |
| :--------------------: | :-----------------------: | :----------------------: | :----------------------: | :--------------------: | :------------------------: | ------------------------ | :----------------------: | :-----------------------: | --------------------- | :-------------------: | ---------------------- |
| [🤖 ](README?id=🤖-算法) | [🎮](README?id=🎮-操作系统) | [🎨  ](README?id=🎨-网络 ) | [📑 ](README?id=📑-数据库) | [🍵 ](README?id=🍵-Java) | [🔥 ](README?id=🔥-必备框架) | [🔮 ](README?id=🔮-微服务) | [👷 ](README?id=👷-中间件) | [🦄](README?id=🦄-系统设计) | [🏆](README?id=🏆-项目) | [🔨](README?id=🔨-工具) | [📞 ](README?id=📞-后记) |

</br>

---

💡 **「关于」**

- 🎓 博主渣渣一个，这是博主的学习记录笔记，不得用于商用。
- 🔮  [Github 仓库地址](https://github.com/kuangtianyu/cs-blog)
- 常用学习网站：
  - [Gitee](https://kuangtf.gitee.io/blogs/#/)
  - [CS-Wiki](https://veal98.gitee.io/cs-wiki/#/README)
  - [Java全栈](https://www.pdai.tech/md/outline/x-outline.html#%E5%85%A8%E6%A0%88%E7%9F%A5%E8%AF%86%E4%BD%93%E7%B3%BB%E6%80%BB%E8%A7%88)
  - [CS-Notes](http://www.cyc2018.xyz/#%E7%AE%97%E6%B3%95)
  - [OI-Wiki](https://oi-wiki.org/)
  - [JavaGuide](https://snailclimb.gitee.io/javaguide/#/)
  - [Doocs](https://doocs.gitee.io/advanced-java/#/)

## 🤖 算法

### 数据结构

- [红黑树](https://mp.weixin.qq.com/s/sPIE54UmvNgINZIATQKyew)
- AVL树
- [平衡二叉树](https://zhuanlan.zhihu.com/p/56066942)
- [手撸LRU](http://mp.weixin.qq.com/s?__biz=MzAxODQxMDM0Mw==&mid=2247486428&idx=1&sn=3611a14535669ba3372c73e24121247c&chksm=9bd7f5d4aca07cc28c02c3411d0633fc12c94c2555c08cbfaa2ccd50cc2d25160fb23bccce7f&scene=21#wechat_redirect)
- [手撸LFU](http://mp.weixin.qq.com/s?__biz=MzAxODQxMDM0Mw==&mid=2247486545&idx=1&sn=315ebfafa82c0dd3bcd9197eb270a7b6&chksm=9bd7f259aca07b4f063778509b3803993bc0d6cdaff32c076a102547b0afb82a5eea6119ed1a&scene=21#wechat_redirect)

### 算法

- [排序算法](algorithm/排序算法.md)
- [算法模板](algorithm/算法模板.md)
- [算法题](algorithm/算法题.md)
- [提高课](algorithm/提高课.md)
- [基础课](algorithm/基础课.md)

## 🎮 操作系统

### 操作系统

- 基础
  - 用户态和核心态的区别

- 进程
  - [进程通信的方式](https://mp.weixin.qq.com/s/kxxV_yy5eesHiHHLPO0mWg)
  - [进程同步机制](https://mp.weixin.qq.com/s/vvjhbzsWQNRkU7-b_dURlQ)
  - [进程调度算法](https://mp.weixin.qq.com/s/CEntVZvo_f3VPw5-mjxbqw)
  - 进程、线程的区别
  - 进程的几种状态
  - [用户线程和守护线程](https://www.jianshu.com/p/b51da027bfe1)
  - [孤儿进程和僵尸进程](https://www.cnblogs.com/anker/p/3271773.html)
  - 银行家算法
  - 生产者消费者问题
  - 死锁
- 内存
  - 内存页面置换算法
  - 内存管理，虚拟内存
  - 逻辑地址和物理地址
- 文件
  - [磁盘的寻道算法](https://blog.csdn.net/weixin_46156200/article/details/114084146)
- IO
  - select、poll、epoll的区别
  - NIO - IO多路复用详解
  - Java AIO
  - NIO - 零拷贝
  - 阻塞、非阻塞
  - 同步、异步
  - [Reactor和Proactor](https://mp.weixin.qq.com/s/px6-YnPEUCEqYIp_YHhDzg)

### Linux

- [常用的Linux命令](https://juejin.cn/post/6844903930166509581)
- Linux磁盘管理
- Linux文件与目录管理

## 🎨 网络 

### 计算机网络

- 应用层
  - [HTTP](https://mp.weixin.qq.com/s/98FtlAy0mAtf6tGplQMDqA)
  - [HTTPS](https://mp.weixin.qq.com/s/NTZlUzu4R3xyWB5T6qWo9w)
  - [典型的HTTP攻击手段](https://www.hollischuang.com/archives/2101)
  - HTTP  1.0  1.1  2.1 的区别
  - HTTP常见的状态码
  - [DNS协议详解](https://mp.weixin.qq.com/s/AfVqL7lEsbRE-YLOPZ4gDQ)
  - [DNS协议使用UDP吗](https://mp.weixin.qq.com/s/3QieSeqbuU2fmqYRqj6GaQ)
- 传输层
  - [TCP三次握手和四次挥手](https://mp.weixin.qq.com/s/u56NcMs68sgi6uDpzJ61yw)
  - [TCP保证可靠传输的机制](https://mp.weixin.qq.com/s/AwdxuP5nJSnkyvXRKnqdOg)
  - [TCP和UDP区别](https://juejin.cn/post/6857707137797292046)
- 网络层
  - [IP协议详解](https://mp.weixin.qq.com/s/NO9RDt1A3T1rz-Q4_Y0gPw)
  - [ARP协议详解](https://mp.weixin.qq.com/s/HkcMdiZbfsV52IW7xhfdqg)
  - [ICMP详解](https://mp.weixin.qq.com/s/3SujLofRpxA2RfLljFbW1Q)
  - [粘包和拆包](https://www.cnblogs.com/wade-luffy/p/6165671.html)
  - [ping的原理](https://www.cnblogs.com/xiaolincoding/p/12571184.html)
- 其他
  - [长连接和短连接](https://www.cnblogs.com/0201zcr/p/4694945.html)
  - [get与post请求的区别](https://www.huaweicloud.com/articles/5c532839eeb5e1cd4665f48b0a581eb3.html)
  - [Cookie和session的区别](https://www.cnblogs.com/ityouknow/p/10856177.html)
  - [输入一个URL回车发生了什么](https://mp.weixin.qq.com/s/9vGRSkUNgRQWO6tVmUisOw)
  - URI 和 RUL 的区别
  - 常用的网络攻击技术

### 网络编程

- Socket编程
- netty编程

## 📑 数据库

### MySQL

- 索引
  - [聚簇索引和非聚簇索引的区别](https://www.huaweicloud.com/articles/ce5c6f4d1d60cf7f82f2db6e215555d3.html)
  - [索引在哪种情况下会失效](https://bbs.huaweicloud.com/blogs/244749)
  - [最左原则?联合索引?](https://blog.csdn.net/u013568373/article/details/93891531#:~:text=%E6%9C%80%E5%B7%A6%E5%8C%B9%E9%85%8D%E5%8E%9F%E5%88%99%E7%9A%84%E6%88%90%E5%9B%A0%20MySQL,%E5%BB%BA%E7%AB%8B%E8%81%94%E5%90%88%E7%B4%A2%E5%BC%95%E7%9A%84%E8%A7%84%E5%88%99%E6%98%AF%E8%BF%99%E6%A0%B7%E7%9A%84%EF%BC%8C%E5%AE%83%E4%BC%9A%20%E9%A6%96%E5%85%88%E6%A0%B9%E6%8D%AE%E8%81%94%E5%90%88%E7%B4%A2%E5%BC%95%E4%B8%AD%E6%9C%80%E5%B7%A6%E8%BE%B9%E7%9A%84%E3%80%81%E4%B9%9F%E5%B0%B1%E6%98%AF%E7%AC%AC%E4%B8%80%E4%B8%AA%E5%AD%97%E6%AE%B5%E8%BF%9B%E8%A1%8C%E6%8E%92%E5%BA%8F%EF%BC%8C%E5%9C%A8%E7%AC%AC%E4%B8%80%E4%B8%AA%E5%AD%97%E6%AE%B5%E6%8E%92%E5%BA%8F%E7%9A%84%E5%9F%BA%E7%A1%80%E4%B8%8A%EF%BC%8C%E5%86%8D%E5%AF%B9%E8%81%94%E5%90%88%E7%B4%A2%E5%BC%95%E4%B8%AD%E5%90%8E%E9%9D%A2%E7%9A%84%E7%AC%AC%E4%BA%8C%E4%B8%AA%E5%AD%97%E6%AE%B5%E8%BF%9B%E8%A1%8C%E6%8E%92%E5%BA%8F%EF%BC%8C%E4%BE%9D%E6%AD%A4%E7%B1%BB%E6%8E%A8%20%E3%80%82)
- 事务
  - 事务的ACID特性
  - 事务的隔离级别
  - 分布式事务
  - 事务的两阶段提交
- 锁
  - 数据库锁有哪些？
  - 数据库的乐观锁和悲观锁?
  - [MVVC](https://juejin.cn/post/6871046354018238472)
- 其他
  - redo log、undo log、bin log 
  - [一条SQL语句的执行过程](https://blog.csdn.net/weixin_41385912/article/details/112975752)
  - [分库解决了什么问题?分表解决了什么问题](https://segmentfault.com/a/1190000023914691)
  - [myISAM和innodb的区别](https://www.huaweicloud.com/articles/bb2e4d7dcc7d849df919a88289c9d74c.html)
  - 可以说下数据库范式吗
  - MySQL的缓存
  - sql优化和索引优化
  - [讲讲数据库表怎么设计的](https://blog.csdn.net/kw023781/article/details/103002794)
  - 数据库的主从复制和保证一致性
  - MySQL慢查询
  - 什么是sql注入，如何防止sql注入
  - Select * 的优化

### Reids

- [Redis底层数据结构](https://www.kancloud.cn/kancloud/redisbook/63826)
- [淘汰过期键的策略和内存淘汰机制](https://mp.weixin.qq.com/s/-caMTrOXQu-o0O44e6I9dQ)
- [Redis持久化](https://veal98.gitee.io/cs-wiki/#/%E7%B3%BB%E7%BB%9F%E8%AE%BE%E8%AE%A1/%E9%AB%98%E5%B9%B6%E5%8F%91/%E7%BC%93%E5%AD%98/Redis/8-Redis%E6%8C%81%E4%B9%85%E5%8C%96)
- [缓存穿透 缓存雪崩 如何避免](https://mp.weixin.qq.com/s/knz-j-m8bTg5GnKc7oeZLg) 
- [Redis事务](https://redisbook.readthedocs.io/en/latest/feature/transaction.html)
- [布隆过滤器](https://github.com/AobingJava/JavaFamily/blob/master/docs/redis/%E5%B8%83%E9%9A%86%E8%BF%87%E6%BB%A4%E5%99%A8(BloomFilter).md)
- [redis哨兵](https://www.pdai.tech/md/db/nosql-redis/db-redis-x-sentinel.html)
- [保证数据库和缓存的一致性](https://mp.weixin.qq.com/s/4W7vmICGx6a_WX701zxgPQ)
- [Redis如何实现分布式锁](https://mp.weixin.qq.com/s/RnSokJxYxYDeenOP_JE3fQ)
- [redis事件](https://www.pdai.tech/md/db/nosql-redis/db-redis-x-event.html)
- [Redis发布订阅](https://veal98.gitee.io/cs-wiki/#/%E7%B3%BB%E7%BB%9F%E8%AE%BE%E8%AE%A1/%E9%AB%98%E5%B9%B6%E5%8F%91/%E7%BC%93%E5%AD%98/Redis/9-Redis%E5%8F%91%E5%B8%83%E8%AE%A2%E9%98%85)
- [Redis集群和主从复制](https://mp.weixin.qq.com/s?__biz=MzUxODAzNDg4NQ==&mid=2247495237&idx=1&sn=8302585810958567a57bda3df6c5d036&chksm=f98daaefcefa23f95e9f4ef083bbf6b8ce80794bb00c68d9070f158e6de9a0265ea39b12e560&scene=132#wechat_redirect)
- [一致性哈希](http://walkerdu.com/2020/01/02/consistent_hash/)
- [Redis性能问题](https://mp.weixin.qq.com/s/Qc4t_-_pL4w8VlSoJhRDcg)
- [Redis当做队列](https://mp.weixin.qq.com/s/RthQvzLHZRGNo-z6X_7jQQ)
- [Redis中的一些坑](https://mp.weixin.qq.com/s/CHtZI9k2qQ_YJb5Mwzrukw)
- [Redis常见面试题](https://mp.weixin.qq.com/s/R1TJMo2IbPUUMox9OAAafQ)


## 🍵 Java

### Java 基础

- [解决hash冲突的方法](https://zhuanlan.zhihu.com/p/29520044)
- [反射](https://mp.weixin.qq.com/s/Z4L1y-NbStBDSWYVK28kbA)
- [动态代理](https://mp.weixin.qq.com/s/HI32MA5lsyzgMnqJQi4F6A)
- [String、StringBuilder、StringBuffer区别](https://mp.weixin.qq.com/s/4fXP9ahIPtcsKqlZwdOQJg)
- [Object类中有哪些方法](https://gitee.com/kuangtf/blogImage/raw/master/img/object%E7%B1%BB%E4%B8%AD%E7%9A%84%E6%96%B9%E6%B3%95.jpg)
- [Java泛型详解](https://www.pdai.tech/md/java/basic/java-basic-x-generic.html)
- [Java中的包装类](https://mp.weixin.qq.com/s/qmlNXlPj4gPeVvLOdYLbUA)
- [Comparable和Comparator](https://www.cnblogs.com/skywang12345/p/3324788.html)
- sleep和wait的区别
- 为什么重写equals时要重写hashCode
- Java多态如何实现
- 抽象类和接口的区别

### 集合

- [HashMap底层原理](https://tech.meituan.com/2016/06/24/java-hashmap.html)
- [ConcurrentHash底层原理](https://www.pdai.tech/md/java/thread/java-thread-x-juc-collection-ConcurrentHashMap.html)
- [ConcurrentHash浅谈](java/container/ConcurrentHashMap.md)
- ArrayList 和 LinkedList有什么区别
- vector
- HashTable ， HashSet，TreeSet详解

### 并发

- [Java线程创建的方式](https://veal98.gitee.io/cs-wiki/#/Java/%E5%B9%B6%E5%8F%91/60-%E6%9C%89%E7%82%B9%E6%94%B6%E8%8E%B7-%E4%B8%89%E7%A7%8D%E5%9F%BA%E6%9C%AC%E6%96%B9%E6%B3%95%E5%88%9B%E5%BB%BA%E7%BA%BF%E7%A8%8B)
- [线程的生命周期和状态](https://www.processon.com/diagraming/60fbf1fd1efad46a20a398f7)
- [JMM与原子性、可见性、有序性](https://veal98.gitee.io/cs-wiki/#/Java/%E5%B9%B6%E5%8F%91/40-%E8%B7%AC%E6%AD%A5%E5%8D%83%E9%87%8C-%E8%AF%A6%E8%A7%A3Java%E5%86%85%E5%AD%98%E6%A8%A1%E5%9E%8B%E4%B8%8E%E5%8E%9F%E5%AD%90%E6%80%A7-%E5%8F%AF%E8%A7%81%E6%80%A7-%E6%9C%89%E5%BA%8F%E6%80%A7)
- [Happens-before](https://veal98.gitee.io/cs-wiki/#/Java/%E5%B9%B6%E5%8F%91/50-JMM%E6%9C%80%E6%9C%80%E6%9C%80%E6%A0%B8%E5%BF%83%E7%9A%84%E6%A6%82%E5%BF%B5-Happens-before%E5%8E%9F%E5%88%99)
- [volatile](java/concurrent/volatile.md)
- [synchronized](java/concurrent/synchronized.md)
- [ReentrantLock](https://www.processon.com/view/link/60fbd4800791294ae09f4de1)
- [AQS](https://tech.meituan.com/2019/12/05/aqs-theory-and-apply.html)
- [Unsafe](https://tech.meituan.com/2019/02/14/talk-about-java-magic-class-unsafe.html)
- [ThreadPoolExecutor](https://www.processon.com/view/link/6120e4380791297c64e145ac)
- [ThreadLocal](https://mp.weixin.qq.com/s/LzkZXPtLW2dqPoz3kh3pBQ)
- [CAS](https://blog.csdn.net/ls5718/article/details/52563959) 
- [LockSupport](https://www.pdai.tech/md/java/thread/java-thread-x-lock-LockSupport.html)
- [Semaphore](https://www.pdai.tech/md/java/thread/java-thread-x-juc-tool-semaphore.html)
- [CountDownLatch](https://www.pdai.tech/md/java/thread/java-thread-x-juc-tool-countdownlatch.html)
- [CyclicBarrier](https://www.pdai.tech/md/java/thread/java-thread-x-juc-tool-cyclicbarrier.html)
- [不得不说的Java“锁”事](https://tech.meituan.com/2018/11/15/java-lock.html)

### JVM

- [类加载子系统](https://blog.csdn.net/weixin_46156200/article/details/112572301)
- 双亲委派机制
- Java运行时数据区
- [堆](https://blog.csdn.net/weixin_46156200/article/details/112985882)
- [虚拟机栈](https://blog.csdn.net/weixin_46156200/article/details/112827623)
- 内存泄露和内存溢出
- 强引用、软引用、弱引用、虚引用
- [垃圾收集器](https://blog.csdn.net/weixin_46156200/article/details/113422370)
- CMS和G1的区别
- [常见的垃圾收集算法](https://blog.csdn.net/weixin_46156200/article/details/113178094)
- [哪些对象可以作为GC Roots](https://blog.csdn.net/weixin_38007185/article/details/108093716)
- [CPU100%排查](https://mp.weixin.qq.com/s/roEMz-5tzBZvGxbjq8NhOQ)
- [内存溢出排查](https://mp.weixin.qq.com/s/7XGD-Z3wrThv5HyoK3B8AQ)

## 🔥 必备框架

### Spring

- [Spring 事务传播机制](https://mp.weixin.qq.com/s/IglQITCkmx7Lpz60QOW7HA)
- IOC和AOP原理
- [Spring启动流程](https://mp.weixin.qq.com/s/ut3mRwhfqXNjrBtTmI0oWg)
- Spring bean的生命周期
- Spring 中用到的设计模式
- [spring怎么解决循环依赖](https://mp.weixin.qq.com/s/5mwkgJB7GyLdKDgzijyvXw)
- beanFactory和Factory的区别

### SpringMVC

- SpringMVC的执行流程

### Mybatis

- [mybatis缓存](https://tech.meituan.com/2018/01/19/mybatis-cache.html)
- #{} 和 ${}的区别
- Mybatis如何进行分页的
- Mybatis的动态SQL
- Mybatis半自动和全自动的区别
- mybatis事务

### Spring Boot

- Spring Boot 启动流程
- @SpringBootApplication注解
- 自动装配原理

### Netty

- 从BIO、NIO到Netty

### Dubbo

- 原理

### zookeeper

- [学习笔记](framework/zookeeper/zookeeper.md)

## 🔮 微服务

### SpringCloud

- 服务注册中心：Eureka
- 服务调用：Feign、OpenFeign
- 服务降级：Hystrix
- 服务网关：Zuul、gateway
- 服务配置：Config
- 服务总线：Bus

### SpringCloudAlibaba

- Nacos
- Sentienl
- Ribbon
- Seata

## 👷  中间件

### RabbitMQ

- [RabbitMQ详解](https://blog.csdn.net/weixin_46156200/article/details/113729844)

### Kafka

- 原理

## 🦄 系统设计

### 设计模式

- [创建型模式](https://www.pdai.tech/md/dev-spec/pattern/2_singleton.html)
- [结构型模式](https://www.pdai.tech/md/dev-spec/pattern/8_facade.html)
- [行为型模式](https://www.pdai.tech/md/dev-spec/pattern/15_chain.html)

### 设计原则

- [SOLID原则](https://www.pdai.tech/md/dev-spec/spec/dev-th-solid.html)
- [CAP理论](https://www.pdai.tech/md/dev-spec/spec/dev-th-cap.html)

### 面向对象思想

- 面向对象的三大特征

## 🏆 项目

- 开源考试项目
- RPC项目

## 🔨 工具 

- [Git](https://www.pdai.tech/md/devops/tool/tool-git.html)
- [Docker](https://www.pdai.tech/md/devops/docker/docker-00-overview.html)
- [正则表达式](https://www.pdai.tech/md/develop/regex/dev-regex-all.html)

## 📞 后记

**公众号**

- 文章会第一时间在公众号推送哟

<p align="center">
    <img width="320px" src="https://gitee.com/kuangty/blogImage/raw/master/img/11.jpg" style="zoom:50%;" >
</p>





**联系我**

- 有什么问题也可以添加我的微信，记得备注来意：格式 （学校或公司 - 姓名或昵称 - 来意）

<p align="center">
    <img width="320px" src="https://gitee.com/kuangty/blogImage/raw/master/img/1.png" style="zoom:50%;" >
</p>
