# MIT6.824
MIT6.824-Distributed System(Spring2020)

Course website: https://pdos.csail.mit.edu/6.824/schedule.html 



MapReduce



GFS

Raft



















#### 分布式系统的研究概览

(https://www.zhihu.com/question/23645117/answer/124708083): 

1. 分布式存储系统 
   - 结构化存储: RDBMS,典型的例如MySQL的发展
   - 非结构化存储 : 分布式文件系统, 早期的分布式文件系统并不支持fault tolerance和recovery直到GFS和开源实现的HDFS.
   - 半结构化存储: 为了解决非结构化存储随机访问性差的问题, 应用比如NoSQL,KV Store,甚至对象存储(protobuf, thrift). 
     - NoSQL既具有分布式文件系统的扩展性, 又有结构化存储的随机访问能力, 抛弃RDBMS复杂的SQL查询和ACID事务.有名的系统例如 Google:Bigtable, Amazon: Dynamo还有工业界的HBase, Cassandra. 比如Bigtable是基于LevelDB, 底层数据结构是LSM-Tree.
   - In-memory 存储 : 比如Memchached和Redis
   - 一些理论系统例如Paxos,CAP,ConsistentHash, Timing
2. 分布式计算系统
   - 传统基于msg的系统
   - MapReduce-like 系统
   - 图计算系统
   - 基于状态(state)的系统
   - Streaming系统
3. 分布式管理系统 