# E-Commerce Sales & Customer Insights Dashboard

A SQL-driven analytics project built on the **Olist Brazilian E-Commerce dataset** to study **sales performance, customer behavior, payments, reviews, and delivery operations**.  
The project combines **SQLite + SQL + Python visualization** to turn raw transactional data into concise, business-oriented insights.

---

## Project Overview

This project analyzes **6 interconnected e-commerce datasets** to answer practical business questions around revenue growth, product performance, customer satisfaction, and operational efficiency.

### What this project does
- Built an **SQL-based analysis pipeline** across orders, order items, payments, customers, products, and reviews datasets.
- Analyzed **monthly revenue trends**, **top-performing product categories**, **payment behavior**, and **repeat customer rate**.
- Evaluated **delivery delays by state/region** and **review-score patterns** to uncover customer-experience and logistics issues.
- Transformed raw transaction-level data into **clear business insights** for sales and customer behavior analysis.

---

## Problem Statement

E-commerce businesses generate large amounts of transactional data, but raw tables alone do not reveal:
- Which product categories drive the most revenue
- How customer satisfaction relates to sales
- Whether delivery delays are hurting customer experience
- How often customers come back and purchase again
- Which payment methods contribute most to revenue

This project builds a lightweight analytics workflow to answer those questions using **SQL-first analysis** and visual reporting.

---

## Dataset

The project uses **6 datasets** from the Olist e-commerce data collection:

- **Orders** – order timestamps, delivery status, estimated vs actual delivery dates  
- **Order Items** – products sold in each order and item prices  
- **Payments** – payment type, installments, and payment value  
- **Customers** – customer identifiers and state-level location info  
- **Products** – product metadata including category  
- **Reviews** – customer review scores for completed orders  

---

## Tech Stack

- **SQL / SQLite** – data storage, joins, aggregations, KPI queries
- **Python**
  - **Pandas** – loading CSVs and running SQL query outputs into DataFrames
  - **Matplotlib** – dashboard-style visualizations
- **Jupyter Notebook** – exploratory analysis and reporting

---

## Workflow

### 1) Data Ingestion
CSV files were loaded into a local **SQLite database** using Pandas.

### 2) SQL Analysis
Custom SQL queries were written to answer business questions around:
- revenue trends
- category-level sales
- payment patterns
- delivery delays
- review score distribution
- repeat customer behavior

### 3) Visualization & Insight Generation
Query outputs were visualized in Python to build a compact dashboard and summarize business findings.

---

## Key Business Questions Answered

### Sales & Revenue
- How did monthly revenue change over time?
- Which product categories generated the highest revenue?
- Which payment methods contributed the most to sales?

### Customer Behavior
- What percentage of customers are repeat buyers?
- How are review scores distributed across orders?
- Do higher-revenue categories also receive better ratings?

### Operations & Delivery
- Which states show the highest average delivery delays?
- Are poor reviews linked to delivery or fulfillment issues?

---

## SQL Analyses Performed

The notebook includes SQL queries for:

1. **Monthly Revenue Trend**
   - Revenue by purchase month for delivered orders

2. **Top 10 Product Categories by Revenue**
   - Category-level revenue, order count, and average item price

3. **Average Order Value by Payment Method**
   - Revenue contribution and order value across payment types

4. **Average Delivery Delay by State**
   - Difference between actual and estimated delivery date by customer state

5. **Review Score Distribution**
   - Share of 1★ to 5★ reviews

6. **Revenue vs Average Review Score by Category**
   - Relationship between category revenue and customer ratings

7. **Repeat Customer Rate**
   - Share of customers placing more than one order

---

## Dashboard / Visualizations

The project includes the following visual outputs:

### 1. Monthly Revenue Trend
Shows how revenue evolved across the Olist time period, highlighting overall growth and seasonal peaks.

![Monthly Revenue](01_monthly_revenue.png)

---

### 2. Top 10 Product Categories by Revenue
Ranks the highest-performing categories by total revenue.

![Top Categories](02_top_categories.png)

---

### 3. Review Score Distribution
Shows the percentage distribution of customer ratings from 1 to 5 stars.

![Review Score Distribution](03_review_scores.png)

---

### 4. Revenue vs Average Review Score by Category
Compares category-level revenue against average review scores to identify strong and weak performers.

![Revenue vs Review Score](04_revenue_vs_review.png)

---

## Key Insights

### Revenue & Category Performance
- Revenue shows a **strong upward trend over time**, indicating platform growth through the analysis period.
- A few product categories contribute a **disproportionately high share of revenue**, making category prioritization important.
- Categories such as **gifts, beauty/health, home, and sports/leisure** appear among the top revenue drivers.

### Customer Satisfaction
- **5-star reviews dominate the distribution**, suggesting generally positive customer sentiment.
- However, the presence of **1-star and 2-star reviews** indicates meaningful service gaps that still need attention.
- High revenue does **not always guarantee the highest ratings**, so commercial success and customer satisfaction should be tracked together.

### Operations & Delivery
- Delivery delays vary across states, which may point to **regional logistics bottlenecks**.
- Poor delivery performance is a likely contributor to low review scores in some cases.
- Monitoring estimated vs actual delivery timelines can help reduce customer dissatisfaction.

### Customer Retention
- Repeat customer rate provides a direct signal of **retention and loyalty**.
- Combining repeat-rate analysis with review behavior can help identify which customer segments are most valuable.

---

## Repository Structure

```bash
.
├── code(3).ipynb                # Main notebook with SQL analysis + charts
├── 01_monthly_revenue.png       # Monthly revenue trend chart
├── 02_top_categories.png        # Top categories by revenue
├── 03_review_scores.png         # Review score distribution
├── 04_revenue_vs_review.png     # Revenue vs avg review score plot
└── README.md
```

---

## How to Run

### 1. Clone the repository
```bash
git clone <your-repo-link>
cd <your-repo-folder>
```

### 2. Install dependencies
```bash
pip install pandas matplotlib jupyter
```

### 3. Add the Olist CSV files
Place the following files in the project directory:
- `olist_orders_dataset.csv`
- `olist_order_items_dataset.csv`
- `olist_order_payments_dataset.csv`
- `olist_customers_dataset.csv`
- `olist_products_dataset.csv`
- `olist_order_reviews_dataset.csv`

### 4. Run the notebook
Open the notebook and execute all cells:
```bash
jupyter notebook
```

---

## Example KPIs Produced

- Total revenue by month
- Top product categories by revenue
- Average order value by payment type
- Delivery delay by customer state
- Review score distribution
- Revenue vs review score by category
- Repeat customer rate

---

## Why this project matters

This project demonstrates how to:
- use **SQL for end-to-end business analysis**
- combine **relational data from multiple tables**
- build **decision-oriented dashboards from raw transactions**
- convert raw e-commerce data into **sales, retention, and customer-experience insights**

It is a strong example of a **data analyst / business intelligence style project** focused on practical KPI tracking and insight generation.

---

## Future Improvements

Possible extensions for this project:
- Add **customer segmentation** (RFM / cohort analysis)
- Build a **seller-level performance dashboard**
- Analyze **payment installments vs order value**
- Study **delivery delay vs review score** more directly
- Deploy the dashboard using **Power BI / Tableau / Streamlit**

---

## Author

**Rajgowtham M**
