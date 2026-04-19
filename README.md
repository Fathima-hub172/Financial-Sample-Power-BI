# 💰 Financial Sample – Data Analysis Project

## 📌 Overview
This project analyzes a **Financial Sample dataset** using **Power BI and Python (Pandas, NumPy, Seaborn, Matplotlib)**.  
It demonstrates data cleaning, calculated columns, DAX measures, and interactive dashboards to uncover insights into sales, profit, discounts, and COGS.

## 🎯 Objectives
- Import and preprocess financial data
- Create **calculated columns** (Profit Margin %, Discount %, COGS % of Sales, Year-Month Key, Unit Revenue)
- Build **DAX measures** for Total Sales, Total Profit, YOY Growth %, Segment Contribution %
- Design recruiter‑friendly dashboards with professional color palettes
- Generate **Python visualizations** for exploratory analysis

## 🗂️ Dataset
Typical columns include:
- **Date**
- **Country**
- **Segment**
- **Product**
- **Sales**
- **Profit**
- **Discounts**
- **COGS**
- **Units Sold**

## 🔑 Features
- **Data Cleaning**: Handle missing values and inconsistent formats
- **Calculated Columns**:
  - Profit Margin % = Profit / Sales
  - Discount % = Discounts / Sales
  - COGS % of Sales = COGS / Sales
  - Year-Month Key for time series analysis
- **DAX Measures**:
  - Total Sales, Total Profit, YOY Sales Growth %
  - Average Unit Revenue
  - Segment Contribution %
- **Dashboards**:
  - Sales & Profit Trends
  - Discount Impact Analysis
  - Segment & Country Performance

## 🛠️ Tech Stack
- **Power BI**: DAX measures, calculated columns, dashboards
- **Python**: Pandas, NumPy, Matplotlib, Seaborn, Plotly
- **Excel**: Original dataset source

## 📊 Example DAX Code
```DAX
Total Sales = SUM(Financials[Sales])
Total Profit = SUM(Financials[Profit])
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)
YOY Sales Growth % = 
    DIVIDE([Total Sales] - CALCULATE([Total Sales], DATEADD(Financials[Date], -1, YEAR)),
           CALCULATE([Total Sales], DATEADD(Financials[Date], -1, YEAR)), 0)
