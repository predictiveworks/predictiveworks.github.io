---
layout: default
title: Purpose-built Connectors
---
# Purpose-built Connectors

Google [CDAP](https://cdap.io) offers many connector plugins to integrate with data stores, streaming platforms and cloud applications.

Predictive<span class="brand-teal">Works.</span> complements CDAP's built-in data connectors with plugins that originate from specific enterprise demands, referring to a certain business area or vertical.

## [Aerospike](https://www.aerospike.com/) Plugins

<table>
    <colgroup>
      <col width="20%">
      <col width="80%">
    </colgroup>
    <tr>
      <td>
        <img style="margin:20px" src="/assets/images/aerospike.png" width="120">
      </td>
      <td>
        <b>Aerospike</b>
        <p>
        A Next-Generation NoSQL Data Platform for real-time solutions at extreme scale, with predictable performance at any scale and unmatched uptime and reliability.     
        </p>
        <b>Use Cases</b>
        <p>
        Advertising, Cyber Defense, Internet-of-Things
        </p>
      </td>
    </tr>
</table>

### Aerospike as Source

```java
@Plugin(type = BatchSource.PLUGIN_TYPE)
@Name("AerospikeSource")
@Description("A batch connector plugin to read data records from Aerospike namespaces and "
      + "sets and transform into structured pipeline records.")
public class AerospikeSource extends BatchSource<AerospikeKey, AerospikeRecord, StructuredRecord> {

    ...

}      
```

### Aerospike as Sink

```java
@Plugin(type = BatchSink.PLUGIN_TYPE)
@Name("AerospikeSink")
@Description("A batch connector plugin to write structured pipelines records to "
      + "Aerospike namespaces and sets.")
public class AerospikeSink extends BatchSink<StructuredRecord, AerospikeKey, AerospikeRecord> {

    ...

}
```

## [Crate](https://crate.io) Plugins

<table>
    <colgroup>
      <col width="20%">
      <col width="80%">
    </colgroup>
    <tr>
      <td>
        <img style="margin:20px" src="/assets/images/crate.png" width="120">
      </td>
      <td>
        <b>Crate DB</b>
        <p>
        Crate is a distributed SQL database at IoT-scale built on top of a NoSQL foundation. It combines the familiarity of SQL with the scalability and data flexibility of NoSQL.   
        </p>
        <b>Use Cases</b>
        <p>
        Cyber Defense, Internet-of-Things
        </p>
      </td>
    </tr>
</table>

### Crate as Source

```java
@Plugin(type = BatchSource.PLUGIN_TYPE)
@Name("CrateSource")
@Description("A batch connector plugin to read data rows from Crate tables "
      + "and transform into structured pipeline records.")
public class CrateSource extends BatchSource<NullWritable, CrateWritable, StructuredRecord> {

    ...

}      
```

### Crate as Sink

```java
@Plugin(type = BatchSink.PLUGIN_TYPE)
@Name("CrateSink")
@Description("A batch connector plugin to write structured pipelines records to "
      + "Crate tables.")
public class CrateSink extends BatchSink<StructuredRecord, NullWritable, CrateWritable> {

    ...

}
```
