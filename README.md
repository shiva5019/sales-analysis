# 📊 Power BI Sales Analysis Project

An end-to-end Power BI dashboard project designed to analyze **sales performance, profit trends, and customer behavior** for a retail company.  
The dashboard addresses both **CEO** and **Marketing & Product Team** requirements, transforming raw multi-year sales data into actionable business insights.

---

## 🔗 Project Context

This project demonstrates **data cleaning, modelling, DAX calculations, and interactive dashboard design** in Power BI.

- Built using sales data (2017–2020)
- Focused on performance insights across **countries, categories, and customers**
- Features drill-through pages, tooltips, and dynamic measures for deep analysis

---

## 🎯 Project Objectives

The goal was to create an **interactive reporting system** that serves two user perspectives:

1. **CEO Dashboard** — to track company-wide revenue and profit development  
2. **Marketing & Product Team Dashboard** — to analyze category-level and customer-level trends

---

## 📁 Repository Structure

```bash
PowerBI-Sales-analysis/
│
├── Instructions/
│   └── Instructions.pdf
│
├── Notes/
│   └── PBI_sales_analysis_notes.pdf
│
├── Scripts/
│   ├── Final Project CEO.pbix
│   └── Final Project Marketing Team.pbix
│
├── data/
│   ├── Retail Company Data.xlsx
│   ├── Sales2017.csv
│   ├── Sales2018.csv
│   ├── Sales2019.csv
│   └── Sales2020.csv
│
└── README.md
```

---

## ⚙️ Data Preparation Process

### 1️⃣ Data Loading
- Imported yearly sales files  
- Standardized headers and data types  
- Combined all files into one **Sales table**

### 2️⃣ Data Transformation
- Cleaned customer, reseller, and product data
- Removed null values and unnecessary columns
- Split combined location columns (City/State/Country)

### 3️⃣ Data Modelling
- **Fact Table:** Sales  
- **Dimension Tables:** Customer, Product, Sales Territory, Reseller, Sales Order  
- Created **1-to-many relationships**
- Added **Date Table** for time analysis

---

## 📐 Measure Creation (DAX)

| Measure | Description |
|--------|-------------|
| Revenue | Total revenue from sales |
| Profit | Total profit after cost deduction |
| Revenue YTD | Year-to-date cumulative revenue |
| Profit YTD | Year-to-date cumulative profit |
| Previous Year Profit | Profit comparison with previous year |
| Profit Margin | `(Profit / Revenue)` |
| Avg Profit per Customer | `(Total Profit / Distinct Customers)` |

---

## 🧩 CEO Dashboard

### Profit/Loss by Country
- Tree Map visualization
- Category → Country
- Values → Profit
- Tooltip showing profit trend

### Revenue Trend Over Time
- Line chart showing revenue over time
- Interactive zoom slider

### Profit by Categories
- Matrix visualization
- Data bars for easy comparison

---

## 📈 Marketing & Product Dashboard

### Marketing Overview
- Total Sales YTD line chart
- Profit comparison table

### Customer Analysis
- Average profit per customer
- Top 10 customers by revenue

### Extended Insights
- Revenue per category
- Profit margin trends
- Profit-making categories

---

## 🎨 Key Features

- Interactive dashboards
- Drill-through navigation
- Tooltip analysis
- Year-over-year comparison
- Dynamic DAX calculations

---

## 📊 Insights

| Area | Insight |
|-----|--------|
| Country Performance | Certain regions drive most profit |
| Product Profitability | Few categories dominate revenue |
| Customer Trends | High-value customers identified |
| Yearly Growth | Clear YoY revenue improvement |

---

## 🚀 Tools Used

- Power BI Desktop  
- DAX  
- Power Query  
- Excel / CSV Data

---

## 👨‍💻 Author

**Shiva Jetpol**

Data Analyst

GitHub: https://github.com/shiva5019
