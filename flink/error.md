# error
## 3.1.0
```
Exception in thread "main" java.lang.RuntimeException: Error to list databases: Access denied for user 'bigdb_admin'@'10.80.130.%' to database 'bigdata'
        at org.apache.flink.cdc.connectors.mysql.utils.MySqlSchemaUtils.listTables(MySqlSchemaUtils.java:70)
        at org.apache.flink.cdc.connectors.mysql.factory.MySqlDataSourceFactory.getTableList(MySqlDataSourceFactory.java:232)
        at org.apache.flink.cdc.connectors.mysql.factory.MySqlDataSourceFactory.createDataSource(MySqlDataSourceFactory.java:158)
        at org.apache.flink.cdc.composer.flink.translator.DataSourceTranslator.translate(DataSourceTranslator.java:52)
        at org.apache.flink.cdc.composer.flink.FlinkPipelineComposer.compose(FlinkPipelineComposer.java:101)
        at org.apache.flink.cdc.cli.CliExecutor.run(CliExecutor.java:71)
        at org.apache.flink.cdc.cli.CliFrontend.main(CliFrontend.java:71)
Caused by: java.sql.SQLSyntaxErrorException: Access denied for user 'bigdb_admin'@'10.80.130.%' to database 'bigdata'
        at com.mysql.cj.jdbc.exceptions.SQLError.createSQLException(SQLError.java:120)
        at com.mysql.cj.jdbc.exceptions.SQLExceptionsMapping.translateException(SQLExceptionsMapping.java:122)
        at com.mysql.cj.jdbc.StatementImpl.executeQuery(StatementImpl.java:1201)
        at io.debezium.jdbc.JdbcConnection.query(JdbcConnection.java:553)
        at io.debezium.jdbc.JdbcConnection.query(JdbcConnection.java:496)
        at org.apache.flink.cdc.connectors.mysql.utils.MySqlSchemaUtils.listTables(MySqlSchemaUtils.java:111)
        at org.apache.flink.cdc.connectors.mysql.utils.MySqlSchemaUtils.listTables(MySqlSchemaUtils.java:66)
        ... 6 more
```

## 3.0.1
```
Setting HBASE_CONF_DIR=/etc/hbase/conf because no HBASE_CONF_DIR was set.
SLF4J: Class path contains multiple SLF4J bindings.
SLF4J: Found binding in [jar:file:/opt/flink-1.16.2/lib/log4j-slf4j-impl-2.17.1.jar!/org/slf4j/impl/StaticLoggerBinder.class]
SLF4J: Found binding in [jar:file:/opt/cloudera/parcels/CDH-6.3.1-1.cdh6.3.1.p0.1470567/jars/slf4j-log4j12-1.7.25.jar!/org/slf4j/impl/StaticLoggerBinder.class]
SLF4J: See http://www.slf4j.org/codes.html#multiple_bindings for an explanation.
SLF4J: Actual binding is of type [org.apache.logging.slf4j.Log4jLoggerFactory]
Exception in thread "main" java.lang.RuntimeException: Error to list databases: Access denied for user 'bigdb_admin'@'10.80.130.%' to database 'bigdata'
        at com.ververica.cdc.connectors.mysql.utils.MySqlSchemaUtils.listTables(MySqlSchemaUtils.java:68)
        at com.ververica.cdc.connectors.mysql.factory.MySqlDataSourceFactory.getTableList(MySqlDataSourceFactory.java:212)
        at com.ververica.cdc.connectors.mysql.factory.MySqlDataSourceFactory.createDataSource(MySqlDataSourceFactory.java:153)
        at com.ververica.cdc.composer.flink.translator.DataSourceTranslator.translate(DataSourceTranslator.java:54)
        at com.ververica.cdc.composer.flink.FlinkPipelineComposer.compose(FlinkPipelineComposer.java:101)
        at com.ververica.cdc.cli.CliExecutor.run(CliExecutor.java:65)
        at com.ververica.cdc.cli.CliFrontend.main(CliFrontend.java:62)
Caused by: java.sql.SQLSyntaxErrorException: Access denied for user 'bigdb_admin'@'10.80.130.%' to database 'bigdata'
        at com.mysql.cj.jdbc.exceptions.SQLError.createSQLException(SQLError.java:120)
        at com.mysql.cj.jdbc.exceptions.SQLExceptionsMapping.translateException(SQLExceptionsMapping.java:122)
        at com.mysql.cj.jdbc.StatementImpl.executeQuery(StatementImpl.java:1201)
        at io.debezium.jdbc.JdbcConnection.query(JdbcConnection.java:553)
        at io.debezium.jdbc.JdbcConnection.query(JdbcConnection.java:496)
        at com.ververica.cdc.connectors.mysql.utils.MySqlSchemaUtils.listTables(MySqlSchemaUtils.java:109)
        at com.ververica.cdc.connectors.mysql.utils.MySqlSchemaUtils.listTables(MySqlSchemaUtils.java:64)
        ... 6 more
```
## 3.1.0
```
Setting HBASE_CONF_DIR=/etc/hbase/conf because no HBASE_CONF_DIR was set.
SLF4J: Class path contains multiple SLF4J bindings.
SLF4J: Found binding in [jar:file:/opt/flink-1.16.2/lib/log4j-slf4j-impl-2.17.1.jar!/org/slf4j/impl/StaticLoggerBinder.class]
SLF4J: Found binding in [jar:file:/opt/cloudera/parcels/CDH-6.3.1-1.cdh6.3.1.p0.1470567/jars/slf4j-log4j12-1.7.25.jar!/org/slf4j/impl/StaticLoggerBinder.class]
SLF4J: See http://www.slf4j.org/codes.html#multiple_bindings for an explanation.
SLF4J: Actual binding is of type [org.apache.logging.slf4j.Log4jLoggerFactory]
Exception in thread "main" java.lang.NoSuchFieldError: SINK_USE_NEW_SINK_API
        at org.apache.flink.cdc.connectors.starrocks.sink.StarRocksDataSinkFactory.buildSinkConnectorOptions(StarRocksDataSinkFactory.java:122)
        at org.apache.flink.cdc.connectors.starrocks.sink.StarRocksDataSinkFactory.createDataSink(StarRocksDataSinkFactory.java:43)
        at org.apache.flink.cdc.composer.flink.FlinkPipelineComposer.createDataSink(FlinkPipelineComposer.java:164)
        at org.apache.flink.cdc.composer.flink.FlinkPipelineComposer.compose(FlinkPipelineComposer.java:129)
        at org.apache.flink.cdc.cli.CliExecutor.run(CliExecutor.java:71)
        at org.apache.flink.cdc.cli.CliFrontend.main(CliFrontend.java:71)
```

