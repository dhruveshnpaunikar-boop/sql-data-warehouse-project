# sql-data-warehouse-project
Building a modern data warehouse using SQL Server, including ETL processes, data modeling, and analytics.

# Data Warehouse and Analytics Project

Welcome to the **Data Warehouse and Analytics Project** repository! 🚀  
This project demonstrates a comprehensive data warehousing and analytics solution,
from building a data warehouse to generating actionable insights. Designed as a 
portfolio project, it highlights industry best practices in data engineering and analytics.

---

## 🚀 Project Requirements

### Building the Data Warehouse (Data Engineering)

**Objective**

Develop a modern data warehouse using SQL Server to consolidate sales data, enabling
analytical reporting and informed decision-making.

**Specifications**

- **Data Sources**: Import data from two source systems (ERP and CRM) provided as CSV files.
- **Data Quality**: Cleanse and resolve data quality issues prior to analysis.
- **Integration**: Combine both sources into a single, user-friendly data model designed
  for analytical queries.
- **Scope**: Focus on the latest dataset only; historization of data is not required.
- **Documentation**: Provide clear documentation of the data model to support both
  business stakeholders and analytics teams.

---

### BI: Analytics & Reporting (Data Analytics)

**Objective**

Develop SQL-based analytics to deliver detailed insights into:

- **Customer Behavior**
- **Product Performance**
- **Sales Trends**

These insights empower stakeholders with key business metrics, enabling strategic
decision-making.

---

## 🏗️ Architecture Overview

This project follows the **Medallion Architecture** (Bronze → Silver → Gold):
```
Sources (CSV files)
    ├── Bronze Layer  →  Raw data, loaded as-is (Tables)
    ├── Silver Layer  →  Cleaned & standardized data (Tables)
    └── Gold Layer    →  Business-ready data (Views)
```

| Layer  | Object Type | Load Method              | Transformations                          |
|--------|-------------|--------------------------|------------------------------------------|
| Bronze | Tables      | Batch / Truncate & Insert | None (as-is)                            |
| Silver | Tables      | Batch / Truncate & Insert | Cleansing, Normalization, Enrichment    |
| Gold   | Views       | None                      | Aggregations, Business Logic, Integration|

---

## 🗂️ Repository Structure
```
/
├── datasets/          # Raw source CSV files (ERP & CRM)
├── bronze/            # Scripts for raw data ingestion
├── silver/            # Transformation & cleansing scripts
├── gold/              # View definitions & business logic
├── analytics/         # SQL-based analytics & reporting queries
├── docs/              # Data model documentation & diagrams
└── README.md
```

---

## 🛠️ Tools & Technologies

- **Database**: Microsoft SQL Server
- **Language**: T-SQL
- **Source Data**: CSV files (ERP & CRM systems)
- **BI / Reporting**: SQL-based analytics queries

---

## 📋 Project Status

🚧 In Progress

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).  
You are free to use, modify, and share this project with proper attribution.
