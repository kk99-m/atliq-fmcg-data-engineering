# atliq-fmcg-data-engineering

## 📌 Project Overview

This project demonstrates the design and implementation of an end-to-end data engineering pipeline using the Databricks Lakehouse Platform.
The solution ingests raw sales data stored in Amazon S3, processes it through the Medallion Architecture (Bronze → Silver → Gold), and delivers analytics-ready datasets that power an interactive business dashboard.
The project follows industry-standard data engineering practices including historical loading, incremental loading, orchestration, dimensional modeling, and dashboard development.

# 🏢 Business Problem

AtliQ is a growing FMCG company that generates sales data across multiple business channels, customers, products, and regions.
Business teams require reliable, timely, and centralized reporting to answer questions such as:

 Which products generate the highest revenue?
 Which customers contribute the most sales?
 How does revenue change over time?
 Which sales channels perform best?
 What trends help support strategic business decisions?

Raw operational data alone cannot answer these questions efficiently.

The objective was to build a scalable data platform capable of transforming raw transactional data into analytics-ready datasets for reporting and decision-making.

# 🎯 Objectives

Build an end-to-end ETL pipeline using Databricks
Implement Medallion Architecture
Process historical and incremental data
Create optimized Gold Layer reporting tables
Develop an interactive dashboard for business users

#  Data Engineering Workflow

## 1️⃣ Data Ingestion

Uploaded source datasets into Amazon S3
Connected Databricks with S3 using External Location
Imported raw datasets into Bronze Layer

## 2️⃣ Bronze Layer

The Bronze Layer stores raw data exactly as received.

Tasks performed:

Raw CSV ingestion
Schema definition
Delta table creation

## 3️⃣ Silver Layer

The Silver Layer transforms raw data into clean, reliable datasets.

Transformations include:

Data cleaning
Duplicate removal
Null handling
Data type corrections
Dimension table processing
Business transformations

## 4️⃣ Gold Layer

The Gold Layer contains business-ready datasets optimized for reporting.

Implemented:

Fact tables
Dimension tables
Denormalized reporting views
Sales metrics

## 5️⃣ Historical Load

Performed an initial full load of historical sales data into the Gold Layer.

This establishes the baseline dataset for reporting.

## 6️⃣ Incremental Load

Implemented incremental processing to load only newly arrived records.

Benefits include:

Faster processing
Reduced compute cost
Better scalability

## 7️⃣ Pipeline Orchestration

Built an automated workflow to execute the pipeline in the correct order:

Bronze
Silver
Gold
Dashboard Refresh
