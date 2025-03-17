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

This repository is a curated collection of SQL scripts that cover a wide range of data analysis tasks

### Part 1 - Data Exploration (EDA):

- **Database Exploration** 🔍  
- **Dimensions Exploration** 📏  
- **Date Exploration** 📅  
- **Measures Exploration** 📈  
- **Magnitude and Ranking** 🗂️  
- **And More!** 🎯  

### Part 2 - Data Analysis (Advanced):

- **Change-over-time Trends** 📈
- **Cumulativ Analysis** 📊
- **Performance Analysis** ⚖️

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

### Data Exploration Queries:

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
### 2. **Dimensions Exploration** 📏  
   - Explore the structure of dimension tables.  
   - Inspect the range of unique dimensions.
     
     <br> *Code example:*
```sql
SELECT DISTINCT 
    category, 
    subcategory, 
    product_name 
FROM gold.dim_products
ORDER BY category, subcategory, product_name;
```

### 3. **Date Exploration** 📅  
   - Determine the temporal boundaries of key data points.
   - Understand the range of historical data.

     <br> *Code example:*
```sql
SELECT 
    MIN(order_date) AS first_order_date,
    MAX(order_date) AS last_order_date,
    DATEDIFF(MONTH, MIN(order_date), MAX(order_date)) AS order_range_months
FROM gold.fact_sales;
```

### 4. **Measures Exploration** 📈  
   - Calculate aggregated metrics (e.g., totals, averages, sum) for quick insights.  
   - Generate a Report that shows all key metrics of the business.

     <br> *Code example:*
```sql
SELECT 'Total Sales' AS measure_name, SUM(sales_amount) AS measure_value FROM gold.fact_sales
UNION ALL
SELECT 'Total Quantity', SUM(quantity) FROM gold.fact_sales
UNION ALL
SELECT 'Average Price', AVG(price) FROM gold.fact_sales
UNION ALL
SELECT 'Total Orders', COUNT(DISTINCT order_number) FROM gold.fact_sales
UNION ALL
SELECT 'Total Products', COUNT(DISTINCT product_name) FROM gold.dim_products
UNION ALL
SELECT 'Total Customers', COUNT(customer_key) FROM gold.dim_customers;
```

### 5. **Magnitude and Ranking** 🗂️  
   - Quantify data and group results by specific dimensions.
   - Understanding data distribution across categories.

     <br> *Code example:*
```sql
SELECT
    p.category,
    SUM(f.sales_amount) AS total_revenue
FROM gold.fact_sales f
LEFT JOIN gold.dim_products p
    ON p.product_key = f.product_key
GROUP BY p.category
ORDER BY total_revenue DESC;
```

### 6. **Advanced Ranking Analytics** 🚀  
   - Rank items (e.g., products, customers) based on performance or other metrics.
   - Identify top performers or laggards.

     <br> *Code example:*
```sql
SELECT TOP 5
    p.product_name,
    SUM(f.sales_amount) AS total_revenue
FROM gold.fact_sales f
LEFT JOIN gold.dim_products p
    ON p.product_key = f.product_key
GROUP BY p.product_name
ORDER BY total_revenue;
```

### Data Exploration Queries:


### 1. **Change-over-time Trends** 📈


- **Cumulativ Analysis** 📊
- **Performance Analysis** ⚖️

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
