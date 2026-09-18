# ZEPTO_SQL_DATA_ANALYST_PROJECT
ZEPTO E-COMMERCE DATA ANALYST PORTFOLIO PROJECT
# 🛒 Zepto E-Commerce Data Analysis

##  Project Overview

This project analyzes **Zepto e-commerce sales and product data** to identify important business insights related to **sales, pricing, discounts, product categories, inventory, and customer demand**.

The project demonstrates how a Data Analyst can use **Python, SQL, Excel, and Power BI** to clean, analyze, visualize, and communicate business data.

The main objective is to convert raw e-commerce data into **actionable business insights** that can help improve sales performance, pricing decisions, inventory management, and product strategy.

---

##  Business Objectives

The analysis aims to answer questions such as:

* Which product categories generate the most sales?
* Which products have the highest revenue?
* What is the impact of discounts on sales?
* Which products are frequently out of stock?
* What are the most expensive and cheapest products?
* Which categories have the highest average prices?
* How does product availability vary across categories?
* Which products contribute most to overall revenue?
* What are the major sales trends?
* Which products/categories should receive more attention?

---

##  Dataset

The dataset contains e-commerce product and sales-related information.

### Important Columns

| Column           | Description                 |
| ---------------- | --------------------------- |
| Product Name     | Name of the product         |
| Category         | Product category            |
| Brand            | Product brand               |
| Price            | Original product price      |
| Discount         | Discount offered            |
| Discounted Price | Price after discount        |
| Quantity         | Quantity sold/available     |
| Stock            | Available inventory         |
| Availability     | Product availability status |
| Revenue          | Revenue generated           |

> **Note:** Column names may vary depending on the dataset used for this project.

---

# Tools & Technologies

### Python

* Pandas
* NumPy
* Matplotlib
* Seaborn

### SQL

* SELECT
* WHERE
* GROUP BY
* ORDER BY
* JOIN
* Aggregate Functions
* CASE statements
* Subqueries

### Power BI

* Data visualization
* KPI cards
* Interactive dashboard
* Filters and slicers
* Category analysis
* Sales analysis

### Excel

* Data cleaning
* Pivot Tables
* VLOOKUP/XLOOKUP
* Charts
* Basic data analysis

---

#  Project Workflow

```text
Raw E-Commerce Data
        ↓
Data Cleaning
        ↓
Exploratory Data Analysis
        ↓
SQL Analysis
        ↓
Power BI Dashboard
        ↓
Business Insights
        ↓
Recommendations
```

---

#  Python Data Analysis

Python was used to clean and analyze the dataset.

### Main Steps

1. Imported the dataset using Pandas.
2. Checked the structure of the dataset.
3. Identified missing values.
4. Removed duplicate records.
5. Corrected data types.
6. Cleaned product and category names.
7. Created calculated columns.
8. Performed exploratory data analysis.
9. Analyzed product categories and pricing.
10. Created charts to identify important trends.

### Example Python Operations

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

df = pd.read_csv("zepto_data.csv")

print(df.head())
print(df.info())
print(df.isnull().sum())

# Category analysis
category_sales = df.groupby("Category")["Revenue"].sum()

print(category_sales)
```

---

#  SQL Analysis

SQL was used to perform business-oriented analysis on the dataset.

### Example Questions

#### 1. Find total revenue

```sql
SELECT SUM(Revenue) AS Total_Revenue
FROM zepto_sales;
```

#### 2. Find revenue by category

```sql
SELECT 
    Category,
    SUM(Revenue) AS Total_Revenue
FROM zepto_sales
GROUP BY Category
ORDER BY Total_Revenue DESC;
```

#### 3. Find top-selling products

```sql
SELECT 
    Product_Name,
    SUM(Quantity) AS Total_Quantity
FROM zepto_sales
GROUP BY Product_Name
ORDER BY Total_Quantity DESC;
```

#### 4. Find products with high discounts

```sql
SELECT 
    Product_Name,
    Price,
    Discount,
    Discounted_Price
FROM zepto_sales
WHERE Discount > 20
ORDER BY Discount DESC;
```

#### 5. Find out-of-stock products

```sql
SELECT 
    Product_Name,
    Category
FROM zepto_sales
WHERE Availability = 'Out of Stock';
```

---

#  Power BI Dashboard

A Power BI dashboard was created to provide an interactive view of the e-commerce business.

### Dashboard KPIs

*  Total Revenue
*  Total Products
*  Total Quantity Sold
*  Average Discount
*  Average Product Price
*  Number of Categories
*  Out-of-Stock Products

### Dashboard Visualizations

* Revenue by Category
* Top 10 Products by Revenue
* Top Products by Quantity Sold
* Discount Analysis
* Product Availability
* Category-wise Pricing
* Revenue Distribution
* Product Stock Analysis

### Interactive Filters

Users can filter the dashboard by:

* Category
* Brand
* Product
* Price Range
* Discount
* Availability

---

#  Key Business Insights

The analysis can be used to identify:

* High-performing product categories.
* Products contributing significantly to revenue.
* Products with high customer demand.
* Categories with comparatively higher prices.
* Products receiving larger discounts.
* Products frequently facing stock availability issues.
* Relationship between pricing, discounts, and sales.
* Areas where inventory planning can be improved.

> **Important:** The exact insights should be updated based on the results of the dataset used in the project.

---

# Business Recommendations

Based on the analysis, e-commerce businesses can:

1. Focus inventory planning on high-demand products.
2. Monitor frequently out-of-stock products.
3. Analyze discount effectiveness before offering large discounts.
4. Promote high-performing products.
5. Review pricing for products with low sales.
6. Use category-level performance to improve product assortment.
7. Monitor revenue contribution from different categories.
8. Use historical sales patterns to improve inventory forecasting.

---

# Project Structure

```text
Zepto-Ecommerce-Data-Analysis/
│
├── data/
│   └── zepto_data.csv
│
├── python/
│   └── zepto_analysis.ipynb
│
├── sql/
│   └── zepto_analysis.sql
│
├── powerbi/
│   └── zepto_dashboard.pbix
│
├── screenshots/
│   └── dashboard.png
│
└── README.md
```

---

#  How to Run the Project

### Step 1 — Clone the Repository

```bash
git clone https://github.com/yourusername/Zepto-Ecommerce-Data-Analysis.git
```

### Step 2 — Install Python Libraries

```bash
pip install pandas numpy matplotlib seaborn
```

### Step 3 — Open the Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
python/zepto_analysis.ipynb
```

### Step 4 — SQL Analysis

Open:

```text
sql/zepto_analysis.sql
```

Run the queries using MySQL or another compatible SQL database.

### Step 5 — Power BI

Open:

```text
powerbi/zepto_dashboard.pbix
```

---

#  Dashboard Preview

Add your Power BI dashboard screenshot here:

```markdown
![Zepto Power BI Dashboard](screenshots/dashboard.png)
```

---

#  Skills Demonstrated

This project demonstrates practical knowledge of:

* Data Cleaning
* Data Wrangling
* Exploratory Data Analysis
* Python
* Pandas
* NumPy
* SQL
* Excel
* Power BI
* Data Visualization
* KPI Development
* Business Analysis
* Business Insights
* Data Storytelling

---

# Author

**Dhruv Bhardwaj**

 Aspiring Data Analyst

Skills: **Python | SQL | Excel | Power BI | Data Analytics**

---.
