# 🌍 Global Sales Dashboard – Power BI & SQL Project

### 🧩 Overview
This project analyzes sales performance across **six countries** —  USA, UK, Canada, Nigeria, India, and China.  
The goal was to clean, transform, and visualize multi-country sales data to uncover key insights on revenue, profit, top products, and store performance.

---

### 🧱 Project Workflow
**1️⃣ Data Source & Loading**
- Raw CSV files were uploaded to **PostgreSQL** (one per country).  
- Tables: `Canada Sales`, `China Sales`, `India Sales`, `Nigeria Sales`, `UK Sales`, `US Sales`.  
- Minor adjustments and validations were done in **Excel** (formatting & null checks).

**2️⃣ SQL Data Cleaning & Transformation**
All cleaning and transformation were handled using **PostgreSQL**:
- Combined six country tables using `UNION ALL` into a master table: **`Sales Data`**
- Checked for **missing values** and imputed where necessary  
- Fixed invalid records using `UPDATE` statements  
- Detected and handled **duplicate Transaction IDs**  
- Added calculated columns:
  - `Total Amount` = (`Price Per Unit` × `Quantity Purchased`) – `Discount Applied`
  - `Profit` = `Total Amount` – (`Cost Price` + `Quantity Purchased`)
- Ran multiple queries to extract insights:
  - **Total Revenue & Profit by Country**
  - **Top 5 Best-Selling Products**
  - **Top Sales Representatives**
  - **Best-Performing Store Locations**
  - **Key Sales & Profit Statistics (Min, Max, Avg, Total)**

> All SQL transformations were executed in PostgreSQL before importing the dataset into Power BI.

**3️⃣ Data Import & Modeling**
- Imported the cleaned `Sales Data` table into **Power BI** (Import mode via PostgreSQL connector).  
- Built relationships and data model for country and product dimensions.

**4️⃣ Dashboard Design**
Developed a dynamic, interactive **Power BI dashboard** featuring:
- **KPI cards** for total sales, profit, and discount trends  
- **Map visualization** to display Sales by country  
- **Bar/Column charts** for Daily Sales  
- **Date slicer** for time-based analysis  
- **DAX measures** for dynamic calculations (Total Sales, Total Profit, Average Revenue, etc.)

---


### 🧮 Tools & Technologies
| Category | Tool |
|-----------|------|
| Database | PostgreSQL |
| Query Language | SQL |
| Visualization | Power BI |
| Data Preparation | Excel |
| Languages/Concepts | DAX, SQL Joins, Data Modeling |

---

