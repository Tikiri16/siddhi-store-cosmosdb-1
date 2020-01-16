# API Docs - v2.0.2-SNAPSHOT

## Store

### cosmosdb *<a target="_blank" href="http://siddhi.io/documentation/siddhi-5.x/query-guide-5.x/#store">(Store)</a>*

<p style="word-wrap: break-word">Using this extension a CosmosDB Event Table can be configured to persist events in a CosmosDB of user's choice.</p>

<span id="syntax" class="md-typeset" style="display: block; font-weight: bold;">Syntax</span>
```
@Store(type="cosmosdb", cosmosdb.uri="<STRING>", collection.name="<STRING>", secure.connection="<STRING>", trust.store="<STRING>", trust.store.password="<STRING>", key.store="<STRING>", key.store.password="<STRING>")
@PrimaryKey("PRIMARY_KEY")
@Index("INDEX")
```

<span id="query-parameters" class="md-typeset" style="display: block; color: rgba(0, 0, 0, 0.54); font-size: 12.8px; font-weight: bold;">QUERY PARAMETERS</span>
<table>
    <tr>
        <th>Name</th>
        <th style="min-width: 20em">Description</th>
        <th>Default Value</th>
        <th>Possible Data Types</th>
        <th>Optional</th>
        <th>Dynamic</th>
    </tr>
    <tr>
        <td style="vertical-align: top">cosmosdb.uri</td>
        <td style="vertical-align: top; word-wrap: break-word">The CosmosDB URI for the CosmosDB data store. The uri must be of the format <br>cosmosdb://[username:password@]host1[:port1][,hostN[:portN]][/[database][?options]]<br>The options specified in the uri will override any connection options specified in the deployment yaml file.</td>
        <td style="vertical-align: top"></td>
        <td style="vertical-align: top">STRING</td>
        <td style="vertical-align: top">No</td>
        <td style="vertical-align: top">No</td>
    </tr>
    <tr>
        <td style="vertical-align: top">collection.name</td>
        <td style="vertical-align: top; word-wrap: break-word">The name of the collection in the store this Event Table should be persisted as.</td>
        <td style="vertical-align: top">Name of the siddhi event table.</td>
        <td style="vertical-align: top">STRING</td>
        <td style="vertical-align: top">Yes</td>
        <td style="vertical-align: top">No</td>
    </tr>
    <tr>
        <td style="vertical-align: top">secure.connection</td>
        <td style="vertical-align: top; word-wrap: break-word">Describes enabling the SSL for the cosmosdb connection</td>
        <td style="vertical-align: top">false</td>
        <td style="vertical-align: top">STRING</td>
        <td style="vertical-align: top">Yes</td>
        <td style="vertical-align: top">No</td>
    </tr>
    <tr>
        <td style="vertical-align: top">trust.store</td>
        <td style="vertical-align: top; word-wrap: break-word">File path to the trust store.</td>
        <td style="vertical-align: top">${carbon.home}/resources/security/client-truststore.jks</td>
        <td style="vertical-align: top">STRING</td>
        <td style="vertical-align: top">Yes</td>
        <td style="vertical-align: top">No</td>
    </tr>
    <tr>
        <td style="vertical-align: top">trust.store.password</td>
        <td style="vertical-align: top; word-wrap: break-word">Password to access the trust store</td>
        <td style="vertical-align: top">wso2carbon</td>
        <td style="vertical-align: top">STRING</td>
        <td style="vertical-align: top">Yes</td>
        <td style="vertical-align: top">No</td>
    </tr>
    <tr>
        <td style="vertical-align: top">key.store</td>
        <td style="vertical-align: top; word-wrap: break-word">File path to the keystore.</td>
        <td style="vertical-align: top">${carbon.home}/resources/security/client-truststore.jks</td>
        <td style="vertical-align: top">STRING</td>
        <td style="vertical-align: top">Yes</td>
        <td style="vertical-align: top">No</td>
    </tr>
    <tr>
        <td style="vertical-align: top">key.store.password</td>
        <td style="vertical-align: top; word-wrap: break-word">Password to access the keystore</td>
        <td style="vertical-align: top">wso2carbon</td>
        <td style="vertical-align: top">STRING</td>
        <td style="vertical-align: top">Yes</td>
        <td style="vertical-align: top">No</td>
    </tr>
