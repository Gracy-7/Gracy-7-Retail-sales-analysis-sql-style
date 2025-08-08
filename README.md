# 🛒 Retail Sales Analysis Using Google Sheets (SQL Style)

## 📌 Project Overview
This project analyzes retail sales data using **Google Sheets** with SQL-style queries via the **QUERY function**.  
The goal was to explore and clean the dataset, perform SQL-style analysis, and visualize insights through charts and dashboards.

---

## 📂 Dataset
- **Source:** Generated sample retail dataset  
- **Rows:** 1,000+  
- **Columns:**
  - `Sale Date`
  - `Product Category`
  - `Product Name`
  - `Region`
  - `Customer Name`
  - `Quantity Sold`
  - `Unit Price`
  - `Total Sales`
  - `Stock Level`

---

## 🛠️ Tools & Skills Used
- **Google Sheets** – Data cleaning, transformation, and visualization  
- **QUERY Function** – SQL-style data analysis in Sheets  
- **Pivot Tables** – Summarizing sales data  
- **Charts** – Creating sales trends and performance visuals  
- **Data Cleaning** – Removing text formatting, fixing number columns

---

## 🧹 Data Cleaning Steps
1. Removed currency symbols and formatting from numeric columns (`Quantity Sold`, `Unit Price`, `Total Sales`).
2. Converted date column into proper date format.
3. Fixed non-numeric column issues using **REGEXREPLACE** and **VALUE** functions.
4. Removed duplicates and missing values.
5. Standardized region and category names.

---

## 📊 Analysis Performed
- **Category-wise Sales** – Total sales by product category.
- **Region-wise Sales** – Comparing sales performance across regions.
- **Top Selling Products** – Ranking products by sales.
- **category wise sales for specific region** – Total sales by category filter with specific region.
- **Profit Calculation** – Using formula:  
  `Profit = Total Sales - (Quantity Sold × Cost Price)`

---

## 📈 Dashboard
The interactive Google Sheets dashboard includes:
- **Bar chart**: Sales by category
- **Pie chart**: Quantity sold by product
- **KPI cards**: Total Sales, Quantity Sold, Average Price
- **scatter plot**: Quantity sold vs Total sales

![Dashboard Screenshot](https://github.com/Gracy-7/Gracy-7-Retail-sales-analysis-sql-style/"Retail-Sales-Dashboard.png")

---

## 📜 Example sql-style query
```sql
SELECT ProductCategory, SUM(TotalSales) 
WHERE Region = 'North' 
GROUP BY ProductCategory 
ORDER BY SUM(TotalSales) DESC

## Google Sheets version:

=QUERY(SalesData!A1:K1001, 
"SELECT C, SUM(I) 
WHERE E = 'North' 
GROUP BY C 
ORDER BY SUM(I) DESC", 1)

---

## 📂 Project structure

Retail-Sales-Analysis
│── Retail_Sales_Analysis_GoogleSheets.xlsx
│── README.md
│── dashboard.png

---

## 🚀 How to use

1. **Open Google Sheets** and import the dataset.  
2. Use the **QUERY function** in Sheets for SQL-style analysis.  
   Example:
   ``` =QUERY(A1:G1000, "SELECT C, SUM(F) WHERE F IS NOT NULL GROUP BY C ORDER BY SUM(F) DESC", 1)
3. Create Pivot Tables for quick summaries.
4. Build charts directly in Sheets to visualize the results.

---

## 📌 Key Insights

Product X is the highest-selling product in revenue.

The North Region leads in overall sales, while the South Region has the highest average order value.

Some products require stock refills due to high demand.

Profit margins vary greatly across categories, suggesting targeted pricing strategies.

---

## 📬 Contact

📧 Email: gracymanisha@gmail.com

📊 GitHub: https://github.com/Gracy-7
