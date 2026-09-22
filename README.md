# 🛒 Superstore Sales Analysis - SQL Project

## 📌 Project Overview
This project analyzes **9800 orders** from the Superstore dataset using **Python, Pandas & SQLite** in Google Colab.
Converted the CSV dataset into SQL database and performed business analysis using SQL queries.

## 📂 Dataset
- **File:** train.csv
- **Rows:** 9800
- **Columns:** 18 (Order ID, Customer, Product, Sales, Profit, Region, etc.)
- **Database:** superstore.db (SQLite)

## 🔧 Tools Used
- Python
- Pandas
- SQLite
- Google Colab

## ⚙️ Steps Performed
1. Uploaded train.csv to Colab
2. Cleaned column names (replaced space with underscore)
3. Created SQLite database: superstore.db
4. Loaded data into table: orders
5. Executed 8 SQL business queries

## 📊 SQL Queries Executed

### 1. Total Sales & Profit
```sql
SELECT SUM(Sales) as Total_Sales FROM orders;
### 2. Sales by Category
SELECT Category, SUM(Sales) as Sales FROM orders GROUP BY Category;
### 3. Sales by Region
SELECT Region, SUM(Sales) as Sales FROM orders GROUP BY Region ORDER BY Sales DESC;
### 4. Top 5 Customers by Sales
SELECT Customer_Name, SUM(Sales) as Sales FROM orders GROUP BY Customer_Name ORDER BY Sales DESC LIMIT 5;
### 5. Top 5 Sub-Category by Sales
SELECT Sub_Category, SUM(Sales) as Sales FROM orders GROUP BY Sub_Category ORDER BY Sales DESC LIMIT 5;
### 6. Top 5 States by Sales
SELECT State, SUM(Sales) as Sales FROM orders GROUP BY State ORDER BY Sales DESC LIMIT 5;
*Result:* California ($446,306), New York ($306,361), Texas ($168,572)

### 7. Orders by Ship Mode
SELECT Ship_Mode, COUNT(*) as Orders FROM orders GROUP BY Ship_Mode;
*Result:* Standard Class - 5859, Second Class - 1902, First Class - 1501, Same Day - 538

### 8. Top Selling Products
SELECT Product_Name, SUM(Sales) as Sales FROM orders GROUP BY Product_Name ORDER BY Sales DESC LIMIT 5;
*Result:* Canon imageCLASS 2200 Advanced Copier - $61,599 is highest selling

## 💡 Key Insights
- *Best State:* California generates highest sales
- *Preferred Shipping:* Customers mostly use Standard Class (5859 orders)
- *Top Product:* Canon imageCLASS 2200 Copier is most valuable product
- *Business Use:* This analysis helps in inventory and regional marketing decisions

## 📁 Project Files
- http://train.csv - Original Dataset
- Superstore_SQL_Project.ipynb - Google Colab Notebook
- http://superstore.db - SQLite Database
- http://README.md - Project Documentation

## ▶️ How to Run
1. Open Google Colab
2. Upload http://train.csv
3. Run the notebook cells
4. Database http://superstore.db will be auto-created


> **Conclusion:** Successfully converted CSV to SQL database and performed business analysis. The project shows strong SQL skills and data-driven decision making.

Copy done? Need help uploading to GitHub?
