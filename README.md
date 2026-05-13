# 🍔 Restaurant Operations & Sales Analysis | Big Data Case Study

## 📌 Project Overview
An end-to-end Data Engineering and Business Intelligence project designed to handle over **11 Million+ orders**. The project leverages the **Medallion Architecture** on **Databricks** to process large-scale restaurant data, delivering actionable insights through a high-performance **Power BI** Dashboard.

## 🛠 Tech Stack
* **Data Orchestration & Processing:** Databricks (Spark SQL & PySpark)
* **Storage:** Delta Lake (ACID Transactions, Time Travel)
* **Ingestion:** Fivetran (Managed Connectors) & Google Cloud API
* **Business Intelligence:** Power BI (DirectQuery Mode)
* **Data Source:** 7 CSV Files & 2 JSON Files (Stored on Google Drive)

## 🏗 Data Pipeline Architecture (Medallion)

### 🥉 Bronze Layer (Ingestion)
* Automated ingestion from Google Drive using **Fivetran**.
* Raw data persisted as **Delta Tables** to ensure schema enforcement and reliability.

### 🥈 Silver Layer (Transformation)
* **Standardization:** Uniform data types and schema alignment.
* **Data Cleaning:** Handling Nulls, Outliers, and invalid records.
* **Problem Solving:** Identified and resolved duplication issues using a **Composite Primary Key** `(order_id + source_file)` to maintain data integrity across multi-source files.

### 🥇 Gold Layer (Aggregations)
* Optimized **Star Schema** implementation.
* Aggregated business metrics for high-speed reporting performance.

## 📊 Business Intelligence & Insights
The reporting layer consists of 4 specialized dashboards designed for executive decision-making:

1.  **Executive Summary (نظرة عامة على الأداء):** High-level KPIs including Total Revenue (2.9B EGP), Total Orders (11M), and overall ratings.
2.  **Menu Analysis (تحليل الأصناف):** Deep dive into product performance and category contributions.
3.  **Branch Performance (أداء الفروع):** Geospatial analysis of branches across Egypt.
4.  **Operational Patterns (تحليل أنماط التشغيل):** Time-series analysis for Peak Hours, Peak Days, and payment methods.

## 🚀 Key Features
* **High Performance:** Utilizing Spark's distributed computing to handle 11M+ records without performance degradation.
* **Data Reliability:** Implemented ACID transactions and auditing via Delta Lake.
* **Scalability:** DirectQuery connection ensures real-time scalability from Databricks to Power BI.

## 📁 Repository Structure
```text
├── notebooks/          # Databricks Notebooks (.py/.sql)
├── powerbi/            # Power BI Desktop File (.pbix)
├── assets/             # Dashboard Screenshots & Icons
└── README.md           # Project Documentation
