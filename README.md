# centralized-log-management
## Overview
Enterprise solution for Centralized Logging that will allow organization to capture applications' log in single place in cost effective and secure way.

## Design Considerations
* Ability to query application logs when needed.
* Provide longer retention of logs in reliable and highly available (HA) as persistent storage.
* Ability to handle high volume logs with low latency,
* Scalable

## Architecture
CLM is a collection of various technologies in order to provide reliable, highly available and secure Enterprise Solution.
Logs will be ingested using **Logstash**. Log is then moved to **Elasticsearch** and **Kafka**. **Elasticsearch** will be use for data indexing.

Once data is available in **Elasticsearch**, logs can be view by visualisation tool **Kibana**.

Logs can be published to **Kafka** and consumed by **Apache Flume** where log *aggregation* can be applied.

**Apache Flume** will store logs to **Hadoop** for longer retention period and can be consumed by **Elasticsearch**



![CLM](https://github.com/ehfajkhan/centralized-log-management/blob/master/clm-1.0.png)



