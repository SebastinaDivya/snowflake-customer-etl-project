# ❄️ Snowflake Customer Data ETL Pipeline

## 📌 Project Overview

This is a hands-on mini project built using Snowflake SQL to demonstrate a basic Customer Data ETL pipeline.

The project focuses on loading raw customer data, applying SQL transformations, and performing data quality checks using a layered architecture.

## 🏗️ Architecture

```text
RETAIL_DB
│
├── RAW
│   └── CUSTOMER_RAW
│
├── STAGING
│   └── CUSTOMER_STG
│
└── ANALYTICS
```

## 🛠️ Technologies Used

- Snowflake
- SQL
- Virtual Warehouse
- CTAS (Create Table As Select)
- Data Quality Validation

## 🚀 Implementation Steps

### 1. Database and Warehouse Setup
- Created database: `RETAIL_DB`
- Created schemas: `RAW`, `STAGING`, `ANALYTICS`
- Configured virtual warehouse: `RETAIL_WH`
- Set warehouse size to XSMALL with auto-suspend and auto-resume.

### 2. Raw Data Loading
- Created `CUSTOMER_RAW` table.
- Inserted five sample customer records.

### 3. Data Transformation
- Created `CUSTOMER_STG` using CTAS.
- Used `TRIM()` to remove unwanted spaces.
- Used `UPPER()` to standardize city names.
- Filtered records with missing customer IDs and names.

### 4. Data Quality Checks
- Checked NULL values.
- Identified duplicate customer IDs using `GROUP BY` and `HAVING`.
- Validated total and unique customer counts.

## 📂 SQL Scripts

The SQL scripts are organized in the `sql` directory:

1. Database and warehouse setup
2. Raw customer table creation and loading
3. Staging transformations
4. Data quality checks

## 📚 Key Learnings

- Snowflake database and schema management
- Virtual warehouse configuration
- Layered data architecture
- SQL-based ETL transformations
- Data quality validation

## 🔮 Future Enhancements

- Duplicate record removal using `ROW_NUMBER()`
- Build the ANALYTICS layer
- Add customer and sales reporting
- Extend the pipeline with additional datasets

---

**Project:** Snowflake Customer Data ETL Pipeline  
**Learning Journey:** Snowflake From Scratch – Mini Project 1
