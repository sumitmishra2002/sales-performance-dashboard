# Sales Performance Dashboard (Power BI)

## Project Overview
This project presents an interactive Sales Performance Dashboard built using Power BI to analyze sales trends and performance across multiple dimensions. The dashboard helps in identifying key business insights such as top-performing regions, products, and revenue trends over time.

## Objectives
- Monitor overall sales performance
- Track regional and product-wise sales
- Analyze monthly revenue trends
- Evaluate YoY growth and contribution metrics

## Tools & Technologies
- Power BI Desktop
- DAX
- Microsoft Excel / CSV
- Data Visualization Techniques

## Key Features
- Interactive KPI Cards (Total Sales, Total Profit, Profit Margin, YoY Growth)
- Monthly Sales Trend Analysis
- Region-wise and Product-wise Performance
- Drill-through Pages for Detailed Analysis
- Contribution Analysis using DAX
- Dynamic Filters and Slicers

## Files Included
- `/pbix/Sales_Performance_Dashboard.pbix` – Full Power BI dashboard file  
- `/data/Large_Sales_Data_for_PowerBI.csv` – Dataset used  
- `/screenshots/` – Dashboard preview images  

## Sample DAX Measures
```DAX
Total Sales = SUM(Sales[Revenue])
Total Profit = [Total Sales] - SUM(Sales[Cost])
YoY Growth % = DIVIDE([Total Sales] - [Sales LY], [Sales LY])
Product Contribution % =
DIVIDE([Total Sales], CALCULATE([Total Sales], ALL(Sales[Product])))
