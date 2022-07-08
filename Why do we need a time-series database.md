#         Why do we need a time-series database? 

​	Due to the proliferative use of big data in fields such as e-commerce, media and administration, the number of databases increases steeply and the importance of database draws attention of  people. among a multitude of kinds of database, the time-series database which is purpose-built to process mass of time-series data is rising and getting more popular. 

​	So why do we need a time-series database?  Why those time-series database have became more popular? I deem that I can give a brief introduction in this article.

### 1. What is time-series database?

​	First and foremost, we should comprehend the time-series data. Time series data, which is also referred to as time-stamped data, is a sequence of data points indexed in time order. Time-stamped is data collected at different points in time. These data points typically consist of successive measurements made from the same source over a time interval and are used to track change over time. For instance, If we use a thermometer to measure the temperature of a city all the time for a day, and record these temperatures, these are time-series data.

​	Time-series data is structured and rarely updated or deleted. A collection point's data source is unique, the data must be searched in a specified period and a specified area. It is estimated that more than 10 billion pieces of time-series data are generated every single day. By connecting these data, we can make a multi-latitude report in the past to reveal its tendency, regularity and anomaly. 

​	In recent years, the application of time-series data exerts a salutary effect in many fields including the IOT, economic and financial field, environmental monitoring, medical, industrial manufacturing, agricultural production field, system monitoring of hardware and software and so on.

​	Obviously, time-series database is aimed at storing and processing time-series data, and it supports some basic functions such as fast writing of time-series data, persistence, and multi-latitude aggregated query.  Whereas traditional databases only record the current value of data, time-series databases record all historical data. At the same time, time is always used as a filter condition in the query of time series data. 

### 2. The history of time-series database 

​	<img src="https://pics4.baidu.com/feed/72f082025aafa40ff32c0ee4e34dff4779f019d7.jpeg?token=11c41b43eb56d4fb34fe0eef47d8e521" alt="img" style="zoom:150%;" />

  As shown in the figure above,the development of time-series database can be traced back to the 1990s, when the demand for timing data storage came into being in the monitoring field. The first generation of timing databases, represented by RRDTool and Whisper, using fixed-size databases to rapidly store numerical data over time, it's often embedded in the monitoring system. 

​	With the development of big data, time-series data has exploded. Not only monitoring systems, but also other systems have more requirements for processing time-series data. In 2011, time-series databases represented by OpenTSDB and KairosDB which are based on distributed storage and optimize for time began to appear.

​	In 2013, the vertical sequential database represented by InfluxDB has become the mainstream of the time-series database which has more efficient storage, reading and other data processing capabilities and efficient compression algorithms for time-series data.

![image-20220707222641803](C:\Users\Lucas Wang\AppData\Roaming\Typora\typora-user-images\image-20220707222641803.png)

​	The figure above explicitly illustrates the development of time-series database, the popularity of time-series database increased quickly from 250 in 2018 to 600 in 2022 which demonstrates that time-series database has become the second most popular database nowadays.

### 3. The advantages of time-series database

(1) Storage cost:  

​	TSDB takes advantage of the characteristics of time increasing, dimension repeating and index smooth change, chooses reasonable coding compression algorithm to improve the data compression ratio. in other hands, TSDB pre-reduce the accuracy to aggregate historical data and save storage space.  

(2) Highly concurrent write:  

​	TSDB writes data in batches to reduce network overhead.  Data is written to the memory and then periodically dumped as immutable files.  

(3) Low query delay, highly query concurrency:  

​	TSDB optimizes common query mode and reduce query delay through index and other technologies.  Improve query concurrency through caching and routing. 

### 4. The application scenarios of time-series database

​	Now TSDB has been widely used in the IOT, enterprise energy management, Internet supervision, power detection system, etc.  

​	(1) IOT device status monitoring analysis. a variety of IOT devices can be connected to the cloud through the platform, and the status data of the devices can be written into the timing database in real time efficiently. It can provide the following three functions: reading real-time data through the data API interface of the time-series database; With the advantage of fast query speed of time series database, data reports are obtained by aggregating the data. The change trend and curve of the data can be obtained visually through the console or objects of the sequential database to help users analyze the data connotation.  

​	(2) Internet service performance monitoring service. Internet service can write user access delay, query return efficiency, and business service indicator monitoring data into the sequential database, which can perform multi-dimensional aggregation analysis and display monitoring items. For example, a website service provider needs to record the clarity, smoothness, clicks, visits and other information of each web page in real time, that is, these monitoring items can be written into the timing database at a certain frequency. According to certain aggregation conditions, which carrier network is smoother in a certain period of time; Look at a site's fluency curve for the past day/week; Find how clicks change over time.  

​	(3) Real-time analysis of big data. User data reported by various acquisition terminals and business status data obtained by log cleaning programs are stored in the timing database. Finally, data is obtained through API to achieve efficient real-time analysis and modeling. 

### 5. What will the future of time-series database be?

![image-20220707222711931](C:\Users\Lucas Wang\AppData\Roaming\Typora\typora-user-images\image-20220707222711931.png)

​	The figure above reveals the popularity trend of the last 24 months about DBMS according to DB-engines. We can assert that the time-series database has been the most active and well-regarded DBMS and it's popularity has increasing over time. As time-series data plays a pivot role in many fields, I maintain that TSDB will show it's capabilities and impose a instrumental effect in those fields.

​	![](C:\Users\Lucas Wang\AppData\Roaming\Typora\typora-user-images\image-20220707222133779.png)

​		As we can see above, we can assert utterly that  InfluxDB is the most remarkable TSDB in kinds of TSDB because of it's powerful and comprehensive functions. A domestic time-series database---TDengine which is established by TAOS data ranks 13. 

### 6. Summary

​	Time-series database is in the stage of rapid development, time-series data technology is gradually mature, but this is by no means the end, time-series data technology is still facing a variety of new requirements and challenges. While improving the performance of time-series database, major manufacturers are putting forward more solutions to meet the new requirements. Facing these challenges and opportunities, we believe that time-series database will have further development in the future. 

### 7. Reference

 1.https://developer.aliyun.com/article/202551

 2.https://baijiahao.baidu.com/s?id=1708500603441764092

 3.https://www.ksyun.com/developer/article/22060.html