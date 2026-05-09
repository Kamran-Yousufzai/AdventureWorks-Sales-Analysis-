🚲 AdventureWorks Sales Analysis Project
📋 Project Overview
This project involves building a comprehensive Business Intelligence solution for AdventureWorks, a global manufacturing company. The goal is to transform raw sales, product, customer, and returns data into an interactive dashboard that tracks Key Performance Indicators (KPIs), analyzes regional performance, and identifies product trends.

🛠️ 1. Data Transformation (Power Query)
Before modeling, raw CSV files were processed to ensure data integrity and high performance:

🧹 Data Cleaning: Handled missing values and corrected data types (e.g., Dates, Currency).

🌿 Conditional Columns: Created custom segments for products and regional categories to enhance filtering.

📅 Calendar Table: Generated a dynamic Calendar Lookup table to support advanced Time Intelligence calculations.

🏗️ 2. Data Modeling (Star Schema)
The project follows a Star Schema design to optimize performance and ensure accurate filter propagation.

📈 Fact Tables: Sales Data and Returns Data (containing quantitative data).

🗂️ Dimension Tables: Product Lookup, Customer Lookup, Territory Lookup, and Calendar Lookup.

🔗 Relationships: Established 1:Many relationships from Dimension tables to Fact tables, ensuring a consistent one-way filter flow.

🧮 3. DAX Calculations (Measures)
The following business logic was implemented using DAX to drive the report's visual analytical depth:

💰 Sales & Quantity Metrics
💵 TOTAL REVENUE (ITERATOR): Calculates total sales by multiplying quantity and price at the row level.

📦 QTY Sold: Aggregates the total number of items sold.

👤 Unique customer: Counts distinct customer keys to track business reach.

📈 Average revenue per customer: Ratio of total revenue to the unique customer count.

💳 Profit & Cost Analysis
💸 Total cost: Sums the product of quantity sold and product cost across all sales.

💎 Total profit: The net difference between Revenue and Total Cost.

🏷️ Average retail price: The mean price of products across the entire catalog.

📑 Order Logic & Filtering
📋 All orders: Calculates the total count of distinct sales orders, ignoring specific filters.

🚚 Bulk orders: Filters sales to include only transactions where the quantity is greater than one.

🎟️ High ticket orders: Identifies orders for products priced above the Overall Average Price.

📊 % of total orders: Shows the proportion of specific orders against the entire dataset.

🔄 Returns Analysis
🔙 Return QTY: Total units returned by customers.

🌎 All returns: Total return count across the entire dataset (context-independent).

📉 % of all returns: The percentage of returns contributed by specific categories.

⏳ Time Intelligence & Trends
📆 YTD SALES: Cumulative sales tracking from the start of the current year.

⏪ Previous month metrics: A suite of measures (Sales, Profit, Orders, Returns) comparing current data to the prior month.

🌊 10-day Rolling Revenue: Uses DATESINPERIOD to create a moving revenue window for trend smoothing.

🎯 Target Tracking
🚩 Target Gaps: Variance measures for Revenue, Profit, and Orders to compare actual performance against business goals.

🎨 4. Key Features & Visualizations
👑 Executive Summary: High-level KPIs for Revenue, Profit, and Returns at a glance.

🔍 Product Detail: Deep dive into specific product performance and "High Ticket" items.

👥 Customer Analysis: Identifying top-tier customers and average revenue per user.

🗺️ Geospatial Mapping: Visualizing sales volume across different global territories.

🎛️ Interactive Slicers: Dynamic filtering by date, region, and product category.

🚀 5. Conclusion
This end-to-end Power BI project provides AdventureWorks with a powerful tool to track its global footprint, monitor real-time margins, and understand return rates, ultimately enabling data-driven decision-making.