```
2024-06-05 13:24:50
org.apache.flink.streaming.runtime.tasks.StreamTaskException: Cannot instantiate user function.
	at org.apache.flink.streaming.api.graph.StreamConfig.getStreamOperatorFactory(StreamConfig.java:399)
	at org.apache.flink.streaming.runtime.tasks.OperatorChain.createOperator(OperatorChain.java:763)
	at org.apache.flink.streaming.runtime.tasks.OperatorChain.createOperatorChain(OperatorChain.java:736)
	at org.apache.flink.streaming.runtime.tasks.OperatorChain.createOutputCollector(OperatorChain.java:676)
	at org.apache.flink.streaming.runtime.tasks.OperatorChain.createOperatorChain(OperatorChain.java:726)
	at org.apache.flink.streaming.runtime.tasks.OperatorChain.createOutputCollector(OperatorChain.java:676)
	at org.apache.flink.streaming.runtime.tasks.OperatorChain.<init>(OperatorChain.java:195)
	at org.apache.flink.streaming.runtime.tasks.RegularOperatorChain.<init>(RegularOperatorChain.java:60)
	at org.apache.flink.streaming.runtime.tasks.StreamTask.restoreInternal(StreamTask.java:685)
	at org.apache.flink.streaming.runtime.tasks.StreamTask.restore(StreamTask.java:672)
	at org.apache.flink.runtime.taskmanager.Task.runWithSystemExitMonitoring(Task.java:935)
	at org.apache.flink.runtime.taskmanager.Task.restoreAndInvoke(Task.java:904)
	at org.apache.flink.runtime.taskmanager.Task.doRun(Task.java:728)
	at org.apache.flink.runtime.taskmanager.Task.run(Task.java:550)
	at java.base/java.lang.Thread.run(Thread.java:834)
Caused by: java.io.InvalidClassException: com.starrocks.data.load.stream.properties.StreamLoadProperties; local class incompatible: stream classdesc serialVersionUID = 1230732817680638024, local class serialVersionUID = -3071747118591617397
	at java.base/java.io.ObjectStreamClass.initNonProxy(ObjectStreamClass.java:571)
	at java.base/java.io.ObjectInputStream.readNonProxyDesc(ObjectInputStream.java:2042)
	at java.base/java.io.ObjectInputStream.readClassDesc(ObjectInputStream.java:1892)
	at java.base/java.io.ObjectInputStream.readOrdinaryObject(ObjectInputStream.java:2223)
	at java.base/java.io.ObjectInputStream.readObject0(ObjectInputStream.java:1709)
	at java.base/java.io.ObjectInputStream.defaultReadFields(ObjectInputStream.java:2518)
	at java.base/java.io.ObjectInputStream.readSerialData(ObjectInputStream.java:2412)
	at java.base/java.io.ObjectInputStream.readOrdinaryObject(ObjectInputStream.java:2250)
	at java.base/java.io.ObjectInputStream.readObject0(ObjectInputStream.java:1709)
	at java.base/java.io.ObjectInputStream.defaultReadFields(ObjectInputStream.java:2518)
	at java.base/java.io.ObjectInputStream.readSerialData(ObjectInputStream.java:2412)
	at java.base/java.io.ObjectInputStream.readOrdinaryObject(ObjectInputStream.java:2250)
	at java.base/java.io.ObjectInputStream.readObject0(ObjectInputStream.java:1709)
	at java.base/java.io.ObjectInputStream.readObject(ObjectInputStream.java:500)
	at java.base/java.io.ObjectInputStream.readObject(ObjectInputStream.java:458)
	at org.apache.flink.util.InstantiationUtil.deserializeObject(InstantiationUtil.java:617)
	at org.apache.flink.util.InstantiationUtil.deserializeObject(InstantiationUtil.java:602)
	at org.apache.flink.util.InstantiationUtil.deserializeObject(InstantiationUtil.java:589)
	at org.apache.flink.util.InstantiationUtil.readObjectFromConfig(InstantiationUtil.java:543)
	at org.apache.flink.streaming.api.graph.StreamConfig.getStreamOperatorFactory(StreamConfig.java:383)
	... 14 more

```

