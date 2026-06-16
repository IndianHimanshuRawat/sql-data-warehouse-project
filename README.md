# 🏗️ Data Warehouse Project | Medallion Architecture

## 📖 Project Overview

This project demonstrates the design and implementation of a modern Data Warehouse using the **Medallion Architecture (Bronze → Silver → Gold)** in PostgreSQL.

The solution integrates data from multiple source systems (CRM and ERP), applies data quality transformations, and delivers business-ready analytical models for reporting and decision-making.

The project follows industry-standard Data Engineering practices, including ETL development, data cleansing, dimensional modeling, and automated data loading using PL/pgSQL stored procedures.

---

## 🎯 Project Objectives

- Build a scalable Data Warehouse using PostgreSQL.
- Implement Medallion Architecture (Bronze, Silver, Gold).
- Integrate data from CRM and ERP source systems.
- Improve data quality through cleansing and standardization.
- Create analytical models using Star Schema design.
- Automate ETL pipelines using stored procedures.
- Provide a single source of truth for reporting and analytics.

---

## 🏛️ Data Architecture

The project follows the Medallion Architecture pattern:

### Source Systems
- CRM Data
- ERP Data

### Bronze Layer
Stores raw source data without transformations.

**Key Characteristics**
- Raw data ingestion
- Full load processing
- Data stored as received
- Source of truth

### Silver Layer
Stores cleansed and standardized data.

**Transformations**
- Data cleaning
- Duplicate removal
- Data standardization
- Data normalization
- Derived column creation
- Data enrichment

### Gold Layer
Stores business-ready analytical models.

**Features**
- Data integration
- Business logic implementation
- Aggregations
- Star Schema modeling


## 🔄 ETL Pipeline

### Bronze Layer

Raw CSV files are loaded into PostgreSQL Bronze tables using batch processing.

#### Tasks Performed
- Table truncation
- Full data load
- Load monitoring
- Error handling

---

### Silver Layer

Data quality and transformation layer.

#### Data Quality Checks
- Remove duplicate records
- Standardize customer information
- Standardize product information
- Handle missing values
- Validate dates
- Apply business rules

#### Output Tables

##### CRM
- crm_cust_info
- crm_prd_info
- crm_sales_details

##### ERP
- erp_cust_az12
- erp_loc_a101
- erp_px_cat_g1v2

---

### Gold Layer

Business-ready analytical layer.

#### Dimension Models

##### dim_customers
Contains customer information enriched from CRM and ERP systems.

##### dim_products
Contains product information and category details.

#### Fact Models

##### fact_sales
Contains transactional sales information and business metrics.

---

## 📊 Data Model

The Gold Layer follows a Star Schema design.

### Fact Table

#### fact_sales

Stores sales transactions and measures:

- Customer Key
- Product Key
- Order Number
- Sales Amount
- Quantity Sold

### Dimension Tables

#### dim_customers

Attributes include:

- Customer ID
- Customer Name
- Gender
- Marital Status
- Country

#### dim_products

Attributes include:

- Product ID
- Product Name
- Product Category
- Product Line
- Product Cost

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|----------|
| PostgreSQL | Data Warehouse |
| SQL | Data Transformation |
| PL/pgSQL | Stored Procedures |

---

## ✨ Key Features

- Medallion Architecture Implementation
- End-to-End ETL Pipeline
- Automated Data Loading
- Data Quality Validation
- Data Cleansing & Standardization
- Star Schema Design
- Fact & Dimension Modeling
- Logging and Execution Monitoring
- Business-Ready Analytics Layer

---

## 📈 Skills Demonstrated

### Data Engineering
- Data Warehousing
- ETL Development
- Data Modeling
- Data Integration

### SQL Development
- Advanced SQL
- Window Functions
- CTEs
- Stored Procedures
- Exception Handling

### Database Management
- PostgreSQL
- Schema Design
- Query Optimization
- Data Quality Management

---

## 🚀 Future Enhancements

- Incremental Loading Strategy
- Audit and Logging Framework
- Change Data Capture (CDC)
- Data Quality Dashboard
- Power BI Dashboard Integration
- Cloud Deployment (AWS / Azure)

---

## 📚 Key Learnings

Through this project, I gained hands-on experience in:

- Designing a Data Warehouse from scratch
- Implementing Medallion Architecture
- Building ETL pipelines using PostgreSQL
- Creating Star Schema data models
- Applying data quality and transformation rules
- Automating data processing using PL/pgSQL

---

## 👨‍💻 Author

**Himanshu Rawat**

Aspiring Data Analyst |

- LinkedIn: *linkedin.com/in/himanshu-rawat-0396423a2*

---
