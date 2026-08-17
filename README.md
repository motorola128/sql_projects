# SQL Data Warehouse & Analytics Project

This repository showcases an end-to-end SQL portfolio project built in two parts: a **Data Warehouse project** (data engineering) and a **Data Analytics project** (SQL-based reporting and insights). Together, they simulate a real-world workflow — from raw source data all the way to business-ready insights.

## 🎯 Skills Demonstrated

SQL Development · Data Architecture · ETL Pipeline Development · Data Modeling · Data Analytics & Reporting

## 🛠️ Tools Used

- **SQL Server & SSMS** – database hosting, development, and querying
- **Draw.io** – architecture, data flow, and data model diagrams
- **Git & GitHub** – version control and project management

---

## 📦 Project 1: Data Warehouse (Data Engineering)

### Objective
Build a modern data warehouse in SQL Server that consolidates sales data from two separate source systems (ERP and CRM) into a single, clean, analysis-ready model.

### Architecture
The warehouse follows the **Medallion Architecture**, moving data through three progressively refined layers:

| Layer | Purpose |
|---|---|
| **Bronze** | Raw data ingested as-is from CSV files (ERP & CRM) into SQL Server, with no transformations |
| **Silver** | Data cleansing, standardization, deduplication, and normalization to make the data reliable and consistent |
| **Gold** | Business-ready data modeled into a **star schema** (fact and dimension tables), optimized for reporting and analytical queries |

### What Was Done
- Imported raw ERP and CRM CSV data into the Bronze layer
- Wrote SQL scripts to clean, standardize, and resolve data quality issues in the Silver layer
- Integrated both source systems into one unified data model
- Designed and built fact and dimension tables (star schema) in the Gold layer
- Documented the data model, table naming conventions, and data catalog for future reference
- Focused on the latest snapshot of data (no historical tracking/SCD required, by design)

### Key Scripts
```
scripts/bronze/   # Load raw CSVs into SQL Server
scripts/silver/   # Clean, transform, and standardize data
scripts/gold/     # Build the star schema (views/tables for reporting)
```

---

## 📊 Project 2: Data Analytics (SQL Reporting & Insights)

### Objective
Use the Gold layer of the warehouse to answer real business questions through SQL — turning clean, modeled data into actionable insights.

### What Was Analyzed
- **Customer Behavior** – customer segmentation, purchasing patterns, and activity over time
- **Product Performance** – top/bottom performing products, category-level trends
- **Sales Trends** – revenue trends over time, growth analysis, and period-over-period comparisons

### What Was Done
- Wrote exploratory and advanced SQL queries directly on the star schema
- Built reusable views/reports for key business metrics
- Used window functions, aggregations, CTEs, and joins to derive insights
- Structured queries so they could support dashboards or downstream reporting tools

---
