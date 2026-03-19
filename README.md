# Ecommerce Analytics and BI Dashboard
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

[Ecommerce Star Schema Diagram](./star_schema_diagram.png)

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

* **Revenue:** November had the highest revenue driven by products in Watches_Gifts, Bed_bath_table, and Health_beauty categories.
* **Order Cancellations:** One state(SP) makes up over 50% (52.31%) of total cancelled orders.
* **Customer Concentration:** Customer concentration is limited, with Top 10 customers accounting for <1% total revenue.
* **Product Category Performance:** Health_beauty, Watches_Gifts and Bed_Bath are highest revenue categories across all states.
* **Customer Retention:** Avg order per customer is 1, indicating opportunities for improvement in customer retention.

---

## Tableau Dashboard Features

* **Monthly Revenue Trend** with MoM growth
* **Revenue by Product Category**
* **Top Products & Top Customers**
* **Order Cancellation Analysis** by state and city
* **Interactive filters** for date, customer state, and city

[Ecommerce Dashboard Screenshot](./dashboard/ecommerce_analysis_dashboard.png)

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
