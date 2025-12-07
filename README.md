# 🚀 Distributed Data Processing with Apache Spark on Databricks

This project implements an end-to-end **distributed data processing pipeline** using **Apache Spark** running on **Azure Databricks**, with data ingestion from **Azure Data Lake Storage (ADLS)**.  
It demonstrates a realistic workflow for building scalable data engineering solutions based on the Spark DataFrame API.

---

## Overview

The notebook included in this repository showcases how to:

- Ingest structured data from ADLS using `abfss://` paths  
- Configure secure access to Data Lake resources  
- Process and transform large datasets using optimized, chained Spark transformations  
- Apply data quality checks and validation logic  
- Build reproducible and scalable pipelines executed on a Databricks Spark cluster  

The implementation follows clean and professional Spark coding practices, using immutable transformations and avoiding unnecessary intermediate variables.

---

## Key Features

### Data Ingestion
Reads input data stored in Azure Data Lake Storage (ADLS Gen2) using:

```python
spark.read.format("csv") \
     .option("header", "true") \
     .option("inferSchema", "true") \
     .load("abfss://<container>@<storageaccount>.dfs.core.windows.net/<path>")

spark-distributed-processing/
│
├── notebooks/
│   └── spark_processing.ipynb     # Main Databricks/Spark notebook
│
├── README.md                      # Project documentation
└── requirements.txt (optional)

