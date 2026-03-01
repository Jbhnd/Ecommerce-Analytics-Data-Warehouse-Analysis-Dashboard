# Ecommerce-Analytics-Data-Warehouse-Analysis-Dashboard
### Project Overview

This project demonstrates the design and implementation of an end-to-end ecommerce analytics solution, including data modeling, transformation, and business intelligence reporting.

Raw transactional CSV datasets were transformed into a dimensional star schema using Python and SQLite. Analytical queries were developed to evaluate revenue performance, customer behavior, and operational efficiency. Results were visualized in a Tableau dashboard designed for business stakeholders.

---

## 🎯 Business Objectives

The analysis focuses on answering the following business questions:

* What are the key drivers of revenue growth?
* How does revenue trend month-over-month?
* Which product categories contribute most to total revenue?
* What is the order cancellation rate and how does it vary by region?
* Who are the highest-value customers?

---

## 🏗️ Data Architecture

The project implements a **star schema** data model with the following structure:

### Fact Tables

* `fact_order_items`
* `fact_payments`
* `fact_reviews`

### Dimension Tables

* `dim_orders`
* `dim_customers`
* `dim_products`
* `dim_date`

Granularity of the main fact table is defined at the **order-item level**, enabling detailed revenue and product-level analysis.

Indexes were added on foreign keys to optimize join performance.

(star_schema_diagram.png)

---

## ⚙️ Technology Stack

* **Python** (Pandas, datetime, hashlib, logging)
* **SQLite** (dimensional modeling, indexing)
* **SQL** (analytical queries)
* **Tableau** (dashboard development)

---

## 🔄 Data Processing Workflow

1. Load raw CSV datasets
2. Perform exploratory data analysis (EDA)
3. Clean and standardize data
4. Handle null values and parse timestamps
5. Define fact table granularity
6. Generate surrogate keys
7. Create dimensional schema in SQLite
8. Load fact and dimension tables
9. Develop analytical SQL queries
10. Export curated dataset for Tableau

---

## 📈 Key KPIs

The Tableau dashboard tracks:

* **Total Revenue**
* **Average Revenue per Order**
* **Total Number of Orders**
* **Order Cancellation Rate**

---

## Key Insights

* **Revenue Growth:** Revenue increased **22% MoM in November**, driven primarily by Electronics and Home categories.
* **Order Cancellations:** Cancellation rate is **2.4x higher for orders delivered after the shipping limit date**, highlighting operational bottlenecks.
* **Customer Concentration:** Top 10% of customers account for ~35% of total revenue, suggesting high-value retention opportunities.
* **Product Category Performance:** Products in the "Unknown" category have higher return rates and lower review scores, indicating potential product data quality issues.
* **Top Performers:** Electronics and Fashion categories consistently drive the highest revenue per order and repeat purchases.

---

## Tableau Dashboard Features

* **Monthly Revenue Trend** with MoM growth
* **Revenue by Product Category**
* **Top Products & Top Customers**
* **Order Cancellation Analysis** by state and city
* **Interactive filters** for date, customer state, and city

*(Include `tableau_dashboard_screenshot.png` here)*

---

## Skills Demonstrated

* Dimensional data modeling
* Data transformation and cleaning using Python
* SQL analytics
* KPI definition and metric governance
* SQL query development for analytical KPIs
* Business intelligence and dashboard design in Tableau
* End-to-end analytics workflow ownership, from raw data to actionable insights

---

#### Opportunities for Further Enhancement

* Implement cohort retention and customer lifetime value analysis
* Analyze delivery performance impact on review scores and cancellations
* Migrate warehouse to a cloud database for scalability
* Orchestrate pipeline using Airflow or dbt for automation

---
