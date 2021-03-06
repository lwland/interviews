### Java多线程

1. 线程池的原理，为什么要创建线程池？
    目的：线程是稀缺资源，线程的创建和销毁需要消耗一定的系统资源，使用线程池可以减少线程的创建和销毁的次数，每个线程可以重复使用。可以通过线程池控制线程的数量，防止线程过多导致服务器崩溃。
    原理：java 线程池
    ````
    public ThreadPoolExecutor(int corePoolSize,//池中核心线程数
       int maximumPoolSize,//池中最大线程数
       long keepAliveTime,
       TimeUnit unit,
       BlockingQueue<Runnable> workQueue,
       RejectedExecutionHandler handler) 
   ````

2. 线程的生命周期，什么时候会出现僵死进程；

什么实现线程安全，如何实现线程安全；

创建线程池有哪几个核心参数？ 如何合理配置线程池的大小？

synchronized、volatile区别、synchronized锁粒度、模拟死锁场景、原子性与可见性；

### JVM相关
JVM内存模型，GC机制和原理；GC分哪两种；什么时候会触发Full GC？

JVM里的有几种classloader，为什么会有多种？

什么是双亲委派机制？介绍一些运作过程，双亲委派模型的好处；(这个我真的不会...)

什么情况下我们需要破坏双亲委派模型；

常见的JVM调优方法有哪些？可以具体到调整哪个参数，调成什么值？

JVM虚拟机内存划分、类加载器、垃圾收集算法、垃圾收集器、class文件结构是如何解析的；

Java扩展
红黑树的实现原理和应用场景；

NIO是什么？适用于何种场景？

Java9比Java8改进了什么；

HashMap内部的数据结构是什么？底层是怎么实现的？

说说反射的用途及实现，反射是不是很慢，我们在项目中是否要避免使用反射；

说说自定义注解的场景及实现；

List和Map区别，Arraylist与LinkedList区别，ArrayList与Vector 区别；

Spring

Spring AOP的实现原理和场景；（应用场景很重要）

Spring bean的作用域和生命周期；

Spring Boot比Spring做了哪些改进？ Spring 5比Spring4做了哪些改进；（惭愧呀，我们还在用Spring4，高版本的没关心过）

Spring IOC是什么？优点是什么？

SpringMVC、动态代理、反射、AOP原理、事务隔离级别；

中间件
Dubbo完整的一次调用链路介绍；

Dubbo支持几种负载均衡策略？

Dubbo Provider服务提供者要控制执行并发请求上限，具体怎么做？

Dubbo启动的时候支持几种配置方式？

了解几种消息中间件产品？各产品的优缺点介绍；

消息中间件如何保证消息的一致性和如何进行消息的重试机制？

Spring Cloud熔断机制介绍；

Spring Cloud对比下Dubbo，什么场景下该使用Spring Cloud？

数据库篇
锁机制介绍：行锁、表锁、排他锁、共享锁；

乐观锁的业务场景及实现方式；

事务介绍，分布式事物的理解，常见的解决方案有哪些，什么事两阶段提交、三阶段提交；

MySQL记录binlog的方式主要包括三种模式？每种模式的优缺点是什么？

MySQL锁，悲观锁、乐观锁、排它锁、共享锁、表级锁、行级锁；

分布式事务的原理2阶段提交，同步\异步\阻塞\非阻塞；

数据库事务隔离级别，MySQL默认的隔离级别、Spring如何实现事务、

JDBC如何实现事务、嵌套事务实现、分布式事务实现；

SQL的整个解析、执行过程原理、SQL行转列；

Redis
Redis为什么这么快？redis采用多线程会有哪些问题？

Redis支持哪几种数据结构；

Redis跳跃表的问题；

Redis单进程单线程的Redis如何能够高并发?

Redis如何使用Redis实现分布式锁？

Redis分布式锁操作的原子性，Redis内部是如何实现的？