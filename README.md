---

# 📊 SQL Data Exploration & Analytics Project

Welcome to the **SQL Data Exploration & Analytics Repository**! �  
This repository is a comprehensive collection of SQL scripts designed for **data exploration, analytics, and reporting**. Whether you're a data analyst, BI professional, or SQL enthusiast, these scripts will help you quickly explore, segment, and analyze data within a relational database. Each script focuses on a specific analytical theme and demonstrates best practices for SQL queries.

---

## � Table of Contents

1. [Project Overview](#-project-overview)
2. [Key Features](#-key-features)
3. [Script Categories](#-script-categories)
4. [Summary](#-summary)
5. [Acknowledgements](#-acknowledgements)

---

## � Project Overview

This repository is a curated collection of SQL scripts that cover a wide range of data analysis tasks, including:

- **Database Exploration** 🔍  
- **Measures and Metrics** 📏  
- **Time-Based Trends** 📅  
- **Cumulative Analytics** 📈  
- **Segmentation** 🗂️  
- **And More!** 🎯  

These scripts are designed to help you gain insights from your data efficiently and effectively. They are written with clarity and best practices in mind, making them easy to adapt to your own datasets.

---

## 🎯 Key Features

- **Ready-to-Use Scripts**: Each script is self-contained and ready to run on your database.  
- **Modular Design**: Scripts are organized by analytical themes, making it easy to find what you need.  
- **Best Practices**: Demonstrates clean, efficient, and optimized SQL queries.    
- **Documented**: Each script includes comments to explain its purpose and logic.  

---

## 📂 Script Categories

Here’s a breakdown of the SQL scripts available in this repository:

### 1. **Database Exploration** 🔍  
   - Explore database structures, list of tables, schemas and relationships.  
   - inspect the columns and metadata for specific tables.

     <br> *Code example:*
```sql
SELECT
   TABLE_CATALOG, 
   TABLE_SCHEMA, 
   TABLE_NAME, 
   TABLE_TYPE
FROM INFORMATION_SCHEMA.TABLES
ORDER BY TABLE_TYPE;
```
### 2. **Measures and Metrics** 📏  
   - Calculate key performance indicators (KPIs).  
   - Aggregate data using `SUM`, `AVG`, `COUNT`, etc.  

### 3. **Time-Based Trends** 📅  
   - Analyze data over time (daily, weekly, monthly).  
   - Identify seasonality or trends.  

### 4. **Cumulative Analytics** 📈  
   - Calculate running totals and cumulative metrics.  
   - Track progress over time.  

### 5. **Segmentation** 🗂️  
   - Group data into meaningful categories (e.g., customer segments).  
   - Perform cohort analysis.  

### 6. **Advanced Analytics** 🚀  
   - Use window functions, subqueries, and CTEs.  
   - Perform complex joins and transformations.  

---

## 🤝 Summary

This project is logical continuation of my [Data Warehouse Project](https://github.com/Timaxrus/sql-data-warehouse-project) where I tried to demonstrate best practices of ETL. This repository is a comprehensive collection of SQL scripts designed for data exploration, analytics, and reporting demonstrating my data analytics EDA skills. It includes queries for database exploration, measures and metrics, time-based trends, cumulative analytics, and segmentation. Tailored for data analysts and BI professionals, these scripts help quickly explore, segment, and analyze relational database data. Each script focuses on a specific analytical theme and follows SQL best practices.


---

## 📜 License

This project is licensed under the **MIT License**. Feel free to use, modify, and distribute the scripts as needed.  

---

## 🙏 Acknowledgements

- Inspired by [DataWithBaraa](https://github.com/DataWithBaraa).  
- Built with ❤️ for the data community.  

---

Happy Querying! 🚀  

--- 
