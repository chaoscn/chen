## [1 Billion Reasons Why Adobe Chose HBase ](/blog/2010/3/16/1-billion-reasons-why-adobe-chose-hbase.html)


Cosmin Lehene ﻿wrote two excellent articles on Adobe's experiences with HBase: [Why we’re using HBase: Part 1](http://hstack.org/why-were-using-hbase-part-1/) and [Why we’re using HBase: Part 2](http://hstack.org/why-were-using-hbase-part-2/). Adobe needed a _generic,_ _real-time, structured data storage and processing system that could handle any data volume, with access times under 50ms, with no downtime and _no data loss__. The article goes into great detail about their experiences with HBase and their evaluation process, providing a "well reasoned impartial use case from a commercial user". It talks about failure handling, availability, write performance, read performance, random reads, sequential scans, and consistency. 

One of the knocks against HBase has been it's complexity, as it has many parts that need installation and configuration. All is not lost according to the Adobe team:

> HBase is more complex than other systems (you need Hadoop, Zookeeper, cluster machines have multiple roles). We believe that for HBase, this is not accidental complexity and that the argument that “HBase is not a good choice because it is complex” is irrelevant. The advantages far outweigh the problems. Relying on decoupled components plays nice with the Unix philosophy: do one thing and do it well. Distributed storage is delegated to HDFS, so is distributed processing, cluster state goes to Zookeeper. All these systems are developed and tested separately, and are good at what they do. More than that, this allows you to scale your cluster on separate vectors. This is not optimal, but it **allows for incremental investment** in either spindles, CPU or RAM. You don’t have to add them all at the same time.

Highly recommended, especially if you need some sort of balance to the recent gush of Cassandra articles. 
