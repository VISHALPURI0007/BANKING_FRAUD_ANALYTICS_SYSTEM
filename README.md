# BANKING_FRAUD_ANALYTICS_SYSTEM# 
# 🏦 End-to-End Banking Fraud & Risk Analytics System

A production-grade, enterprise-scale data analytics project designed to detect suspicious transactions, mitigate financial risks, and deliver actionable fraud intelligence for banking operations. 

---

## 🛠️ Tech Stack & Architecture Overview

The architecture implements a robust end-to-end data pipeline processing records through **Python ➔ SQL ➔ Excel (CSV) ➔ Power BI**.

### 1. Data Engineering & Simulation (Python)
* Built a custom data generation logic leveraging the `Faker` library to simulate an enterprise-scale banking environment with **1,000+ unique Customer Profiles** and thousands of transactions.
* Handled data pre-processing, schema alignment, and missing value treatments using `Pandas` and `NumPy` to make the synthetic data clean and relational-database-ready.

### 2. Relational Warehousing & Fraud Engineering (SQL - MySQL)
* Designed a normalized relational database leveraging a **Star Schema** architecture (`Customers` Dimension Table and `Transactions` Fact Table).
* Engineered a dynamic SQL `VIEW` utilizing advanced analytical **Window Functions (`LAG`)** and **CTEs (Common Table Expressions)** to identify real-time fraud vectors:
  * **Velocity Attacks:** Flags transactions occurring within short time intervals across physically impossible geographical locations.
  * **Night Spikes:** Monitors high-value transactions executed during high-risk hours (1:00 AM - 4:00 AM).
  * **ATM Churning:** Detects consecutive rapid cash withdrawals indicating cloned cards.
* Developed an operational **Stored Procedure** (`GetCustomerFraudReport`) enabling branch managers to instantly fetch a single customer's complete risk and compliance history.

### 3. Data Optimization & Intermediary Auditing (Excel / CSV)
* Emplemented enterprise best practices by exporting processed views into optimized **CSV (Comma Delimited)** formats.
* Conducted ad-hoc data auditing and schema verification to ensure resource-efficient data loading, reducing RAM footprint for subsequent business intelligence tools.

### 4. Enterprise Business Intelligence (Power BI)
* Engineered a highly interactive Executive Fraud Monitoring Dashboard utilizing native DAX expressions for risk scoring.
* **Key Visual Elements Included:**
  * **Geographical Slicers (Dynamic City Filters):** Allows region-wise drill-down of transaction behaviors.
  * **Core KPI Metrics:** Real-time visibility into total transaction volume and financial exposure.
  * **Fraud Distribution (Donut Visual):** Percent-of-total breakdown distinguishing Velocity Attacks vs. Night Spikes.
  * **Operational Fraud Alert Grid (Table View):** A high-priority table sorting critical alerts by severity to facilitate immediate legal and operational escalations.

---

## ⚙️ Key Database Artifacts Included

* `BANKING_FRAUD_DASHBOARD.pbix` - Complete Power BI dashboard workbook with dynamic calculations.
* `VIEW_DASHBOARD.PNG` - High-resolution dashboard screenshot for quick visualization assessment.
*