## 超时报错
```
org.apache.flink.table.client.gateway.SqlExecutionException: Could not execute SQL statement.
        at org.apache.flink.table.client.gateway.local.LocalExecutor.executeOperation(LocalExecutor.java:208) ~[flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.gateway.local.LocalExecutor.executeQuery(LocalExecutor.java:228) ~[flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.cli.CliClient.callSelect(CliClient.java:542) ~[flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.cli.CliClient.callOperation(CliClient.java:446) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.cli.CliClient.executeOperation(CliClient.java:372) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.cli.CliClient.getAndExecuteStatements(CliClient.java:329) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.cli.CliClient.executeInteractive(CliClient.java:280) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.cli.CliClient.executeInInteractiveMode(CliClient.java:228) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.SqlClient.openCli(SqlClient.java:151) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.SqlClient.start(SqlClient.java:95) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.SqlClient.startClient(SqlClient.java:187) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.SqlClient.main(SqlClient.java:161) [flink-sql-client-1.16.2.jar:1.16.2]
Caused by: org.apache.flink.table.api.TableException: Failed to execute sql
        at org.apache.flink.table.api.internal.TableEnvironmentImpl.executeQueryOperation(TableEnvironmentImpl.java:903) ~[flink-table-api-java-uber-1.16.2.jar:1.16.2]
        at org.apache.flink.table.api.internal.TableEnvironmentImpl.executeInternal(TableEnvironmentImpl.java:1382) ~[flink-table-api-java-uber-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.gateway.local.LocalExecutor.executeOperation(LocalExecutor.java:206) ~[flink-sql-client-1.16.2.jar:1.16.2]
        ... 11 more
Caused by: org.apache.flink.util.FlinkException: Failed to execute job 'collect'.
        at org.apache.flink.streaming.api.environment.StreamExecutionEnvironment.executeAsync(StreamExecutionEnvironment.java:2203) ~[flink-dist-1.16.2.jar:1.16.2]
        at org.apache.flink.table.planner.delegation.DefaultExecutor.executeAsync(DefaultExecutor.java:95) ~[flink-table-planner_2.12-1.16.2.jar:1.16.2]
        at org.apache.flink.table.api.internal.TableEnvironmentImpl.executeQueryOperation(TableEnvironmentImpl.java:884) ~[flink-table-api-java-uber-1.16.2.jar:1.16.2]
        at org.apache.flink.table.api.internal.TableEnvironmentImpl.executeInternal(TableEnvironmentImpl.java:1382) ~[flink-table-api-java-uber-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.gateway.local.LocalExecutor.executeOperation(LocalExecutor.java:206) ~[flink-sql-client-1.16.2.jar:1.16.2]
        ... 11 more
Caused by: org.apache.flink.runtime.client.JobSubmissionException: Failed to submit JobGraph.
        at org.apache.flink.client.program.rest.RestClusterClient.lambda$submitJob$11(RestClusterClient.java:448) ~[flink-dist-1.16.2.jar:1.16.2]
        at java.util.concurrent.CompletableFuture.uniExceptionally(CompletableFuture.java:986) ~[?:?]
        at java.util.concurrent.CompletableFuture$UniExceptionally.tryFire(CompletableFuture.java:970) ~[?:?]
        at java.util.concurrent.CompletableFuture.postComplete(CompletableFuture.java:506) ~[?:?]
        at java.util.concurrent.CompletableFuture.completeExceptionally(CompletableFuture.java:2088) ~[?:?]
        at org.apache.flink.util.concurrent.FutureUtils.lambda$retryOperationWithDelay$6(FutureUtils.java:272) ~[flink-dist-1.16.2.jar:1.16.2]
        at java.util.concurrent.CompletableFuture.uniWhenComplete(CompletableFuture.java:859) ~[?:?]
        at java.util.concurrent.CompletableFuture$UniWhenComplete.tryFire(CompletableFuture.java:837) ~[?:?]
        at java.util.concurrent.CompletableFuture.postComplete(CompletableFuture.java:506) ~[?:?]
        at java.util.concurrent.CompletableFuture.completeExceptionally(CompletableFuture.java:2088) ~[?:?]
        at org.apache.flink.util.concurrent.FutureUtils$Timeout.run(FutureUtils.java:1126) ~[flink-dist-1.16.2.jar:1.16.2]
        at org.apache.flink.util.concurrent.DirectExecutorService.execute(DirectExecutorService.java:217) ~[flink-dist-1.16.2.jar:1.16.2]
        at org.apache.flink.util.concurrent.FutureUtils.lambda$orTimeout$12(FutureUtils.java:490) ~[flink-dist-1.16.2.jar:1.16.2]
        at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:515) ~[?:?]
        at java.util.concurrent.FutureTask.run(FutureTask.java:264) ~[?:?]
        at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:304) ~[?:?]
        at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1128) ~[?:?]
        at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:628) ~[?:?]
        at java.lang.Thread.run(Thread.java:834) ~[?:?]
Caused by: java.util.concurrent.TimeoutException
        at org.apache.flink.util.concurrent.FutureUtils$Timeout.run(FutureUtils.java:1126) ~[flink-dist-1.16.2.jar:1.16.2]
        at org.apache.flink.util.concurrent.DirectExecutorService.execute(DirectExecutorService.java:217) ~[flink-dist-1.16.2.jar:1.16.2]
        at org.apache.flink.util.concurrent.FutureUtils.lambda$orTimeout$12(FutureUtils.java:490) ~[flink-dist-1.16.2.jar:1.16.2]
        at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:515) ~[?:?]
        at java.util.concurrent.FutureTask.run(FutureTask.java:264) ~[?:?]
        at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:304) ~[?:?]
        at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1128) ~[?:?]
        at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:628) ~[?:?]
        at java.lang.Thread.run(Thread.java:834) ~[?:?]
```

