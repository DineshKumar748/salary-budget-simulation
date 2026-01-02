# Rule-Based Salary Simulation Using SQL Window Functions

## ?? Project Overview
This project simulates a **rule-based salary revision policy** to analyze its **financial impact before implementation**.  
The goal is to help HR and finance teams understand how different pay rules affect **individual employees and department budgets** without modifying actual salary data.

The solution uses **SQL window functions, CASE logic, and Common Table Expressions (CTEs)** to perform a safe and scalable what-if analysis.

?? **Security Note:** Credentials are not included. Update locally before running.

---

## ?? Business Problem
Organizations revise salaries annually, but applying changes without analysis can lead to:
- Budget overruns
- Inequitable raises
- Difficult rollbacks

This project answers:
- Who should receive a raise?
- How much should each employee receive?
- What is the total cost impact per department?
- Can the company stay within its annual budget?

---

## ?? Salary Rules
Employees are classified based on their salary relative to their **department average**:
- **Low**: Salary < 90% of department average ? **10% raise**
- **Mid**: Salary between 90% and 110% ? **5% raise**
- **High**: Salary > 110% ? **No raise**

The logic ensures fairness within departments rather than using absolute salary values.

---

## ?? New-Year Budget Constraint
For the new year, each department is assigned a **fixed salary increase budget** (amount-based, not percentage).

- If the total calculated increase is **within the budget**, raises are applied fully.
- If the increase **exceeds the budget**, individual raises are **scaled proportionally** so the department stays within its allowed amount.

This mirrors real-world HR and finance planning.

---

## ??? Tools & Technologies
- **MySQL 8+**
- **SQL** (CTEs, Window Functions, CASE)
- **Python** (Pandas, SQLAlchemy)
- **Jupyter Notebook**

---

## ?? SQL Concepts Used
- `AVG() OVER (PARTITION BY department)` for department averages
- `CASE` expressions for rule-based classification
- CTEs for modular and readable queries
- Aggregations for department-level budget analysis
- Joins to combine employee and department metrics

---

## ?? Output

### Employee-Level
- Old salary
- Department average salary
- Salary category (Low / Mid / High)
- Simulated new salary
- Individual salary increase

### Department-Level
- Total salary before revision
- Total salary after revision
- Final budget usage per department

---

## ?? How to Run
1. Create a MySQL database named `hr_db`
2. Update the MySQL connection string in the notebook with your local credentials
3. Run the notebook cells in order

---

## ?? Key Insight
This project demonstrates how SQL can be used not just for querying data, but for **decision-making, scenario modeling, and budget planning**.

---

## ?? Author
**Dinesh Kumar**  
SQL | Data Analytics | MySQL | Window Functions












