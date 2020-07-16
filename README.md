# DABODS

浙江大学NESC课题组实习项目——基于分布式的数据分析和管理系统。

## 0. 项目描述

本项目需要实现一个完整分布式数据分析和管理系统，最终的功能是定位物联设备的故障和物联数据可视化。以下是具体的实现细节：

（1）下载数据集和相关文献参考；

（2）模拟物联网设备，读取数据集，并通过合适的物联网通信协议发送数据到服务器；

（3）设计服务器整体架构，具备抗高并发、拓展性强等特点；

（4）服务器需具备对应的通信协议解析功能，并有较强的抗高并发能力；

（5）服务器需具备分布式计算能力，并实现物联设备数据分析、可视化和故障定位；

（6）采用合适的数据库类型，存储物联数据；

（7）完成实习报告，包括系统架构、系统性能、可视化情况等。

## 1. 资料下载

见仓库的[release](https://github.com/Neyzoter/dabods/releases)。

## 2. 项目建议

### 2.1 技术建议

（1）物联网模拟设备可以基于paho实现；

（2）物联网通信协议可以选择MQTT，并基于EMQ、Mosquito等开源中间件实现；也可以各种场景下的具体协议，比如交通部的JT/T808协议；

（3）MQTT解析后，可以选择再加入Kafka等消息中间件，分析加入消息中间件是优势还是劣势；

（4）分布式计算可以通过Spark、Flink等方式实现，而且两者具备机器学习库；也可以选择TensorFlow部署到TensoFlow Serving的方式实现；

（5）数据库可以选择时序数据库，比如InfluxDB、HBase等；

（6）数据可视化可以用JS自行实现，也可以使用InfluxDB自带的可视化功能或者Grafana可视化工具。

## 3. 其他说明

（1）实现语言不限；

（2）建议先实现基本功能，再提升局部性能；

## 4. 其他参考

[paho](https://github.com/eclipse?q=paho&type=&language=)

[EMQ](https://www.emqx.io/cn/)

[Mosquitto](https://mosquitto.org/)

[InfluxDB官网](https://www.influxdata.com/)

[InfluxDB小笔记](https://neyzoter.cn/wiki/InfluxDb/)

[时序数据库对比](https://neyzoter.cn/2019/09/14/Survey-On-Time-Series-DB/)

[MSCRED - AAAI中文解读](http://vlambda.com/wz_wJc078JGW6.html)

[Spark](http://spark.apache.org/)

[Flink](https://flink.apache.org/zh/flink-architecture.html)

[Kafka](http://kafka.apache.org/)