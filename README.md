
📊 Sales & Revenue Analysis Dashboard

An interactive Sales & Revenue Analysis Dashboard built in Power BI, analyzing retail transaction data to track KPIs, uncover regional and product performance trends, and support data-driven business decisions.

🎯 Project Overview

This project analyzes ~10,000 retail order records (the "Superstore" dataset) to answer key business questions around revenue performance, profitability, and customer/product trends. It was built end-to-end — from raw CSV data cleaning to a fully interactive, multi-visual Power BI report — to demonstrate practical data analysis and dashboard design skills.

🎯 Business Problems Addressed

What are the overall Sales, Profit, Profit Margin, and Order volume?
How does revenue trend over time, and is there seasonality?
Which products and categories drive the most revenue?
Which U.S. states/regions generate the highest sales?
How do Customer Segments (Consumer, Corporate, Home Office) differ in performance?
Can a non-technical stakeholder filter and explore the data themselves?

🛠️ Tools Used

Power BI Desktop — data modeling, DAX, visualization
Power Query — data cleaning and transformation
DAX (Data Analysis Expressions) — custom KPI measures
Star Schema Data Modeling — dedicated Date table with relationships

🗂️ Dataset

Source: Superstore Dataset – Kaggle
Size: 9,994 order line items, 5,009 unique orders, spanning 2014–2017
Fields: Order Date, Ship Date, Customer Segment, Region, State, City, Category, Sub-Category, Product Name, Sales, Quantity, Discount, Profit

🧹 Data Preparation

Cleaned and validated the full 9,994-row transactional dataset in Power Query (data type corrections, locale-based date parsing, blank/error handling via column profiling).
Removed non-analytical fields (e.g. Row ID).
Built a dedicated Date table using DAX (CALENDAR()), marked as an official Date table, and connected it to the sales table via a one-to-many relationship — enabling accurate time-intelligence calculations.

Before vs. After Cleaning:

Raw dataset (as downloaded): 9,994 rows — included ambiguous US-format dates and an unneeded index column.
After initial (incorrect) cleaning: 2,739 rows — a locale mismatch during date conversion caused ~73% of rows to error out, which were then accidentally dropped.
After corrected cleaning: 9,994 rows — fixed by re-parsing dates with an explicit US locale before any error-removal step, preserving every valid record.

📐 KPI Measures (DAX)

Total Sales — SUM(Sales) — overall revenue
Total Profit — SUM(Profit) — overall profitability
Profit Margin % — Profit as a percentage of Sales
Total Orders — distinct order count (not row count)
Avg Order Value — revenue per order
YoY Sales Growth % — year-over-year revenue growth using SAMEPERIODLASTYEAR

🔍 Analysis & Visuals

KPI Cards — Total Sales, Total Profit, Profit Margin %, Total Orders at a glance
Sales Trend Line Chart — Year → Quarter → Month drill-down to reveal seasonality
Top 10 Products Bar Chart — dynamically ranked by revenue
Category Breakdown Donut Chart — revenue share by Furniture / Office Supplies / Technology
Regional Sales Map — U.S. states shaded by sales volume
Interactive Slicers — Region, Category, Segment, and Date, fully cross-filtering every visual

💡 Key Insights

Total Sales: $2,297,201 | Total Profit: $286,397 | Profit Margin: 12.5% | Total Orders: 5,009 | Avg Order Value: $458.61
The West region led all regions in sales ($725.5K), followed by East ($678.8K) — South lagged furthest behind ($391.7K).
Technology was the top-performing category by revenue ($836.2K), ahead of Furniture ($742.0K) and Office Supplies ($719.0K).
Phones and Chairs were the top-selling sub-categories, each generating over $328K in sales.
Sales follow a clear upward seasonal trend through the year, peaking in Q4 (~$878K) — nearly 2.5x higher than Q1 (~$360K), consistent with holiday-season demand.
The Consumer segment generated the most revenue ($1.16M) — more than Corporate and Home Office combined.
California and New York are the top two states by sales, together contributing over $768K.

📷 Dashboard Preview

dashboard overview.png

🚀 How to View
1. Download Sales_Revenue_Dashboard.pbix
2. Open it in Power BI Desktop (free)
3. Use the slicers on the report to explore Region, Category, Segment, and Date filters interactively

📈 Skills Demonstrated

Data cleaning · Data modeling (star schema) · DAX measures & time intelligence · Data visualization · KPI design · Interactive filtering · Business insight generation


