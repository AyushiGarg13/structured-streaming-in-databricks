# Structured Streaming in Databricks

> Short tutorial for Streaming in Databricks

This project describes how structured streaming works in Databricks meanwhile making contrast with the traditional batch processing methods. The basics of windowing operations are also seen through this.

## Introduction

Structured streaming API of Spark is built upon the Spark SQL Engine. Before these, we had DStream APIs which were based on **RDDs**. RDDs being the unstructured APIs of spark, had drawbacks in regard with establishing complete optimization of code.

Structured streaming APIs leverage the benefits of Structured APIs `Dataframes/Datasets` and enhance user experience by unifying them with older APIs as well. Due to the structured nature of data, optimizations can be performed to full extent in these APIs.

## Usage

The notebooks for this project are created using the [Community Edition](https://community.cloud.databricks.com) of databricks.

- The only requirement to run the notebooks is setting up a cluster.
- The default configuration for the cluster is as follows: 

```
Databricks Runtime Version          7.3 LTS (includes Apache Spark 3.0.1, Scala 2.12)
Driver Type                         Community Optimized; 15.3 GB Memory, 2 Cores, 1 DBU
```

Sample data is provided by Spark. 

`%fs ls /databricks-datasets/structured-streaming/events/`

Overview of the windowing operations are seen through the notebooks. The 2 basic windowing operations are:

1. Tumbling Window
2. Sliding Window
