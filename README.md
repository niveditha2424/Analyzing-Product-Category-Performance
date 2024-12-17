# Analyzing Product Category Performance with Rolling Average

## Overview
This SQL query combines two analytical approaches to provide insights into product category performance over a specified period. It calculates a rolling average of daily transaction amounts and aggregates total orders and revenue for each product category. This README.md file explains the use case, query description, and provides setup instructions.

## Use Case
In retail analytics, understanding both short-term transaction trends and overall category sales performance is crucial for strategic decision-making. This combined query helps identify categories with consistent sales performance and assess recent changes in transaction patterns.

## SQL Query Description
The SQL query consists of two main parts:
1. **Rolling Average Calculation**: Utilizes historical transaction data (`transactions` table) to compute a rolling average (`rol_avg`) of daily transaction amounts over a dynamic three-day window.
   
2. **Category Performance Summary**: Aggregates total orders (`total_orders`) and revenue (`total_revenue`) for each product category over the last three months using the `orders`, `order_items`, `products`, and `categories` tables.

The results are joined based on `transaction_date`, providing a consolidated view of daily transaction trends alongside category-specific sales metrics.

## SQL Setup Instructions
To run the SQL query:
1. Ensure you have access to a relational database management system (RDBMS) such as PostgreSQL, MySQL, or SQLite.
2. Execute the provided SQL script in your database environment.
3. Adjust the `WHERE` clause in the query to specify the desired date range for analysis (`DATE_SUB(CURDATE(), INTERVAL 3 MONTH)` to `CURDATE()`).
4. Review the output to gain insights into product category performance with a focus on revenue trends and transaction volumes.
