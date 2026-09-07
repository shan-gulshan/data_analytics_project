# SQL Data Analytics using SQL Server

## Overview

This project is a comprehensive **SQL Data Analyst Portfolio Project** focused on performing advanced analytics on a structured data warehouse using **SQL Server**.

The project simulates a real-world business environment where customer, product, and sales data are analyzed to generate meaningful business insights. Advanced SQL techniques are used to analyze trends, measure performance, segment customers and products, and build reusable analytical reports.

## Objectives

* Analyze sales trends and business performance over time.
* Perform cumulative and year-over-year analysis.
* Evaluate customer and product performance.
* Calculate important business KPIs.
* Segment customers and products based on business rules.
* Build reusable SQL views for reporting.
* Apply advanced SQL techniques commonly used in Data Analyst roles.

## Dataset & Data Warehouse

The project uses a **Star Schema** consisting of fact and dimension tables.

### Dimension Tables

* **dim_customers** – Contains customer information and attributes.
* **dim_products** – Contains product details, categories, and costs.

### Fact Table

* **fact_sales** – Contains transactional sales data including orders, products, customers, quantities, and sales amounts.

The tables are connected through appropriate keys to enable customer, product, and sales analysis.

## Analytical Phases

### 1. Change Over Time Analysis

Analyzed sales and business measures across different time periods to identify trends and changes in business performance.

**Key analysis:**

* Monthly and yearly sales trends
* Revenue growth
* Changes in customer activity

### 2. Cumulative Analysis

Used window functions to calculate cumulative business metrics and understand overall growth patterns.

**Examples:**

* Running total sales
* Cumulative revenue
* Growth over time

### 3. Performance Analysis

Compared current performance with historical and benchmark values using advanced SQL window functions.

**Techniques used:**

* `LAG()`
* `LEAD()`
* Moving averages
* Year-over-year comparisons
* Product ranking

### 4. Part-to-Whole Analysis

Analyzed how individual products and categories contribute to overall business revenue.

**Examples:**

* Category contribution to total revenue
* Product revenue percentage
* Revenue distribution

### 5. Data Segmentation

Converted quantitative metrics into meaningful business categories using `CASE WHEN`.

**Customer Segmentation:**

* VIP
* Regular
* New

**Product Segmentation:**

* High Revenue
* Medium Revenue
* Low Revenue

## Customer Report

A **360-degree Customer Report** was created to understand customer purchasing behavior and value.

### Key KPIs

* Total Sales
* Total Orders
* Total Quantity
* Average Order Value
* Average Monthly Spend
* Recency
* Customer Lifespan
* Customer Segment

The final customer analysis was implemented as a **SQL View**, making the report reusable for further analysis and business reporting.

## Product Report

A **Product Report** was developed to evaluate product performance and profitability.

### Key Metrics

* Total Sales
* Quantity Sold
* Total Cost
* Total Profit
* Profit Margin
* Average Selling Price
* Product Lifespan
* Revenue Segment

This report helps identify high-performing products and understand their contribution to overall business performance.

## SQL Techniques Used

This project demonstrates practical usage of:

* **CTEs (Common Table Expressions)**
* **Subqueries**
* **Window Functions**
* **Aggregate Functions**
* **CASE Statements**
* **SQL Views**
* **Joins**
* **Date & Time Functions**
* **Ranking Functions**
* **Data Segmentation**

### Example Window Function

```sql
LAG(total_sales) OVER (
    PARTITION BY product_id
    ORDER BY year
)
```

This allows current performance to be compared with the previous period.

## Key Insights

The analysis provides insights into:

* Sales and revenue trends over time.
* High-value and low-value customers.
* Customer purchasing behavior and recency.
* Top-performing and under-performing products.
* Revenue contribution by product categories.
* Product profitability and performance.
* Customer and product segments that can support business decisions.

## Project Structure

```text
SQL-Data-Warehouse-Analytics/
│
├── datasets/
│   ├── dim_customers.csv
│   ├── dim_products.csv
│   └── fact_sales.csv
│
├── scripts/
│   ├── change_over_time.sql
│   ├── cumulative_analysis.sql
│   ├── performance_analysis.sql
│   ├── part_to_whole_analysis.sql
│   ├── data_segmentation.sql
│   ├── customer_report.sql
│   └── product_report.sql
│
├── logo.png
└── README.md
```

## Skills Demonstrated

* SQL Server & T-SQL
* Advanced SQL Analytics
* Data Warehousing
* Star Schema
* Fact & Dimension Tables
* Business KPI Development
* Customer Segmentation
* Product Performance Analysis
* Data Analysis
* Git & GitHub

## Conclusion

This project demonstrates how **SQL Server and advanced SQL techniques** can be used to transform transactional data into meaningful business insights.

Through customer analysis, product performance evaluation, trend analysis, segmentation, and KPI development, the project provides a practical example of how a **Data Analyst can use SQL to support business decision-making**.

## Author

**Gulshan kumar**

This project is part of my **Data Analyst portfolio**, showcasing my skills in SQL, data analysis, data warehousing, and business problem-solving.

⭐ If you find this project useful, consider giving the repository a star!
