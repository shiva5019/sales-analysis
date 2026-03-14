# 📊 Power BI Sales Analysis Project

An end-to-end Power BI dashboard project designed to analyze **sales performance, profit trends, and customer behavior** for a retail company.  
The dashboard addresses both **CEO** and **Marketing & Product Team** requirements, transforming raw multi-year sales data into actionable business insights.

---

## 🔗 Project Context

This project demonstrates **data cleaning, modelling, DAX calculations, and interactive dashboard design** in Power BI.

- Built using sales data (2017–2020).  
- Focused on performance insights across **countries, categories, and customers**.  
- Features drill-through pages, tooltips, and dynamic measures for deep analysis.  

---

## 🎯 Project Objectives

The goal was to create an **interactive reporting system** that serves two user perspectives:

1. **CEO Dashboard** — to track company-wide revenue and profit development.  
2. **Marketing & Product Team Dashboard** — to analyze category-level and customer-level trends.

---

## 📁 Repository Structure
```bash

PowerBI-Sales-analysis/
│
├── Instructions/
│ └── Instructions.pdf                             # Project overview and business requirements
│
├── Notes/
│ └── PBI_sales_analysis_notes.pdf                 # Detailed handwritten notes and visual planning
│
├── Scripts/
│ ├── Final Project CEO.pbix                       # CEO dashboard (profit, loss, and revenue KPIs)
│ └── Final Project Marketing Team.pbix            # Marketing & product analysis dashboard
│
├── data/
│ ├── Retail Company Data.xlsx                     # Master data file containing all entities
│ ├── Sales2017.csv                                # Year-wise sales data
│ ├── Sales2018.csv
│ ├── Sales2019.csv
│ └── Sales2020.csv
│
└── readme.txt                                     # Setup instructions / documentation

```
---
## ⚙️ Data Preparation Process

### **1. Data Loading**
- Imported all yearly sales files: `Sales2017.csv`, `Sales2018.csv`, `Sales2019.csv`, `Sales2020.csv`.
- Set the first row as headers and standardized data types.
- Removed redundant columns and combined yearly files into one consolidated **Sales** table.

### **2. Data Transformation**
- Cleaned customer, reseller, and product data:
  - Removed nulls and unnecessary columns (e.g., Postal).
  - Split combined columns (City/State/Country) using delimiters.
- Adjusted column types (Date, Numeric, Text).

### **3. Data Modelling**
- **Fact Table:** `Sales`
- **Dimension Tables:** `Customer`, `Product`, `Sales Territory`, `Reseller`, `Sales Order`
- Established **1-to-Many** relationships between dimensions and the Sales fact table.
- Added an additional **Date Table** for time intelligence.

---

## 📐 Measure Creation (DAX)

| Measure | Description |
|----------|-------------|
| **Revenue** | Total revenue from sales |
| **Profit** | Total profit after cost deduction |
| **Revenue YTD** | Year-to-date cumulative revenue |
| **Profit YTD** | Year-to-date cumulative profit |
| **Previous Year Profit** | Profit using `DATEADD` for year-over-year comparison |
| **Profit Margin** | `(Profit / Revenue)` calculated dynamically |
| **Average Profit per Customer** | `(Total Profit / Distinct Customers)` |

---

## 🧩 CEO Dashboard Requirements

### **1. Profit/Loss by Country**
- Used a **Tree Map** visual:  
  - Category → Country  
  - Details → Categories  
  - Values → Profit  
- Added **tooltip page** with a line chart (`Profit vs Order Date`) for drill-through.

### **2. Revenue Trend Over Time**
- Implemented **Line Chart** showing `Revenue vs Order Date Key`.  
- Added a **Zoom Slider** for interactive period selection.

### **3. Profit by Categories/Subcategories**
- Used **Matrix Visual**:
  - Rows → Subcategory  
  - Columns → Category  
  - Values → Profit  
- Added **Data Bars** with custom color formatting for clear readability.

---

## 📈 Marketing & Product Team Dashboards

### **Page 1: Marketing Team Overview**
- **Visual 1: Total Sales YTD** → Line Chart (Date on X-axis, Revenue YTD on Y-axis).  
- **Visual 2: Profit Comparison** →  
  - Measures for `Profit`, `Previous Year Profit`, and `Difference`.  
  - Table visual showing side-by-side yearly comparisons.

---

### **Page 2: Details Page (Drill-through)**
- **Table Visual** with Order Date, Product, Country, and Key Metrics.  
- Enabled **Drill-through** using:
  - `OrderDateKey`  
  - `Country`  
  - `Product`

---

### **Page 3: Customer Analysis**
- **Visual 1: Average Profit per Customer**  
  - Custom DAX measure plotted against Date.  
- **Visual 2: Top 10 Customers by Revenue**  
  - Table visual filtered using Top N logic on `Revenue`.

---

### **Page 4: Extended Marketing Insights**
- **Revenue per Category** → Line chart (`Date` vs `Revenue` with `Category` in Legend).  
- **Profit Margin Over Time** → Line chart (`Date` on X-axis, `Profit Margin` on Y-axis).  
- **Profit-Making Categories/Subcategories/Products** →  
  - Multi-row card visuals with filters applied for positive-profit entities.

---

## 🎨 Key Features & Interactivity

- **Dynamic drill-through navigation**
- **Tooltip-based performance trends**
- **Custom measures for YoY comparison**
- **Data bars, slicers, and formatted visuals**
- **Multi-perspective dashboards for CEO & Marketing**

---

## 📊 Insights Delivered

| Focus Area | Key Findings |
|-------------|--------------|
| **Country-level Performance** | Certain regions contribute disproportionately to profit; tooltip highlights emerging markets. |
| **Product Profitability** | Top subcategories dominate >60% of profit share. |
| **Customer Trends** | High-value customers identified through revenue concentration. |
| **Year-over-Year Growth** | Clear improvement in YTD metrics visualized via dynamic DAX measures. |

---

## 🚀 Tools & Technologies

- **Power BI Desktop**  
- **DAX (Data Analysis Expressions)**  
- **Power Query Editor**  
- **Excel / CSV for Source Data**

---

## 📂 Output Files

| File | Description |
|------|--------------|
| `Final Project CEO.pbix` | CEO dashboard focusing on revenue & profit KPIs |
| `Final Project Marketing Team.pbix` | Multi-page dashboard for marketing analysis |
| `PBI_sales_analysis_notes.pdf` | Planning and handwritten workflow |
| `Retail Company Data.xlsx` | Consolidated dataset |

---

## 💡 Learnings

- Built practical experience in **data cleaning and modelling** inside Power BI.  
- Learned **DAX measure creation** for dynamic reporting.  
- Designed **multi-layer dashboards** with drill-through and tooltip functionality.  
- Understood **stakeholder-oriented visualization**—different dashboards for different needs.

---


## 👨‍💻 Author

**Shivam Kumar**  
Data Analyst | Writer 
> Building bridges between data pipelines and human insight.  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/meshivamk/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github)](https://github.com/meshivamk)

