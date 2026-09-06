# 📘 Fundamentals of Data Engineering

This repository contains notes on the **Fundamentals of Data Engineering**, covering essential concepts, workflows, and tools used in modern data engineering.

---

## 🔹 What is Data Engineering?
Data Engineering is the process of collecting, moving, storing, transforming, and preparing data so it can be reliably used for:
- Analytics
- Business Intelligence
- Reporting
- Machine Learning
- Business decision-making

A Data Engineer builds and maintains the systems and pipelines that make this possible.

---

## 🔹 Basic Data Engineering Flow

---

## 🔹 Data Sources
Common sources include:
- Application Databases
- APIs
- CSV / JSON Files
- SaaS Applications
- Logs
- Streaming Systems (e.g., Kafka, PostgreSQL, MySQL, APIs)

Key questions before designing a pipeline:
- Where is the data coming from?
- What format is it in?
- How much data is generated?
- How frequently does it change?
- How quickly does the business need it?

---

## 🔹 Data Ingestion
Moving data from source systems into the data platform.  
- Can be **periodic (batch)** or **continuous (streaming)** depending on business needs.

---

## 🔹 Batch vs Streaming
**Batch Processing**  
- Data processed at scheduled intervals (hourly, daily, nightly).  
- Suitable for: daily reports, historical processing, ETL pipelines.

**Streaming Processing**  
- Data processed continuously or near real-time.  
- Suitable for: fraud detection, live monitoring, real-time analytics.

---

## 🔹 Full Load vs Incremental Load
- **Full Load**: Process the entire dataset (used for initial loads, small datasets, complete rebuilds).
- **Incremental Load**: Process only new or changed records (identified via timestamps, watermarks, CDC).  
  ✅ Faster, cheaper, scalable.

---

## 🔹 ETL vs ELT
- **ETL (Extract → Transform → Load)**: Transform before loading.  
- **ELT (Extract → Load → Transform)**: Load raw data first, then transform inside the target platform.  
Modern cloud warehouses often prefer **ELT**.

---

## 🔹 Data Lake vs Data Warehouse
- **Data Lake**: Flexible storage for raw/processed data (CSV, JSON, Parquet, Logs). Examples: S3, ADLS, GCS.  
- **Data Warehouse**: Structured, optimized for analytics/reporting. Examples: Snowflake, BigQuery, Redshift.

---

## 🔹 Data Transformation
Transformations include:
- Removing duplicates
- Handling nulls
- Correcting data types
- Standardizing formats
- Joining datasets
- Filtering invalid records
- Aggregations & derived columns

---

## 🔹 Data Quality
Checks ensure reliability:
- Null checks
- Duplicate detection
- Negative values
- File arrival validation
- Source vs target count validation

Poor data quality → incorrect dashboards & decisions.

---

## 🔹 Data Orchestration
Manages pipeline workflows:
- Scheduling
- Dependencies
- Retries
- Failure handling
- Monitoring

**Tools**: Apache Airflow, Azure Data Factory, Databricks Workflows.

---

## 🔹 End-to-End Pipeline Example (E-commerce)
Includes: Data Quality, Orchestration, Monitoring, Security.

---

## 🔹 Common Tools & Their Purpose
| Technology            | Purpose                          |
|------------------------|----------------------------------|
| SQL                   | Querying & transforming data     |
| Python                | Automation, APIs, data processing|
| Apache Spark          | Distributed data processing      |
| Databricks            | Lakehouse workloads              |
| Kafka                 | Event streaming                  |
| Airflow / ADF         | Pipeline orchestration           |
| Snowflake / BigQuery  | Analytical platforms             |
| S3 / ADLS / GCS       | Cloud storage                    |

---

## 🔹 Quick Revision
- **Data Flow**: Source → Ingestion → Storage → Transformation → Serving → Consumption  
- **Batch vs Streaming**: Periodic vs continuous processing  
- **Full vs Incremental**: All data vs only changed data  
- **ETL vs ELT**: Transform before vs after loading  
- **Data Lake vs Warehouse**: Flexible storage vs structured analytics  
- **Data Quality**: Ensure reliability  
- **Orchestration**: Manage scheduling, dependencies, retries, failures  

