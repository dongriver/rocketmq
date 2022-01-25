#源码说明文档
##1、概述：官方相关资料
##2、组成组件
##3、协作流程图
##4、功能分类与关键词
##5、代码入口
 - [namesrv](NamesrvStartup.java)：org.apache.rocketmq.namesrv.NamesrvStartup
 - [broker](BrokerStartup.java)：org.apache.rocketmq.broker.BrokerStartup
 
 - [producer生产者]()：
 DefaultMQProducer producer = new DefaultMQProducer(topic); 
 producer.setNamesrvAddr("127.0.0.1:9876"); producer.start(); 
 Message msg = new Message(topic, "testTag", "testKey", "testMessage".getBytes()); 
 SendResult result = producer.send(msg);
 
 - [consumer消费者]()：
 // 实例化消费者 
 DefaultMQPushConsumer consumer = new DefaultMQPushConsumer("please_rename_unique_group_name"); 
 // 设置NameServer的地址 
 consumer.setNamesrvAddr("localhost:9876"); 
 // 订阅一个或者多个Topic，以及Tag来过滤需要消费的消息 
 consumer.subscribe("TopicTest", "*");
 // 启动消费者实例 
 consumer.start();
 
###5.1、源码详情

##6、配置属性说明
##7、场景使用场景
##8、public项目工具源码
##9、重复消费涉及相关代码
##10、写得很好的网址
https://gitee.com/leopards/RocketMQ
 