### 正常日志
```
2024-06-06 12:16:13,082 INFO  org.apache.flink.client.program.rest.RestClusterClient       [] - Submitting job 'collect' (ee916be916ff9bc7213c23900b85ddb5).
2024-06-06 12:16:13,088 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Sending request of class class org.apache.flink.runtime.rest.messages.job.JobSubmitRequestBody to aws-hk-yall-dev-bigdb-dt-lake09:20911/v1/jobs
2024-06-06 12:16:13,143 DEBUG org.apache.flink.shaded.netty4.io.netty.util.ResourceLeakDetector [] - -Dorg.apache.flink.shaded.netty4.io.netty.leakDetection.level: simple
2024-06-06 12:16:13,143 DEBUG org.apache.flink.shaded.netty4.io.netty.util.ResourceLeakDetector [] - -Dorg.apache.flink.shaded.netty4.io.netty.leakDetection.targetRecords: 4
2024-06-06 12:16:13,151 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.AbstractByteBuf [] - -Dorg.apache.flink.shaded.netty4.io.netty.buffer.checkAccessible: true
2024-06-06 12:16:13,151 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.AbstractByteBuf [] - -Dorg.apache.flink.shaded.netty4.io.netty.buffer.checkBounds: true
2024-06-06 12:16:13,151 DEBUG org.apache.flink.shaded.netty4.io.netty.util.ResourceLeakDetectorFactory [] - Loaded default ResourceLeakDetector: org.apache.flink.shaded.netty4.io.netty.util.ResourceLeakDetector@713c4e07
2024-06-06 12:16:13,175 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PooledByteBufAllocator [] - -Dio.netty.allocator.numHeapArenas: 32
2024-06-06 12:16:13,175 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PooledByteBufAllocator [] - -Dio.netty.allocator.numDirectArenas: 32
2024-06-06 12:16:13,175 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PooledByteBufAllocator [] - -Dio.netty.allocator.pageSize: 8192
2024-06-06 12:16:13,175 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PooledByteBufAllocator [] - -Dio.netty.allocator.maxOrder: 11
2024-06-06 12:16:13,175 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PooledByteBufAllocator [] - -Dio.netty.allocator.chunkSize: 16777216
2024-06-06 12:16:13,175 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PooledByteBufAllocator [] - -Dio.netty.allocator.smallCacheSize: 256
2024-06-06 12:16:13,175 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PooledByteBufAllocator [] - -Dio.netty.allocator.normalCacheSize: 64
2024-06-06 12:16:13,175 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PooledByteBufAllocator [] - -Dio.netty.allocator.maxCachedBufferCapacity: 32768
2024-06-06 12:16:13,175 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PooledByteBufAllocator [] - -Dio.netty.allocator.cacheTrimInterval: 8192
2024-06-06 12:16:13,175 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PooledByteBufAllocator [] - -Dio.netty.allocator.cacheTrimIntervalMillis: 0
2024-06-06 12:16:13,175 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PooledByteBufAllocator [] - -Dio.netty.allocator.useCacheForAllThreads: true
2024-06-06 12:16:13,175 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PooledByteBufAllocator [] - -Dio.netty.allocator.maxCachedByteBuffersPerChunk: 1023
2024-06-06 12:16:13,184 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.ByteBufUtil   [] - -Dio.netty.allocator.type: pooled
2024-06-06 12:16:13,184 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.ByteBufUtil   [] - -Dio.netty.threadLocalDirectBufferSize: 0
2024-06-06 12:16:13,184 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.ByteBufUtil   [] - -Dio.netty.maxThreadLocalCharBufferSize: 16384
2024-06-06 12:16:13,195 DEBUG org.apache.flink.shaded.netty4.io.netty.channel.DefaultChannelId [] - -Dio.netty.processId: 22510 (auto-detected)
2024-06-06 12:16:13,197 DEBUG org.apache.flink.shaded.netty4.io.netty.util.NetUtil         [] - -Djava.net.preferIPv4Stack: false
2024-06-06 12:16:13,198 DEBUG org.apache.flink.shaded.netty4.io.netty.util.NetUtil         [] - -Djava.net.preferIPv6Addresses: false
2024-06-06 12:16:13,200 DEBUG org.apache.flink.shaded.netty4.io.netty.util.NetUtilInitializations [] - Loopback interface: lo (lo, 127.0.0.1)
2024-06-06 12:16:13,201 DEBUG org.apache.flink.shaded.netty4.io.netty.util.NetUtil         [] - /proc/sys/net/core/somaxconn: 65535
2024-06-06 12:16:13,201 DEBUG org.apache.flink.shaded.netty4.io.netty.channel.DefaultChannelId [] - -Dio.netty.machineId: 0a:78:e9:ff:fe:79:de:a5 (auto-detected)
2024-06-06 12:16:13,253 DEBUG org.apache.flink.shaded.netty4.io.netty.util.Recycler        [] - -Dio.netty.recycler.maxCapacityPerThread: 4096
2024-06-06 12:16:13,253 DEBUG org.apache.flink.shaded.netty4.io.netty.util.Recycler        [] - -Dio.netty.recycler.maxSharedCapacityFactor: 2
2024-06-06 12:16:13,253 DEBUG org.apache.flink.shaded.netty4.io.netty.util.Recycler        [] - -Dio.netty.recycler.linkCapacity: 16
2024-06-06 12:16:13,253 DEBUG org.apache.flink.shaded.netty4.io.netty.util.Recycler        [] - -Dio.netty.recycler.ratio: 8
2024-06-06 12:16:13,253 DEBUG org.apache.flink.shaded.netty4.io.netty.util.Recycler        [] - -Dio.netty.recycler.delayedQueue.ratio: 8
2024-06-06 12:16:13,819 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Received response {"jobUrl":"/jobs/ee916be916ff9bc7213c23900b85ddb5"}.
2024-06-06 12:16:13,852 INFO  org.apache.flink.client.program.rest.RestClusterClient       [] - Successfully submitted job 'collect' (ee916be916ff9bc7213c23900b85ddb5) to 'http://aws-hk-yall-dev-bigdb-dt-lake09:20911'.
2024-06-06 12:16:13,853 DEBUG org.apache.flink.client.ClientUtils                          [] - Wait until job initialization is finished
2024-06-06 12:16:13,855 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Sending request of class class org.apache.flink.runtime.rest.messages.EmptyRequestBody to aws-hk-yall-dev-bigdb-dt-lake09:20911/v1/jobs/ee916be916ff9bc7213c23900b85ddb5/status
2024-06-06 12:16:13,862 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Received response {"status":"RUNNING"}.
2024-06-06 12:16:13,870 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Shutting down rest endpoint.
2024-06-06 12:16:13,870 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PoolThreadCache [] - Freed 19 thread-local buffer(s) from thread: flink-rest-client-netty-thread-1
2024-06-06 12:16:13,871 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Rest endpoint shutdown complete.
2024-06-06 12:16:13,882 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Rest client endpoint started.
2024-06-06 12:16:13,882 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Sending request of class class org.apache.flink.runtime.rest.messages.EmptyRequestBody to aws-hk-yall-dev-bigdb-dt-lake09:20911/v1/jobs/ee916be916ff9bc7213c23900b85ddb5/status
2024-06-06 12:16:13,890 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Received response {"status":"RUNNING"}.
2024-06-06 12:16:13,898 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Shutting down rest endpoint.
2024-06-06 12:16:13,898 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PoolThreadCache [] - Freed 2 thread-local buffer(s) from thread: flink-rest-client-netty-thread-1
2024-06-06 12:16:13,899 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Rest endpoint shutdown complete.
2024-06-06 12:16:13,902 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Rest client endpoint started.
2024-06-06 12:16:13,904 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Sending request of class class org.apache.flink.runtime.rest.messages.job.coordination.ClientCoordinationRequestBody to aws-hk-yall-dev-bigdb-dt-lake09:20911/v1/jobs/ee916be916ff9bc7213c23900b85ddb5/coordinators/3d05135cf7d8f1375d8f655ba9d20255
2024-06-06 12:16:13,920 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Received response {"serializedCoordinationResult":"rO0ABXNyAExvcmcuYXBhY2hlLmZsaW5rLnN0cmVhbWluZy5hcGkub3BlcmF0b3JzLmNvbGxlY3QuQ29sbGVjdENvb3JkaW5hdGlvblJlc3BvbnNlAAAAAAAAAAECAANKABZsYXN0Q2hlY2twb2ludGVkT2Zmc2V0TAARc2VyaWFsaXplZFJlc3VsdHN0ABBMamF2YS91dGlsL0xpc3Q7TAAHdmVyc2lvbnQAEkxqYXZhL2xhbmcvU3RyaW5nO3hw//////////9zcgAfamF2YS51dGlsLkNvbGxlY3Rpb25zJEVtcHR5TGlzdHq4F7Q8p57eAgAAeHB0AAA="}.
2024-06-06 12:16:13,925 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Shutting down rest endpoint.
2024-06-06 12:16:13,926 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PoolThreadCache [] - Freed 3 thread-local buffer(s) from thread: flink-rest-client-netty-thread-1
2024-06-06 12:16:13,926 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Rest endpoint shutdown complete.
2024-06-06 12:16:14,027 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Rest client endpoint started.
2024-06-06 12:16:14,028 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Sending request of class class org.apache.flink.runtime.rest.messages.EmptyRequestBody to aws-hk-yall-dev-bigdb-dt-lake09:20911/v1/jobs/ee916be916ff9bc7213c23900b85ddb5/status
2024-06-06 12:16:14,032 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Received response {"status":"RUNNING"}.
2024-06-06 12:16:14,032 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Shutting down rest endpoint.
2024-06-06 12:16:14,032 DEBUG org.apache.flink.shaded.netty4.io.netty.buffer.PoolThreadCache [] - Freed 2 thread-local buffer(s) from thread: flink-rest-client-netty-thread-1
2024-06-06 12:16:14,033 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Rest endpoint shutdown complete.
2024-06-06 12:16:14,034 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Rest client endpoint started.
```

