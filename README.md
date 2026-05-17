# Noon Food Delivery SQL Analysis (PostgreSQL)

## Project Overview

This project analyzes a food delivery dataset inspired by Noon Food using PostgreSQL.

The goal of this project is to answer business questions related to:

- Restaurant performance
- Customer acquisition
- Promo code effectiveness
- Customer retention and churn
- Organic vs promo-based growth

The project demonstrates practical SQL skills used by data analysts and business analysts.

---

## Dataset Schema

The analysis uses a single table named `orders`.

| Column Name | Description |
|-----------|-----------|
| order_id | Unique identifier for each order |
| customer_code | Unique identifier for each customer |
| placed_at | Timestamp when the order was placed |
| restaurant_id | Unique restaurant identifier |
| cuisine | Cuisine category |
| order_status | Delivery status |
| promo_code_name | Promo code applied (NULL if no promo used) |

---

## SQL Concepts Used

- Common Table Expressions (CTEs)
- Window Functions (`ROW_NUMBER()`)
- Aggregate Functions (`COUNT`, `MIN`, `MAX`)
- Conditional Aggregation
- Date Functions (`EXTRACT`, `INTERVAL`, `CURRENT_DATE`)
- Joins
- Subqueries

---

## Business Questions Solved

### 1. Top 3 Restaurants by Cuisine Type
Ranked the top three restaurants within each cuisine based on order count.

### 2. Daily New Customer Acquisition
Calculated the number of customers placing their first order on each day.

### 3. January 2025 One-Time Customers
Identified customers acquired in January 2025 who placed exactly one order and had no orders outside January.

### 4. Inactive Customers Acquired More Than One Month Ago
Found customers whose latest order was more than 7 days ago and whose first order was at least one month ago, along with the promo used in their first order.

### 5. Every Third Order Trigger
Generated the 3rd, 6th, 9th, etc. order for each customer to support lifecycle messaging.

### 6. Customers Using Promo on Every Order
Listed customers with multiple orders where every order used a promo code.

### 7. Percentage of Organically Acquired Customers (January 2025)
Calculated the percentage of customers whose first order in January 2025 was placed without a promo code.

---

## Key Insights

- Promo codes significantly contribute to customer acquisition.
- Some customers become inactive shortly after their first purchase.
- Organic acquisition remains an important source of growth.
- Customers who repeatedly use promo codes may be discount dependent.
- Triggering campaigns after every third order can improve retention.
- Restaurant performance varies substantially within each cuisine category.

---

## Project Structure

```text
noon-food-delivery-sql-analysis/
│── README.md
│── schema.sql
│── sample_data.sql
│── analysis_queries.sql
│── insights.md
