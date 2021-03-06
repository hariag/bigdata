Hadoop，HBase，Storm，Spark到底是什么？

HDFS: 存储系统
MapReduce：计算系统
Hive：提供给SQL开发人员（通过HiveQL）的MapReduce，基于Hadoop的数据仓库框架
Pig：基于Hadoop的语言开发的
Hbase:NoSQL数据库
Flume：一个收集处理Hadoop数据的框架
Oozie：一个让用户以多种语言（如MapReduce，Pig和Hive）定义一系列作业的工作流处理系统
Ambari：一个基于web的部署/管理/监控Hadoop集群的工具集
Avro：允许编码Hadoop文件的schema的一种数据序列化系统
Mahout：一个数据挖掘库，它包含了最流行的一些数据挖据算法，并且以MapReduce模型来实现他们
Sqoop：一个从非Hadoop数据存储（如关系数据库和数据仓库）进来的移动数据到Hadoop中的连接工具
HCatalog：一个中心化的元数据管理以及Apache Hadoop共享服务，它允许在Hadoop集群中的所有数据的统一视图，并允许不同的工具，包括Pig和Hive，处理任何数据元素，而无需知道身体在集群中的数据存储。

BigTop：为了创造一个更正式的程序或框架Hadoop的子项目及相关组件的目标提高Hadoop的平台，作为一个整体的包装和互操作性测试。

Apache  Storm：一个分布式实时计算系统，Storm是一个任务并行连续计算引擎。 Storm本身并不典型在Hadoop集群上运行，它使用Apache ZooKeeper的和自己的主/从工作进程，协调拓扑，主机和工作者状态，保证信息的语义。无论如何， Storm必定还是可以从HDFS文件消费或者从文件写入到HDFS。

Apache Spark：一种快速，通用引擎用于大规模数据处理，Spark是一个数据并行通用批量处理引擎。工作流中在一个类似的和怀旧风格的MapReduce中定义，但是，比传统Hadoop MapReduce的更能干。Apache Spark有其流API项目，该项目通过短间隔批次允许连续处理。Apache Spark本身并不需要Hadoop操作。但是，它的数据并行模式，需要稳定的数据优化使用共享文件系统。该稳定源的范围可以从S3，NFS或更典型地，HDFS。执行Spark应用程序并不需要Hadoop YARN。Spark有自己独立的主/服务器进程。然而，这是共同的运行使用YARN容器Spark的应用程序。此外，Spark还可以在Mesos集群上运行。