### 异常日志
```
2024-06-06 12:04:48,932 INFO  org.apache.flink.client.program.rest.RestClusterClient       [] - Submitting job 'collect' (f44a2df6d7b16a9409b99a4aa96a195d).
2024-06-06 12:04:48,933 DEBUG org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ClientCnxn [] - Reading reply sessionid:0x1040cf1841106bb, packet:: clientPath:null serverPath:null finished:false header:: 3,3  replyHeader:: 3,12946904338,0  request:: '/flink,F  response:: s{4294967429,4294967429,1698068981763,1698068981763,0,3007,0,0,0,387,12946696435} 
2024-06-06 12:04:48,934 DEBUG org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ClientCnxn [] - Reading reply sessionid:0x1040cf1841106bb, packet:: clientPath:null serverPath:null finished:false header:: 4,3  replyHeader:: 4,12946904338,-101  request:: '/flink/application_1714822662859_0551,F  response::  
2024-06-06 12:04:48,935 DEBUG org.apache.flink.shaded.curator5.org.apache.curator.framework.imps.EnsembleTracker [] - Invalid config event received: {server.2=10.80.130.10:2888:3888:participant, server.1=10.80.130.9:2888:3888:participant, server.3=10.80.130.11:2888:3888:participant, version=0}
2024-06-06 12:04:48,935 INFO  org.apache.flink.shaded.curator5.org.apache.curator.framework.imps.EnsembleTracker [] - New config event received: {server.2=10.80.130.10:2888:3888:participant, server.1=10.80.130.9:2888:3888:participant, server.3=10.80.130.11:2888:3888:participant, version=0}
2024-06-06 12:04:48,935 DEBUG org.apache.flink.shaded.curator5.org.apache.curator.framework.imps.EnsembleTracker [] - Invalid config event received: {server.2=10.80.130.10:2888:3888:participant, server.1=10.80.130.9:2888:3888:participant, server.3=10.80.130.11:2888:3888:participant, version=0}
2024-06-06 12:04:48,937 DEBUG org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ClientCnxn [] - Reading reply sessionid:0x1040cf1841106bb, packet:: clientPath:null serverPath:null finished:false header:: 5,19  replyHeader:: 5,12946904339,0  request:: '/flink/application_1714822662859_0551,,v{s{31,s{'world,'anyone}}},4  response:: '/flink/application_1714822662859_0551 
2024-06-06 12:04:48,938 DEBUG org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ClientCnxn [] - Reading reply sessionid:0x1040cf1841106bb, packet:: clientPath:/flink/application_1714822662859_0551/leader/rest_server/connection_info serverPath:/flink/application_1714822662859_0551/leader/rest_server/connection_info finished:false header:: 6,4  replyHeader:: 6,12946904339,-101  request:: '/flink/application_1714822662859_0551/leader/rest_server/connection_info,T  response::  
2024-06-06 12:04:48,939 DEBUG org.apache.flink.shaded.curator5.org.apache.curator.framework.recipes.cache.TreeCache [] - processResult: CuratorEventImpl{type=GET_DATA, resultCode=-101, path='/leader/rest_server/connection_info', name='null', children=null, context=null, stat=null, data=null, watchedEvent=null, aclList=null, opResults=null}
2024-06-06 12:04:48,940 DEBUG org.apache.flink.shaded.curator5.org.apache.curator.framework.recipes.cache.TreeCache [] - publishEvent: TreeCacheEvent{type=INITIALIZED, data=null}
2024-06-06 12:04:48,940 DEBUG org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ClientCnxn [] - Reading reply sessionid:0x1040cf1841106bb, packet:: clientPath:/flink/application_1714822662859_0551/leader/rest_server/connection_info serverPath:/flink/application_1714822662859_0551/leader/rest_server/connection_info finished:false header:: 7,3  replyHeader:: 7,12946904339,-101  request:: '/flink/application_1714822662859_0551/leader/rest_server/connection_info,T  response::  
2024-06-06 12:04:48,941 DEBUG org.apache.flink.shaded.curator5.org.apache.curator.framework.recipes.cache.TreeCache [] - processResult: CuratorEventImpl{type=EXISTS, resultCode=-101, path='/leader/rest_server/connection_info', name='null', children=null, context=null, stat=null, data=null, watchedEvent=null, aclList=null, opResults=null}
2024-06-06 12:05:08,960 DEBUG org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ClientCnxn [] - Got ping response for sessionid: 0x1040cf1841106bb after 0ms
2024-06-06 12:05:18,940 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Shutting down rest endpoint.
2024-06-06 12:05:18,943 DEBUG org.apache.flink.runtime.rest.RestClient                     [] - Rest endpoint shutdown complete.
2024-06-06 12:05:18,943 INFO  org.apache.flink.runtime.leaderretrieval.DefaultLeaderRetrievalService [] - Stopping DefaultLeaderRetrievalService.
2024-06-06 12:05:18,943 INFO  org.apache.flink.runtime.leaderretrieval.ZooKeeperLeaderRetrievalDriver [] - Closing ZookeeperLeaderRetrievalDriver{connectionInformationPath='/leader/rest_server/connection_info'}.
2024-06-06 12:05:18,945 DEBUG org.apache.flink.shaded.curator5.org.apache.curator.framework.imps.WatcherRemovalManager [] - Removing watcher for path: /flink/application_1714822662859_0551/leader/rest_server/connection_info
2024-06-06 12:05:18,946 DEBUG org.apache.flink.shaded.curator5.org.apache.curator.framework.imps.CuratorFrameworkImpl [] - Closing
2024-06-06 12:05:18,947 INFO  org.apache.flink.shaded.curator5.org.apache.curator.framework.imps.CuratorFrameworkImpl [] - backgroundOperationsLoop exiting
2024-06-06 12:05:18,947 DEBUG org.apache.flink.shaded.curator5.org.apache.curator.framework.imps.WatcherRemovalManager [] - Removing watcher for path: /zookeeper/config
2024-06-06 12:05:18,947 DEBUG org.apache.flink.shaded.curator5.org.apache.curator.CuratorZookeeperClient [] - Closing, waitForShutdownTimeoutMs 0
2024-06-06 12:05:18,947 DEBUG org.apache.flink.shaded.curator5.org.apache.curator.ConnectionState [] - Closing
2024-06-06 12:05:18,947 DEBUG org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ClientCnxn [] - Reading reply sessionid:0x1040cf1841106bb, packet:: clientPath:/flink/application_1714822662859_0551/leader/rest_server/connection_info serverPath:/flink/application_1714822662859_0551/leader/rest_server/connection_info finished:false header:: 8,17  replyHeader:: 8,12946904486,0  request:: '/flink/application_1714822662859_0551/leader/rest_server/connection_info,3  response:: null
2024-06-06 12:05:18,947 DEBUG org.apache.flink.shaded.curator5.org.apache.curator.framework.recipes.cache.TreeCache [] - process: WatchedEvent state:SyncConnected type:DataWatchRemoved path:/leader/rest_server/connection_info
2024-06-06 12:05:18,947 DEBUG org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ClientCnxn [] - Reading reply sessionid:0x1040cf1841106bb, packet:: clientPath:/zookeeper/config serverPath:/zookeeper/config finished:false header:: 9,17  replyHeader:: 9,12946904486,0  request:: '/zookeeper/config,3  response:: null
2024-06-06 12:05:18,948 DEBUG org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ZooKeeper [] - Closing session: 0x1040cf1841106bb
2024-06-06 12:05:18,948 DEBUG org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ClientCnxn [] - Closing client for session: 0x1040cf1841106bb
2024-06-06 12:05:18,949 DEBUG org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ClientCnxn [] - Reading reply sessionid:0x1040cf1841106bb, packet:: clientPath:null serverPath:null finished:false header:: 10,-11  replyHeader:: 10,12946904487,0  request:: null response:: null
2024-06-06 12:05:18,949 DEBUG org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ClientCnxn [] - Disconnecting client for session: 0x1040cf1841106bb
2024-06-06 12:05:18,949 DEBUG org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ClientCnxn [] - An exception was thrown while closing send thread for session 0x1040cf1841106bb : Unable to read additional data from server sessionid 0x1040cf1841106bb, likely server has closed socket
2024-06-06 12:05:19,050 INFO  org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ZooKeeper [] - Session: 0x1040cf1841106bb closed
2024-06-06 12:05:19,050 INFO  org.apache.flink.shaded.zookeeper3.org.apache.zookeeper.ClientCnxn [] - EventThread shut down for session: 0x1040cf1841106bb
2024-06-06 12:05:19,051 WARN  org.apache.flink.table.client.cli.CliClient                  [] - Could not execute SQL statement.
org.apache.flink.table.client.gateway.SqlExecutionException: Could not execute SQL statement.
        at org.apache.flink.table.client.gateway.local.LocalExecutor.executeOperation(LocalExecutor.java:208) ~[flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.gateway.local.LocalExecutor.executeQuery(LocalExecutor.java:228) ~[flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.cli.CliClient.callSelect(CliClient.java:542) ~[flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.cli.CliClient.callOperation(CliClient.java:446) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.cli.CliClient.executeOperation(CliClient.java:372) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.cli.CliClient.getAndExecuteStatements(CliClient.java:329) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.cli.CliClient.executeInteractive(CliClient.java:280) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.cli.CliClient.executeInInteractiveMode(CliClient.java:228) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.SqlClient.openCli(SqlClient.java:151) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.SqlClient.start(SqlClient.java:95) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.SqlClient.startClient(SqlClient.java:187) [flink-sql-client-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.SqlClient.main(SqlClient.java:161) [flink-sql-client-1.16.2.jar:1.16.2]
Caused by: org.apache.flink.table.api.TableException: Failed to execute sql
        at org.apache.flink.table.api.internal.TableEnvironmentImpl.executeQueryOperation(TableEnvironmentImpl.java:903) ~[flink-table-api-java-uber-1.16.2.jar:1.16.2]
        at org.apache.flink.table.api.internal.TableEnvironmentImpl.executeInternal(TableEnvironmentImpl.java:1382) ~[flink-table-api-java-uber-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.gateway.local.LocalExecutor.executeOperation(LocalExecutor.java:206) ~[flink-sql-client-1.16.2.jar:1.16.2]
        ... 11 more
Caused by: org.apache.flink.util.FlinkException: Failed to execute job 'collect'.
        at org.apache.flink.streaming.api.environment.StreamExecutionEnvironment.executeAsync(StreamExecutionEnvironment.java:2203) ~[flink-dist-1.16.2.jar:1.16.2]
        at org.apache.flink.table.planner.delegation.DefaultExecutor.executeAsync(DefaultExecutor.java:95) ~[flink-table-planner_2.12-1.16.2.jar:1.16.2]
        at org.apache.flink.table.api.internal.TableEnvironmentImpl.executeQueryOperation(TableEnvironmentImpl.java:884) ~[flink-table-api-java-uber-1.16.2.jar:1.16.2]
        at org.apache.flink.table.api.internal.TableEnvironmentImpl.executeInternal(TableEnvironmentImpl.java:1382) ~[flink-table-api-java-uber-1.16.2.jar:1.16.2]
        at org.apache.flink.table.client.gateway.local.LocalExecutor.executeOperation(LocalExecutor.java:206) ~[flink-sql-client-1.16.2.jar:1.16.2]
        ... 11 more
Caused by: org.apache.flink.runtime.client.JobSubmissionException: Failed to submit JobGraph.
        at org.apache.flink.client.program.rest.RestClusterClient.lambda$submitJob$11(RestClusterClient.java:448) ~[flink-dist-1.16.2.jar:1.16.2]
        at java.util.concurrent.CompletableFuture.uniExceptionally(CompletableFuture.java:986) ~[?:?]
        at java.util.concurrent.CompletableFuture$UniExceptionally.tryFire(CompletableFuture.java:970) ~[?:?]
        at java.util.concurrent.CompletableFuture.postComplete(CompletableFuture.java:506) ~[?:?]
        at java.util.concurrent.CompletableFuture.completeExceptionally(CompletableFuture.java:2088) ~[?:?]
        at org.apache.flink.util.concurrent.FutureUtils.lambda$retryOperationWithDelay$6(FutureUtils.java:272) ~[flink-dist-1.16.2.jar:1.16.2]
        at java.util.concurrent.CompletableFuture.uniWhenComplete(CompletableFuture.java:859) ~[?:?]
        at java.util.concurrent.CompletableFuture$UniWhenComplete.tryFire(CompletableFuture.java:837) ~[?:?]
        at java.util.concurrent.CompletableFuture.postComplete(CompletableFuture.java:506) ~[?:?]
        at java.util.concurrent.CompletableFuture.completeExceptionally(CompletableFuture.java:2088) ~[?:?]
        at org.apache.flink.util.concurrent.FutureUtils$Timeout.run(FutureUtils.java:1126) ~[flink-dist-1.16.2.jar:1.16.2]
        at org.apache.flink.util.concurrent.DirectExecutorService.execute(DirectExecutorService.java:217) ~[flink-dist-1.16.2.jar:1.16.2]
        at org.apache.flink.util.concurrent.FutureUtils.lambda$orTimeout$12(FutureUtils.java:490) ~[flink-dist-1.16.2.jar:1.16.2]
        at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:515) ~[?:?]
        at java.util.concurrent.FutureTask.run(FutureTask.java:264) ~[?:?]
        at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:304) ~[?:?]
        at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1128) ~[?:?]
        at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:628) ~[?:?]
        at java.lang.Thread.run(Thread.java:834) ~[?:?]
Caused by: java.util.concurrent.TimeoutException
        at org.apache.flink.util.concurrent.FutureUtils$Timeout.run(FutureUtils.java:1126) ~[flink-dist-1.16.2.jar:1.16.2]
        at org.apache.flink.util.concurrent.DirectExecutorService.execute(DirectExecutorService.java:217) ~[flink-dist-1.16.2.jar:1.16.2]
        at org.apache.flink.util.concurrent.FutureUtils.lambda$orTimeout$12(FutureUtils.java:490) ~[flink-dist-1.16.2.jar:1.16.2]
        at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:515) ~[?:?]
        at java.util.concurrent.FutureTask.run(FutureTask.java:264) ~[?:?]
        at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:304) ~[?:?]
        at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1128) ~[?:?]
        at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:628) ~[?:?]
        at java.lang.Thread.run(Thread.java:834) ~[?:?]
```
