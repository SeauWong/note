# RabbitMQ

1. [RabbitMQ：消息发送确认 与 消息接收确认(ACK)](https://www.jianshu.com/p/2c5eebfd0e95)

# Kafka

1. [kafka安装](https://www.cnblogs.com/flower1990/p/7466882.html)
2. [启动错误: 找不到或无法加载主类 Files\Java\jdk1.8.0_101\lib\dt.jar;C:\Program](https://blog.csdn.net/cx2932350/article/details/78870135)

# Git

1. [Git图解](https://learngitbranching.js.org/)

# Nginx
1. [windows下nginx的安装及使用](https://www.cnblogs.com/jiangwangxiang/p/8481661.html)

# Spring事务

### @Transactional的readOnly
* readOnly的意思就是当前的方法是只读的，也就是说当前的方法中没有需要处理事务（insert,update,delete）的操作。则可以加上readOnly=true
* 使用它的好处是Spring会把你优化这方法，使用了readOnly=true，也就是使用了一个只读的connection。效率会高很多
* 例如：如下方法，userAdd肯定用到了insert操作。此时加上readOnly=true的话则会报错，插入不成功。
```java
@Transactional(readOnly=true)
public void userAdd(User user) {
    userDao.userAdd(user);
}
```
* readOnly的使用场景：
1. 只有查询操作的方法上（查询量比较大）
2. 确保当前方法不会出现insert,update,delete情况时，可以使用readOnly=true
3. 防止当前方法会出现insert,update,delete

### @Transactional的timeout
* 事务的超时时间：Transaction时间太长的话，将它停止掉。默认-1

# mybatis

[Mybatis Update操作返回值问题](https://www.cnblogs.com/jpfss/p/8918315.html)