</table>

<span id="system-parameters" class="md-typeset" style="display: block; font-weight: bold;">System Parameters</span>
<table>
    <tr>
        <th>Name</th>
        <th style="min-width: 20em">Description</th>
        <th>Default Value</th>
        <th>Possible Parameters</th>
    </tr>
    <tr>
        <td style="vertical-align: top">applicationName</td>
        <td style="vertical-align: top; word-wrap: break-word">Sets the logical name of the application using this CosmosClient. The application name may be used by the client to identify the application to the server, for use in server logs, slow query logs, and profile collection.</td>
        <td style="vertical-align: top">null</td>
        <td style="vertical-align: top">the logical name of the application using this CosmosClient. The UTF-8 encoding may not exceed 128 bytes.</td>
    </tr>
    <tr>
        <td style="vertical-align: top">cursorFinalizerEnabled</td>
        <td style="vertical-align: top; word-wrap: break-word">Sets whether cursor finalizers are enabled.</td>
        <td style="vertical-align: top">true</td>
        <td style="vertical-align: top">true<br>false</td>
    </tr>
    <tr>
        <td style="vertical-align: top">requiredReplicaSetName</td>
        <td style="vertical-align: top; word-wrap: break-word">The name of the replica set</td>
        <td style="vertical-align: top">null</td>
        <td style="vertical-align: top">the logical name of the replica set</td>
    </tr>
    <tr>
        <td style="vertical-align: top">sslEnabled</td>
        <td style="vertical-align: top; word-wrap: break-word">Sets whether to initiate connection with TSL/SSL enabled. true: Initiate the connection with TLS/SSL. false: Initiate the connection without TLS/SSL.</td>
        <td style="vertical-align: top">false</td>
        <td style="vertical-align: top">true<br>false</td>
    </tr>
    <tr>
        <td style="vertical-align: top">trustStore</td>
        <td style="vertical-align: top; word-wrap: break-word">File path to the trust store.</td>
        <td style="vertical-align: top">${carbon.home}/resources/security/client-truststore.jks</td>
        <td style="vertical-align: top">Any valid file path.</td>
    </tr>
    <tr>
        <td style="vertical-align: top">trustStorePassword</td>
        <td style="vertical-align: top; word-wrap: break-word">Password to access the trust store</td>
        <td style="vertical-align: top">wso2carbon</td>
        <td style="vertical-align: top">Any valid password.</td>
    </tr>
    <tr>
        <td style="vertical-align: top">keyStore</td>
        <td style="vertical-align: top; word-wrap: break-word">File path to the keystore.</td>
        <td style="vertical-align: top">${carbon.home}/resources/security/client-truststore.jks</td>
        <td style="vertical-align: top">Any valid file path.</td>
    </tr>
    <tr>
        <td style="vertical-align: top">keyStorePassword</td>
        <td style="vertical-align: top; word-wrap: break-word">Password to access the keystore</td>
        <td style="vertical-align: top">wso2carbon</td>
        <td style="vertical-align: top">Any valid password.</td>
    </tr>
    <tr>
        <td style="vertical-align: top">connectTimeout</td>
        <td style="vertical-align: top; word-wrap: break-word">The time in milliseconds to attempt a connection before timing out.</td>
        <td style="vertical-align: top">10000</td>
        <td style="vertical-align: top">Any positive integer</td>
    </tr>
    <tr>
        <td style="vertical-align: top">connectionsPerHost</td>
        <td style="vertical-align: top; word-wrap: break-word">The maximum number of connections in the connection pool.</td>
        <td style="vertical-align: top">100</td>
        <td style="vertical-align: top">Any positive integer</td>
    </tr>
    <tr>
        <td style="vertical-align: top">minConnectionsPerHost</td>
        <td style="vertical-align: top; word-wrap: break-word">The minimum number of connections in the connection pool.</td>
        <td style="vertical-align: top">0</td>
        <td style="vertical-align: top">Any natural number</td>
    </tr>
    <tr>
        <td style="vertical-align: top">maxConnectionIdleTime</td>
        <td style="vertical-align: top; word-wrap: break-word">The maximum number of milliseconds that a connection can remain idle in the pool before being removed and closed. A zero value indicates no limit to the idle time.  A pooled connection that has exceeded its idle time will be closed and replaced when necessary by a new connection.</td>
        <td style="vertical-align: top">0</td>
        <td style="vertical-align: top">Any positive integer</td>
    </tr>
    <tr>
        <td style="vertical-align: top">maxWaitTime</td>
        <td style="vertical-align: top; word-wrap: break-word">The maximum wait time in milliseconds that a thread may wait for a connection to become available. A value of 0 means that it will not wait.  A negative value means to wait indefinitely</td>
        <td style="vertical-align: top">120000</td>
        <td style="vertical-align: top">Any integer</td>
    </tr>
    <tr>
        <td style="vertical-align: top">threadsAllowedToBlockForConnectionMultiplier</td>
        <td style="vertical-align: top; word-wrap: break-word">The maximum number of connections allowed per host for this CosmosClient instance. Those connections will be kept in a pool when idle. Once the pool is exhausted, any operation requiring a connection will block waiting for an available connection.</td>
        <td style="vertical-align: top">100</td>
        <td style="vertical-align: top">Any natural number</td>
    </tr>
    <tr>
        <td style="vertical-align: top">maxConnectionLifeTime</td>
        <td style="vertical-align: top; word-wrap: break-word">The maximum life time of a pooled connection.  A zero value indicates no limit to the life time.  A pooled connection that has exceeded its life time will be closed and replaced when necessary by a new connection.</td>
        <td style="vertical-align: top">0</td>
        <td style="vertical-align: top">Any positive integer</td>
    </tr>
    <tr>
        <td style="vertical-align: top">socketKeepAlive</td>
        <td style="vertical-align: top; word-wrap: break-word">Sets whether to keep a connection alive through firewalls</td>
        <td style="vertical-align: top">false</td>
        <td style="vertical-align: top">true<br>false</td>
    </tr>
    <tr>
        <td style="vertical-align: top">socketTimeout</td>
        <td style="vertical-align: top; word-wrap: break-word">The time in milliseconds to attempt a send or receive on a socket before the attempt times out. Default 0 means never to timeout.</td>
        <td style="vertical-align: top">0</td>
        <td style="vertical-align: top">Any natural integer</td>
    </tr>
    <tr>
        <td style="vertical-align: top">writeConcern</td>
        <td style="vertical-align: top; word-wrap: break-word">The write concern to use.</td>
        <td style="vertical-align: top">acknowledged</td>
        <td style="vertical-align: top">acknowledged<br>w1<br>w2<br>w3<br>unacknowledged<br>fsynced<br>journaled<br>replica_acknowledged<br>normal<br>safe<br>majority<br>fsync_safe<br>journal_safe<br>replicas_safe</td>
    </tr>
    <tr>
        <td style="vertical-align: top">readConcern</td>
        <td style="vertical-align: top; word-wrap: break-word">The level of isolation for the reads from replica sets.</td>
        <td style="vertical-align: top">default</td>
        <td style="vertical-align: top">local<br>majority<br>linearizable</td>
    </tr>
    <tr>
        <td style="vertical-align: top">readPreference</td>
        <td style="vertical-align: top; word-wrap: break-word">Specifies the replica set read preference for the connection.</td>
        <td style="vertical-align: top">primary</td>
        <td style="vertical-align: top">primary<br>secondary<br>secondarypreferred<br>primarypreferred<br>nearest</td>
    </tr>
    <tr>
        <td style="vertical-align: top">localThreshold</td>
        <td style="vertical-align: top; word-wrap: break-word">The size (in milliseconds) of the latency window for selecting among multiple suitable CosmosDB instances.</td>
        <td style="vertical-align: top">15</td>
        <td style="vertical-align: top">Any natural number</td>
    </tr>
    <tr>
        <td style="vertical-align: top">serverSelectionTimeout</td>
        <td style="vertical-align: top; word-wrap: break-word">Specifies how long (in milliseconds) to block for server selection before throwing an exception. A value of 0 means that it will timeout immediately if no server is available.  A negative value means to wait indefinitely.</td>
        <td style="vertical-align: top">30000</td>
        <td style="vertical-align: top">Any integer</td>
    </tr>
    <tr>
        <td style="vertical-align: top">heartbeatSocketTimeout</td>
        <td style="vertical-align: top; word-wrap: break-word">The socket timeout for connections used for the cluster heartbeat. A value of 0 means that it will timeout immediately if no cluster member is available.  A negative value means to wait indefinitely.</td>
        <td style="vertical-align: top">20000</td>
        <td style="vertical-align: top">Any integer</td>
    </tr>
    <tr>
        <td style="vertical-align: top">heartbeatConnectTimeout</td>
        <td style="vertical-align: top; word-wrap: break-word">The connect timeout for connections used for the cluster heartbeat. A value of 0 means that it will timeout immediately if no cluster member is available.  A negative value means to wait indefinitely.</td>
        <td style="vertical-align: top">20000</td>
        <td style="vertical-align: top">Any integer</td>
    </tr>
    <tr>
        <td style="vertical-align: top">heartbeatFrequency</td>
        <td style="vertical-align: top; word-wrap: break-word">Specify the interval (in milliseconds) between checks, counted from the end of the previous check until the beginning of the next one.</td>
        <td style="vertical-align: top">10000</td>
        <td style="vertical-align: top">Any positive integer</td>
    </tr>
    <tr>
        <td style="vertical-align: top">minHeartbeatFrequency</td>
        <td style="vertical-align: top; word-wrap: break-word">Sets the minimum heartbeat frequency.  In the event that the driver has to frequently re-check a server's availability, it will wait at least this long since the previous check to avoid wasted effort.</td>
        <td style="vertical-align: top">500</td>
        <td style="vertical-align: top">Any positive integer</td>
    </tr>
