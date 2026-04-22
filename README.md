# Financial-Audit-Profitability-Analysis-System-MySQL-
SQL-based financial audit system — tracks departmental revenue, expenses, and profitability across 5 departments using normalized schema, JOINs, subqueries, and audit summary views.

💼 Financial Audit & Profitability Analysis System
A SQL-based financial analysis system built to track departmental revenue and expenses, calculate profitability, detect high-spending departments, and produce audit-ready summary views for management reporting.

🎯 Project Overview
This project simulates a corporate financial audit environment using a normalized relational database across 5 departments over a 2-month period (Jan–Feb 2025). The goal was to analyze departmental profitability, flag departments exceeding average expense thresholds, and build a reusable audit summary view for management reporting.

🗂️ Database Schema
3 tables, fully normalized with foreign key relationships:
TableDescriptiondepartmentsDepartment ID, name, and manager namerevenueRevenue entries per department with date and amountexpensesExpense entries per department with date, category, and amount
1 view:
ViewDescriptiondepartment_audit_summaryCombines revenue and expense data — shows total revenue, total expense, and profit per department

🔍 Analysis Performed
1. Total Revenue per Department
Aggregated revenue per department using JOIN and GROUP BY across the departments and revenue tables.
2. Total Expense per Department
Aggregated expenses per department using JOIN and GROUP BY across the departments and expenses tables.
3. Profit Calculation
Calculated net profit per department as revenue minus expenses using a three-table JOIN with grouped aggregates.
4. High Expense Detection
Used a nested subquery to identify departments whose total expenses exceed the average departmental expense — flagging outliers for audit review.
5. Expense Category Breakdown
Ranked expense categories (Salary, Equipment, Advertising, etc.) by total spend using GROUP BY and ORDER BY.
6. Audit Summary View
Created a reusable VIEW combining all key metrics — revenue, expense, and profit per department — ready for direct management reporting.

💡 Key Findings

Marketing was identified as a loss-making department after a campaign failure expense pushed total expenses above total revenue
Operations had the highest expense bill driven by Equipment and Maintenance costs
HR had the lowest expense total and remained profitable across both months
High-spending departments flagged by subquery: Marketing and Operations


🛠️ Tech Stack
MySQL — schema design, data insertion, querying, views
SQL Concepts Used:

Normalized relational schema with foreign key constraints
INNER JOINs across multiple tables
GROUP BY with aggregate functions (SUM, AVG)
Nested subqueries with HAVING clause
CREATE VIEW for reusable reporting


▶️ How to Run

Open MySQL Workbench and connect to your local server
Open the .sql file
Run the full script — it creates the database, inserts data, runs all analysis queries, and creates the audit view
Query SELECT * FROM department_audit_summary; to see the final audit report


👤 Author
Parush Tikoo | linkedin.com/in/parush-tikoo | github.com/tikooparush
