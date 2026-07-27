# atliq-fmcg-data-engineering

## 📌 Project Overview

This project demonstrates the implementation of a scalable data engineering pipeline using the Databricks Lakehouse Platform.

Raw business data is ingested from Amazon S3, processed through the Bronze, Silver, and Gold layers using Lakeflow Declarative Pipelines, and served to business users through interactive dashboards and Databricks Genie.

The solution follows modern data engineering best practices, including layered data architecture, automated data processing, incremental loading, centralized governance with Unity Catalog, and analytics-ready reporting.

# 🏢 Business Problem

As the business grows, data is generated from multiple operational systems and stored in raw CSV files.

Business users require reliable and centralized reporting to answer questions such as:

- Which products generate the highest revenue?
- Which sales channels perform best?
- How is revenue changing over time?
- Which customers contribute the most to overall sales?
- How can leadership make data-driven business decisions?

Manually preparing reports is time-consuming, error-prone, and difficult to scale.

The objective of this project is to build an automated, scalable, and reliable data platform capable of transforming raw operational data into trusted business insights.

---

# 🎯 Objectives

- Build an end-to-end ETL pipeline using Databricks
- Implement the Medallion Architecture
- Automate data ingestion using Lakeflow Pipelines
- Process historical and incremental data loads
- Create analytics-ready Gold tables
- Deliver interactive dashboards for business stakeholders

---

# 🏗️ Solution Architecture

![Architecture](architecture/project_architecture.png)

### Pipeline Flow

```
Amazon S3
      │
      ▼
Lakeflow Declarative Pipelines
      │
      ▼
Bronze Layer (Raw Data)
      │
      ▼
Silver Layer (Cleaned & Transformed Data)
      │
      ▼
Gold Layer (Business Ready Analytics)
      │
      ├────────► Databricks SQL Dashboard
      │
      └────────► Databricks Genie
```

Unity Catalog is used to manage governance, permissions, and metadata across the platform.

---

# ⚙️ Technology Stack

| Category | Technologies |
|-----------|--------------|
| Cloud Storage | Amazon S3 |
| Data Platform | Databricks |
| Processing | PySpark |
| Storage | Delta Lake |
| Governance | Unity Catalog |
| Orchestration | Lakeflow Declarative Pipelines |
| Query Engine | Databricks SQL |
| Reporting | Databricks SQL Dashboard |
| AI Analytics | Databricks Genie |

---

# 🔄 Data Engineering Workflow

## 1. Data Ingestion

Business data is uploaded to Amazon S3.

Lakeflow Declarative Pipelines automatically ingest the source data into the Bronze Layer.

---

## 2. Bronze Layer

The Bronze Layer stores raw source data exactly as received.

Activities include:

- Raw data ingestion
- Schema creation
- Delta table generation
- Historical data preservation

---

## 3. Silver Layer

The Silver Layer prepares data for analytics through transformation and cleansing.

Processing includes:

- Data validation
- Duplicate removal
- Null handling
- Data type standardization
- Business rule implementation

---

## 4. Gold Layer

The Gold Layer contains analytics-ready datasets optimized for reporting and business intelligence.

This layer provides:

- Aggregated metrics
- Reporting tables
- Business KPIs
- Optimized SQL queries

---

## 5. Historical Load

Historical datasets are loaded during the initial pipeline execution to establish a complete reporting foundation.

---

## 6. Incremental Load

After the initial load, only newly arrived or modified records are processed.

Benefits include:

- Faster execution
- Lower compute costs
- Improved scalability
- Efficient production pipelines

---

## 7. Data Serving

Business users access analytics through:

- Databricks SQL Dashboards
- Databricks Genie

These tools enable self-service analytics without requiring direct access to raw datasets.

---

# 📊 Dashboard

The final dashboard provides business insights including:

- Total Revenue
- Monthly Revenue Trends
- Revenue by Sales Channel
- Customer Performance
- Product Performance
- Sales Distribution
- Business KPIs

---

# 🌟 Key Features

- End-to-End ETL Pipeline
- Medallion Architecture
- Amazon S3 Integration
- Delta Lake Storage
- Automated Lakeflow Pipelines
- Unity Catalog Governance
- Historical Data Loading
- Incremental Processing
- Analytics-Ready Gold Layer
- Interactive Business Dashboard
- AI-powered Insights with Databricks Genie

---

# 📚 Key Learnings

Through this project, I gained hands-on experience with:

- Building scalable data pipelines
- Designing Medallion Architecture
- Working with Delta Lake
- Automating ETL workflows
- Implementing historical and incremental loading
- Data modeling for analytics
- Developing business dashboards
- Applying modern Lakehouse architecture principles

---

# 🚀 Future Enhancements

Future improvements include:

- Implement Change Data Capture (CDC)
- Integrate CI/CD pipelines
- Add automated data quality validation
- Deploy streaming pipelines
- Implement monitoring and alerting
- Enhance AI-powered analytics using Databricks Genie

---

