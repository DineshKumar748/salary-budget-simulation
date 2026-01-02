# Rule-Based Salary Simulation Using SQL Window Functions

## 📌 Project Overview
This project simulates a **rule-based salary revision policy** to analyze its **financial impact before implementation**.  
It helps HR and finance teams evaluate salary changes safely without modifying real employee data.

The solution uses **SQL window functions, CASE logic, and Common Table Expressions (CTEs)** to perform scalable what-if analysis.

🔐 **Security Note:** Database credentials are not included. Update locally before running.

---

## 🧩 Business Problem
Annual salary revisions can lead to:
- Budget overruns
- Inequitable salary increases
- Difficult rollbacks

This project answers:
- Who should receive a raise?
- How much should each employee receive?
- What is the department-level cost impact?
- Can the organization stay within budget?

---

## 📋 Salary Rules
Employees are evaluated relative to their **department average salary**:
- **Low** (< 90%) → **10% raise**
- **Mid** (90–110%) → **5% raise**
- **High** (> 110%) → **No raise**

---

## 💰 Budget Constraint Logic
Each department has a **fixed salary increase budget**.
- If total raises are within budget → applied fully
- If exceeded → raises are **scaled proportionally**

---

## 🛠️ Tools & Technologies
- SQL (CTEs, Window Functions, CASE)
- MySQL 8+
- Python (Pandas, SQLAlchemy)
- Jupyter Notebook

---

## 📊 Output
**Employee-Level**
- Current salary
- Department average
- Salary category
- Simulated new salary

**Department-Level**
- Total salary before revision
- Total salary after revision
- Budget utilization

---

## ▶️ How to Run
1. Create a database named `hr_db`
2. Update credentials locally
3. Run notebook cells in order

---

## 👤 Author
**Dinesh Kumar**  
SQL | Data Analytics | MySQL | Window Functions
