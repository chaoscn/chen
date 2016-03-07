## [1 Billion Reasons Why Adobe Chose HBase ](/blog/2010/3/16/1-billion-reasons-why-adobe-chose-hbase.html)
## [为什么adobe选择HBase](link)

Cosmin Lehene ﻿wrote two excellent articles on Adobe's experiences with HBase: [Why we’re using HBase: Part 1](http://hstack.org/why-were-using-hbase-part-1/) and [Why we’re using HBase: Part 2](http://hstack.org/why-were-using-hbase-part-2/). Adobe needed a _generic,_ _real-time, structured data storage and processing system that could handle any data volume, with access times under 50ms, with no downtime and _no data loss__. The article goes into great detail about their experiences with HBase and their evaluation process, providing a "well reasoned impartial use case from a commercial user". It talks about failure handling, availability, write performance, read performance, random reads, sequential scans, and consistency. 

Cosmin Lehene写了两篇很好的关于Adobe使用Hbase的文章 [Why we’re using HBase: Part 1](http://hstack.org/why-were-using-hbase-part-1/) and [Why we’re using HBase: Part 2](http://hstack.org/why-were-using-hbase-part-2/).
Adobe需要一个通用的，实时的，结构化的存储系统能处理任何量级的数据，并且能在50ms之内读取数据，同时没有服务器停工时间，没有数据丢失发生。文章详细的解释了他们用Hbase的经验跟他们的评价。客观的从商业用户的角度给定了一个公正的评价。其中还谈到了异常的处理，有效性，读写的性能，随机读写，顺序扫描跟一致性。

One of the knocks against HBase has been it's complexity, as it has many parts that need installation and configuration. All is not lost according to the Adobe team:

反对Hbase的观点基本是说它过于复杂，有太多需要安装和配置的地方。这些在书中也根据Adobe小组使用提到：

> HBase is more complex than other systems (you need Hadoop, Zookeeper, cluster machines have multiple roles). We believe that for HBase, this is not accidental complexity and that the argument that “HBase is not a good choice because it is complex” is irrelevant. The advantages far outweigh the problems. Relying on decoupled components plays nice with the Unix philosophy: do one thing and do it well. Distributed storage is delegated to HDFS, so is distributed processing, cluster state goes to Zookeeper. All these systems are developed and tested separately, and are good at what they do. More than that, this allows you to scale your cluster on separate vectors. This is not optimal, but it **allows for incremental investment** in either spindles, CPU or RAM. You don’t have to add them all at the same time.

Highly recommended, especially if you need some sort of balance to the recent gush of Cassandra articles. 
