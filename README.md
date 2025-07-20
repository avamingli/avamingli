
<h1 align="center">Hi, I'm Zhang Mingli</h1>

# Database Kernel Developer:

* **Postgres Recognized Contributor** - [View Recognition](https://www.postgresql.org/message-id/Zv_zyxTfYmG9WgXn%40msg.df7cb.de)  
  &emsp;Features, Bug fix and patch review.
* **PostgreSQL ACE(China PostgreSQL Association).**
* **Greenplum Team (2019-2022, Pivotal/VMware)**  
  &emsp;Greenplum Committer & Main author of Greenplum Streaming Server (GPSS).
* **Apache Cloudberry Major Contributor & PPMC**  
  &emsp;Founding member of Cloudberry Database, which has contributed to the development of Apache Cloudberry.   
  &emsp;Contributed to almost every component of the system, such as planner, exetutor, storage, distributed transaction, etc.  
  &emsp;Main maintainer of Apache Cloudberry. A significant portion of the development work was completed before the project was  
  &emsp;open-sourced.  
  &emsp;Principal/ Sole author of many significant features: Parallel Query, AQUMV(Answer Query Using Materialized Views),  
  &emsp;Dynamic Tables and etc. Critical bug fixes and much more. 

# Open Source Contribution:
## Postgres:
  
  Critical commits:
* [Add support for LIKE in CREATE FOREIGN TABLE](https://github.com/postgres/postgres/commit/302cf15759233e654512979286ce1a5c3b36625f)
* [Detect redundant GROUP BY columns using UNIQUE indexes](https://github.com/postgres/postgres/commit/bd10ec529796a13670645e6acd640c6f290df020)
* [Disallow setting MAX_PARTITION_BUFFERS to less than 2](https://github.com/postgres/postgres/commit/c19615fe391c9577e2129fed4429736f6b5295da)
* [Remove useless LIMIT_OPTION_DEFAULT value from LimitOption](https://github.com/postgres/postgres/commit/a6be0600ac3b71dda8277ab0fcbe59ee101ac1ce)
* [Provide FORCE_NULL * and FORCE_NOT_NULL * options for COPY FROM](https://github.com/postgres/postgres/commit/f6d4c9cf162b70f2837fb6c2a83e80a3f3410695)
* [Remove code handling FORCE_NULL and FORCE_NOT_NULL for COPY TO](https://github.com/postgres/postgres/commit/8e621c10c73a93e1078ad85fe70fb4478537a798)
* [Fix ordering issue with WAL operations in GIN fast insert path](https://github.com/postgres/postgres/commit/56b662523fd49f75abe89d5bad54d377b2f36c24)
* [Avoid misbehavior when hash_table_bytes < bucket_size.](https://github.com/postgres/postgres/commit/55d9cd46f65a5fc0c3bbb69d36cc9dba597a8c9c)

## Greenplum:
  Some of critical fixes:
* [Fix several DistributedTransaction related issues (#13810)](https://github.com/greenplum-db/gpdb-archive/commit/87fbf064ba231e6bde03bdbb1c07af0adcbdc22f)
* [Optimize MPP FDW LIMIT/OFFSET push down when there is NULL/0. (#17246)](https://github.com/greenplum-db/gpdb-archive/commit/eeea7f194400bd0cfb90f399e53bcacd202fe6e9)
* [Fix incorrect result replicated table union all distributed table when gp_enable_direct_dispatch is off.](https://github.com/greenplum-db/gpdb-archive/commit/e49937c5923845378921372c84796f906d1c2d2e)
* [Fix gp_toolkit.__gp_aocsseg_history crash on non-aocs tables.](https://github.com/greenplum-db/gpdb-archive/commit/2c76c91c98a127ab5a290f1c7d711a31fd2e4e6e)
* [Fix gpconfig ssh retry undefined param issue. (#15283)](https://github.com/greenplum-db/gpdb-archive/commit/ed84aaa260269544d042795d4bed58bd71c2348d)

## Apache Cloudberry

#### Answer Query Using Materialized Views(AQUMV).  
  Sole Author, automatically answer query using the results of Materialized Views, Dynamic Tables and Incremental Materialized views in planner.    
* [Answer Query Using Materialized Views](https://github.com/apache/cloudberry/pull/298)
* [Maintain Data Status of Materialized Views for Partitioned Tables.](https://github.com/apache/cloudberry/pull/786)
* [Optimize Materialized View Status Maintenance for Partitioned Tables](https://github.com/apache/cloudberry/pull/990)
* [Optimize MV invalidation overhead using reference counting.](https://github.com/apache/cloudberry/pull/1029)
* [[Answer Query Using Materialized Views] Support ORDER BY in origin query](https://github.com/apache/cloudberry/pull/358)
* [[Answer Query Using Materialized Views] Support GROUP BY, GROUPING SETS, ROLLUP, CUBE in origin query.](https://github.com/apache/cloudberry/pull/342)
* [[Answer Query Using Materialized Views] Support HAVING clause in origin query](https://github.com/apache/cloudberry/pull/354)
* [[Answer Query Using Materialized Views] Compute Aggregations on Materialized Views.](https://github.com/apache/cloudberry/pull/322)
* [[AQUMV] Support DISTINCT clause on origin query.](https://github.com/apache/cloudberry/pull/439)
* [[Answer Query Using Materialized Views] Support Postgres special grammar DISTINCT ON clause on origin query.](https://github.com/apache/cloudberry/pull/441)
* [[Answer Query Using Materialized Views] Support LIMIT/OFFSET/FETCH clause on origin query.](https://github.com/apache/cloudberry/pull/446)
* [Fast path to REFRESH materialized view.](https://github.com/apache/cloudberry/pull/682)
* [[AQUMV] Answer Aggregation Query Directly.](https://github.com/apache/cloudberry/pull/705)
* [Maintain materialized view data status.](https://github.com/apache/cloudberry/pull/501)
* [[AQUMV]Allow to use normal materialized views to answer query.](https://github.com/apache/cloudberry/pull/528)
* [[AQUMV] Extend AQUMV to support materialized views on partitioned tables.](https://github.com/apache/cloudberry/pull/965)
* [Refactor Extend Protocol in libpq for Binary Data Handling](https://github.com/apache/cloudberry/pull/1098)
* [[AQUMV] Store view query in gp_matview_aux for view matching.](https://github.com/apache/cloudberry/pull/1117)
* [[AQUMV] Directly compute queries from materialized views with GROUP BY.](https://github.com/apache/cloudberry/pull/1143)

#### Parallel Query
Principal Author, Design and implement the architecture of Parallel Query in Greenplum/Apache Cloudberry based on Postgres’ parallel codes.

##### Contributions before open source:
* New locus: HashWorkers, SegmentGeneralWorkers.
* Locus compatible for parallel join including: Parallel Hash/Nestloop/Merge Join, Parallel-aware Hash Join. Parallel inner, left, anti, semi join.
* Append Only (AO) table’s Parallel SeqScan.
* Append Only Column Orientation(AOCS) table’s Parallel SeqScan.
* Parallel Create Table AS of AppendOnly table storage.
* Parallel Refresh Materialized Views of AO/AOCO storage.
* Explain(locus): show locus info of each plan node.
* Insert into multiple segfiles for AO/AOCS table.

##### Open source contributions:
* [Parallel DEDUP_SEMI and DEDUP_SEMI_REVERSE Join.](https://github.com/apache/cloudberry/pull/653)
* [Make UNION Parallel.](https://github.com/apache/cloudberry/pull/1213)
* [Parallel DISTINCT plan of multi-stage.](https://github.com/apache/cloudberry/pull/1173)
* [Parallel-oblivious Hash Left Anti Semi (Not-In) Join](https://github.com/apache/cloudberry/pull/30)
* [Implement Parallel-aware Hash Left Anti Semi (Not-In) Join](https://github.com/apache/cloudberry/pull/149)
* [Fix wrong results of Left Anti Semi (Not-In) Join](https://github.com/apache/cloudberry/pull/130)
* [Add motionhazard to the outer side of parallel aware join.(fix flaky incorrect results of agg)](https://github.com/apache/cloudberry/pull/284)
* [Refactor cdbpath_motion_for_parallel_join() by outer join inner style](https://github.com/apache/cloudberry/pull/98)
* [Open proper AO/AOCS segment files according to data volume](https://github.com/apache/cloudberry/pull/248)
* [Fix AO/AOCS insertDesc memory issue](https://github.com/apache/cloudberry/pull/365)
* [Fix segfilecount of AO/AOCO when bulk insertion: COPY](https://github.com/apache/cloudberry/pull/530)


#### Other Features:
* [[Feature] Dynamic Table.](https://github.com/apache/cloudberry/pull/725)
* [Let Replicated locus join with others(Results of writeable CTE on replicated table Join with others)](https://github.com/apache/cloudberry/pull/84)
* [Enable SingleQE join with SegmentGeneralWorkers](https://github.com/apache/cloudberry/pull/327)
* [Implement 3-phase aggregation with DEDUP HashAgg for DISTINCT.](https://github.com/apache/cloudberry/pull/676)
* [Optimize DISTINCT, ORDER BY and DISTINCT ON when Aggregation without Group By.](https://github.com/apache/cloudberry/pull/685)


# A Journey of Passion: My Story (Chinese)
  * [第三位中国成员！CloudberryDB 核心开发者张明礼入选 PostgreSQL Contributor 名单](https://mp.weixin.qq.com/s/zTC1qXAe4M9XkDXp-2LEyw)
  * [PostgreSQL 16 中国贡献者专访：张明礼](https://mp.weixin.qq.com/s/jVSpFDQt4Sby2XyNTC7vYw)
  * [PostgreSQL全球开发组公布 “New PostgreSQL Contributors”](https://mp.weixin.qq.com/s/hyuxaWyGCS51-ID2rqLXmw)
  * [PostgreSQL 15发布  HashData贡献关键力量](https://mp.weixin.qq.com/s/EqNQxY9GHYuPIAmYv1WM6g)

# Tech Talk (Chinese)
![---_画板 1](https://github.com/user-attachments/assets/77908b91-4b36-4be5-81c6-1150d10f04be)

  * [从单进程到并行化：Append-Only表并行扫描内核解析](https://mp.weixin.qq.com/s/1tGA15ZvIqqAMmbIEhgbmg)
  * [Postgres内核代码100万行，怎么读?](https://mp.weixin.qq.com/s/YPeZ6LjR-Zlf4ZhkPhUqvA?token=240283712&lang=zh_CN)
  * [探索Greenplum/Cloudberry：如何实现数据MPP加载](https://mp.weixin.qq.com/s/cbtbkU_h1wNWnDeiZW6riQ?token=240283712&lang=zh_CN)
  * [CloudberryDB并行化查询之路](https://www.bilibili.com/video/BV1nz4y1A7jP/?share_source=copy_web&vd_source=7ab59479316c3260a8af8ad675a3150d)
  * [Answer Query Using Materizlied Views/利用物化视图进行查询改写](https://www.bilibili.com/video/BV19PyzYUESY/?vd_source=8981cae9a2ba32197a3c2fc070f1464b)



<!--
# Open Source Contributions

## Postgres: 

**[Postgres 15 Contributor Acknowledgement(Zhang Mingli)](https://www.postgresql.org/docs/current/release-15.html#RELEASE-15-ACKNOWLEDGEMENTS)**

**[Postgres 16 Contributor Acknowledgement(Mingli Zhang)](https://www.postgresql.org/docs/16/release-16.html#RELEASE-16-ACKNOWLEDGEMENTS)**
-->
