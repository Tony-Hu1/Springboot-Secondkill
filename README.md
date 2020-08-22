# SpringBoot-SecondKill

#### 介绍
基于SpringBoot+Mybatis+Mysql+中间件构建的商城秒杀系统；其中，中间件主要包括：缓存中间件Redis、消息中间件RabbitMQ、统一协调调度中心中间件ZooKeeper、综合中间件Redisson等等，详细的技术列表可以参见下方“系统整体架构说明”




#### 系统整体架构说明
（1）技术列表：
![alt 核心技术列表](https://img2020.cnblogs.com/blog/1786066/202008/1786066-20200822122218322-851977985.png)

（2）系统整体业务流程：
![alt 系统整体业务流程](https://images.gitee.com/uploads/images/2019/0824/235302_03ea97cd_1442143.png)


(3)部分运行效果截图： 
   
				                  商品首页	
![alt 运行效果1](https://images.gitee.com/uploads/images/2019/0824/235302_3a6851d7_1442143.png)    
   
				                 图书商品详情

![alt 运行效果2](https://images.gitee.com/uploads/images/2019/0824/235302_de1cfc85_1442143.png)   
   
				                  抢购成功
 
![alt 运行效果3](https://images.gitee.com/uploads/images/2019/0824/235302_6cfca7e5_1442143.png)   
 

#### 开发软件与工具
IntelliJ IDEA  
Navicat Premium  
SpringBoot 1.5.7  
JDK1.8  
Mysql5.6  
Tomcat9  
JMeter5.1  
PostMan  
Redis_Windows的简化安装版
ZooKeeper_Windows的简化安装版(Zookeeper-3.4.6)--当然，如果自己有Linux服务器，也可以连接Linux的  

#### 如何运行整个系统  
1.首先需要在本地开发环境启动Redis、ZooKeeper服务（假设整套系统连接的服务是本地的）:双击Redis、ZooKeeper-Windows简化安装版的bin目录，Redis找寻redis-server.exe，ZooKeeper找寻zkServer.cmd文件，双击即可启动相应的服务     
2.将数据库的DDL，即db_second_kill.sql导入到你本地数据库中（前提是你得先建好数据库db_second_kill）     
3.将项目从仓库clone下来，并import进IDEA中，调整IDEA的maven仓库指向，最终将所需要的jar包都下载下来！(如果有一些Jar下载不下来，自己检查一下网络原因跟maven仓库原因吧!)    
4.修改application.properties配置文件中相应的配置信息，比如数据库连接信息等等；    
5.将系统运行在Tomcat服务器上，观察控制台的输出信息，如果没有报错，那么运行之后一般会自动跳转至首页！  
6.最后，可以开心的玩耍了！ 