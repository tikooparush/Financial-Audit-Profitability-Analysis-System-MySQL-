# 💼 Financial Audit & Profitability Analysis System

🔍 **SQL-Based Financial Data Analysis Project**
A relational database system built to track departmental revenue and expenses, calculate profitability, detect high-spending departments, and produce audit-ready summary views for management reporting.


## 📌 Project Overview

Financial auditing is a critical function in any organization. This project simulates a corporate financial audit environment using a **normalized relational database** across 5 departments over a 2-month period (Jan–Feb 2025).

The goal is to identify loss-making departments, flag high-expense outliers, and produce structured reports that can directly support management decision-making.


## 🎯 Key Business Questions Answered

- 💰 What is the total revenue and expense per department?
- 📉 Which departments are operating at a loss?
- ⚠️ Which departments exceed the average expense threshold?
- 🗂️ What are the highest-spend expense categories?
- 📊 How can all key metrics be presented in a single audit summary?


## 🛠️ Tools & Technologies Used

- **MySQL** → Schema design, data insertion, querying, and views
- **MySQL Workbench** → Query execution and database management

**SQL Concepts Used:**
- Normalized relational schema with foreign key constraints
- INNER JOINs across multiple tables
- GROUP BY with aggregate functions (SUM, AVG)
- Nested subqueries with HAVING clause
- CREATE VIEW for reusable management reporting


## 🗂️ Database Schema

**3 Tables, fully normalized with foreign key relationships:**

| Table | Description |
|-------|-------------|
| `departments` | Department ID, name, and manager name |
| `revenue` | Revenue entries per department with date and amount |
| `expenses` | Expense entries per department with date, category, and amount |

**1 View:**

| View | Description |
|------|-------------|
| `department_audit_summary` | Combines revenue and expense data — shows total revenue, total expense, and profit per department |


## 📊 Key Insights

### 🔹 1. Revenue & Expense Analysis
- Aggregated total revenue and expenses per department using multi-table JOINs and GROUP BY.

### 🔹 2. Profitability Calculation
- Calculated net profit per department as revenue minus expenses — identified departments in the red.

### 🔹 3. High Expense Detection
- Used a **nested subquery** to flag departments whose total expenses exceed the average departmental expense threshold.

### 🔹 4. Expense Category Breakdown
- Ranked all expense categories (Salary, Equipment, Advertising, etc.) by total spend to identify cost drivers.

### 🔹 5. Audit Summary View
- Built a reusable **VIEW** combining all key metrics — ready for direct management reporting without rewriting queries.


## 💡 Key Findings

- **Marketing** was identified as a loss-making department — campaign expenses pushed total costs above revenue
- **Operations** had the highest overall expense bill driven by Equipment and Maintenance costs
- **HR** remained profitable across both months with the lowest expense total
- High-spending departments flagged by subquery: **Marketing** and **Operations**


## 📂 Project Structure
financial-audit-analysis/
│
├── Financial_Audit_Profitability_Analysis.sql   ← Schema + Data + Queries + View
└── README.md


## ▶️ How to Run

1. Open **MySQL Workbench** and connect to your local server
2. Open `Financial_Audit_Profitability_Analysis.sql`
3. Run the full script — it creates the database, inserts data, runs all analysis queries, and creates the audit view
4. Run `SELECT * FROM department_audit_summary;` to see the final audit report


## 💡 Conclusion

This project demonstrates how **structured SQL analysis** can turn raw financial data into actionable business insights — identifying loss-making departments, flagging budget overruns, and producing audit-ready reports directly from the database layer.


## 👤 Author

**Parush Tikoo**


## ⭐ If you found this useful

Give this repo a ⭐ and feel free to connect!
