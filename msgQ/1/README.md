# 消息队列的应用场景有哪些？

消息队列的应用场景主要有四个：异步处理、应用解耦、流量削锋和消息通讯。

异步处理：引入消息队列，将不是必须的业务逻辑，推入消息队列做异步处理，从而提高系统并发量与吞吐量。

应用解耦：当两个系统出现强耦合时，可以引入消息队列将两个系统进行解耦，比如订单系统与库存系统。

流量削锋：流量削锋也是消息队列中的常用场景，一般在秒杀和团抢活动中使用广泛！用户的请求，服务器接收后，首先写入消息队列。假如消息队列长度超过最大数量，则直接抛弃用户请求或跳转到错误页面。

日志处理：日志采集客户端，负责日志数据采集，定时写入 Kafka 队列；Kafka 消息队列：负责日志数据的接收、存储和转发；日志处理应用：订阅并消费kafka队列中的日志数据。