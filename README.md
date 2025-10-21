🎯 Sales Performance Dashboard – Regional Insights
📘 Project Overview

This Power BI case study focuses on analyzing sales performance, profitability, and target achievement for GlobalTrend Retail Pvt. Ltd., a company selling consumer electronics — Mobiles, Laptops, and Accessories — across four major regions of India: North, South, East, and West.

The goal of this dashboard is to provide actionable insights into sales trends, profit margins, target achievement by salesperson, and product performance, helping management make data-driven business decisions.

🧠 Business Scenario

As a Business Intelligence Analyst, I was tasked with designing a Power BI dashboard that visualizes and answers key business questions:

What are the total sales, revenue, and profit across regions?

Which products and regions contribute the most to profitability?

Are salespersons achieving their sales targets?

How do sales and profits trend month-over-month?

Which products perform best in each region?

🧩 Data Sources
File	Description
sales_data.xlsx	Contains 100 sales transactions with fields like Date, ProductID, SalespersonID, Quantity, Unit Price, Discount, and Region
salespersons.xlsx	Details of each salesperson (Name, Joining Date, Region, Target)
products.xlsx	Product details (Product Name, Category, and Cost Price)

All datasets were clean and properly related in Power BI through relationships using:

ProductID

SalespersonID

Region

📊 Key Measures & DAX Calculations

To derive insights, several DAX measures were created:

Measure	Formula / Logic	Purpose
Total Sales	SUMX(Sales, Sales[Quantity] * Sales[Unit Price] * (1 - Sales[Discount]))	Calculates total sales revenue
Total Profit	SUMX(Sales, (Sales[Unit Price] - RELATED(Products[Cost Price])) * Sales[Quantity])	Calculates profit amount
Profit Margin %	DIVIDE([Total Profit], [Total Sales]) * 100	Shows profitability ratio
Target Achievement %	DIVIDE([Total Sales], SUM(Salespersons[Target])) * 100	Compares sales vs. targets
Total Transactions	COUNTROWS(Sales)	Tracks total sales transactions
📈 Dashboard Visualizations
Visualization	Purpose / Insight
Clustered Column Chart	Compare Total Sales & Total Profit by Region
Line Chart	Monthly trends in Sales and Profit
Bar Chart	Top 3 Products by Total Sales
KPI / Card Visuals	Display Total Sales, Total Profit, Profit Margin %, Target Achievement %
Gauge Visual	Show Target Achievement % for each Salesperson
Matrix / Table	Show Sales, Profit, and Target Achievement by Salesperson and Region
💡 Key Insights

Highest Sales Region: South — driven by strong mobile and laptop sales.

Most Profitable Category: Laptops generated the highest profit margin.

Top Performer: Priya (SP05) exceeded her sales target with ~246% achievement.

Lowest Performing Region: East region underperformed compared to others.

Trend Observation: Significant sales spike in March and April 2024, indicating seasonal demand.

🧮 Business Impact

This dashboard enables the management team to:

Monitor regional and individual performance effectively

Identify profitable product lines

Improve target setting for salespersons

Optimize inventory and marketing for high-performing regions

🧰 Tools & Skills Used

Power BI – Data modeling, DAX measures, and dashboard design

Excel – Data verification and preprocessing

Data Modeling – Relationship creation between multiple tables

Business Analytics – Translating raw sales data into performance insights

🗂️ Project Files
File	Description
SalesPerformanceDashboard.pbix	Power BI Dashboard file
Retail_Sales_Data.xlsx	Dataset used for analysis
Case_Study_Summary.docx	Written project summary
README.md	Project documentation
🧭 Future Improvements

Add Year-over-Year growth comparisons

Integrate live data refresh via Power Query

Add region-level drill-through pages for deeper insights
