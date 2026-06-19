# Task 3: Interactive Sales & Profit Dashboard

**Internship:** Data Analyst Internship — DataX Labs
**Task:** Dashboard Design
**Tool:** Power BI Desktop

## Objective
Design an interactive dashboard for business stakeholders to track sales, profit, and growth trends using key KPIs, filters, and visual breakdowns.

## Dataset
**Sample Superstore Dataset** (Kaggle) — ~10,000 rows of US retail order data spanning 2014–2017, including Sales, Profit, Discount, Region, Category, Sub-Category, and Customer Segment.
Source: https://www.kaggle.com/datasets/vivek468/superstore-dataset-final

## Process

### 1. Data Cleaning (Power Query Editor)
- Fixed Order Date and Ship Date column types using locale-aware conversion (English - United Kingdom, DD-MM-YYYY format) to resolve date parsing errors
- Removed duplicate rows
- Corrected data types across numeric columns (Sales, Profit, Discount, Quantity)
- Removed unused columns (Row ID)

### 2. DAX Measures
```DAX
Total Sales = SUM(Orders[Sales])
Total Profit = SUM(Orders[Profit])
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)
Total Orders = DISTINCTCOUNT(Orders[Order ID])
```

### 3. Dashboard Visuals
- **KPI Cards:** Total Sales, Total Profit, Profit Margin %, Total Orders
- **Line Chart:** Total Sales by Year (time-series trend)
- **Bar Chart:** Total Sales by Category
- **Bar Chart:** Total Profit by Region
- **Map:** Total Sales by State
- **Slicers:** Region, Category, Order Date (range slider)

### 4. Styling
Applied a consistent green color theme across all visuals (View → Themes) for a clean, professional look.

## Key Insights
- Total Sales: **2.30M** | Total Profit: **286.41K** | Profit Margin: **12%** | Total Orders: **5K**
- Sales grew steadily from 2014, with a sharp increase heading into 2017
- **West** region generates the highest profit, followed by East; Central is the lowest
- **Technology** is the top-selling category, ahead of Furniture and Office Supplies
- Region, Category, and Date slicers allow stakeholders to drill into any segment or time period instantly

## Files in this Repository
| File | Description |
|------|--------------|
| `Superstore_Dashboard.pbix` | Power BI project file (open in Power BI Desktop) |
| `Task3_Dashboard_Summary.pptx` | Slide summary of objective, process, and insights |
| `dashboard_screenshot.png` | Static preview of the final dashboard |
| `Superstore.csv` | Dataset used (or see Kaggle link above if omitted for size) |

## Tools Used
- Power BI Desktop
- Power Query Editor
- DAX

## Outcome
Learned how to clean real-world data, build calculated measures, and design an interactive, stakeholder-ready dashboard that surfaces sales and profitability trends at a glance.
