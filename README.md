# Data_Pipeline_ETL-Data-Engineering-with-Python-and-SQLite

This repository contains a hands-on data engineering lab focused on developing a lightweight ETL (Extract, Transform, Load) pipeline using Python and SQLite. The assignment required ingesting structured CSV files, transforming the data using Python and Pandas, and loading it into a normalized SQLite database. Finally, SQL queries were used to analyze and validate the transformed dataset.

---

### 🧩 Business Problem

Businesses often deal with fragmented datasets from different sources, requiring structured transformation pipelines for integration and analysis. This lab emulates that real-world challenge by requiring the student to build a basic ETL pipeline from CSV files into a queryable SQL database using Python—illustrating key principles of data engineering.

---

### 📦 Dataset Overview

Three CSV files were used:
- `products.csv`: Contains product details such as product ID, name, and manufacturer.
- `orders.csv`: Contains transactional order data with timestamps and customer/product references.
- `customers.csv`: Contains demographic and contact information about customers.

The goal was to clean and join these datasets into a relational schema suitable for business intelligence queries.

---

### 🎯 Project Objectives

- Read and explore raw CSV datasets
- Create SQLite tables with appropriate normalization
- Use Python and SQL to load data into tables while managing foreign key relationships
- Execute analytical queries for business insights (e.g., most purchased products, revenue by region)
- Understand tradeoffs between denormalized and normalized designs

---

### 🛠️ Solution Approach

1. **Data Exploration & Cleaning**
   - Inspected CSV files using Pandas
   - Detected and resolved missing or inconsistent values
   - Normalized string formats and removed special characters

2. **ETL Pipeline Development**
   - Used `sqlite3` to create and manage an embedded SQLite database
   - Created tables with proper keys (e.g., `CustomerID`, `OrderID`, `ProductID`)
   - Loaded each dataset into its respective table using `executemany()` from Pandas DataFrames

3. **Data Integrity & Foreign Keys**
   - Applied primary and foreign key constraints in SQLite
   - Ensured referential integrity between customer, order, and product tables

4. **SQL Analysis**
   - Queried total sales and product popularity
   - Explored customer order behavior
   - Performed joins to answer business-relevant questions like revenue by customer segment

---

### 💡 Business Value

This project simulates a real-world data engineering use-case and provides:
- A modular ETL system that can be scaled or automated for larger datasets
- A normalized database ready for BI tools and advanced analytics
- Better data governance and quality through structured loading and transformation

---

### 🚧 Challenges Encountered

- Dealing with null or malformed rows in the source files
- Ensuring clean type conversions before database insertion
- Validating referential integrity during data loads

---