</table>

<span id="examples" class="md-typeset" style="display: block; font-weight: bold;">Examples</span>
<span id="example-1" class="md-typeset" style="display: block; color: rgba(0, 0, 0, 0.54); font-size: 12.8px; font-weight: bold;">EXAMPLE 1</span>
```
@Store(type="cosmosdb",cosmosdb.uri="cosmosdb://admin:admin@localhost/Foo")
@PrimaryKey("symbol")
@IndexBy("volume 1 {background:true,unique:true}")
define table FooTable (symbol string, price float, volume long);
```
<p style="word-wrap: break-word">This will create a collection called FooTable for the events to be saved with symbol as Primary Key(unique index at cosmosd level) and index for the field volume will be created in ascending order with the index option to create the index in the background.<br><br>Note: <br>@PrimaryKey: This specifies a list of comma-separated values to be treated as unique fields in the table. Each record in the table must have a unique combination of values for the fields specified here.<br><br>@IndexBy: This specifies the fields that must be indexed at the database level. You can specify multiple values as a come-separated list. A single value to be in the format,<br>“&lt;FieldName&gt; &lt;SortOrder&gt; &lt;IndexOptions&gt;”<br>&lt;SortOrder&gt; - ( 1) for Ascending and (-1) for Descending<br>&lt;IndexOptions&gt; - Index Options must be defined inside curly brackets. {} to be used for default options. Options must follow the standard cosmosdb index options format. Reference : https://docs.cosmosdb.com/manual/reference/method/db.collection.createIndex/<br>Example : “symbol 1 {“unique”:true}”<br></p>

