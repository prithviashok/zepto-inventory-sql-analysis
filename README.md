🛒 Zepto Inventory Data Analysis (PostgreSQL)
📌 Project Overview

This project performs end-to-end data analysis using PostgreSQL on a simulated Zepto inventory dataset.

Zepto is a quick-commerce grocery delivery platform, where pricing, discounts, stock levels, and product assortment directly impact revenue and customer satisfaction.

The goal of this project is to explore how SQL can be used to:

Clean raw data
Perform exploratory analysis
Generate business insights
Answer real-world retail questions

This project is designed to showcase SQL skills for Data Analyst roles.

🧰 Tools & Technologies
PostgreSQL
SQL (Data Cleaning + Data Analysis)
Relational Database Design
🗄️ Dataset Description

The dataset contains inventory information for products sold on Zepto.

Column	Description
sku_id	Unique product identifier
category	Product category
name	Product name
mrp	Maximum Retail Price
discountPercent	Discount offered
availableQuantity	Units in stock
discountedSellingPrice	Selling price after discount
weightInGms	Product weight
outOfStock	Stock availability flag
quantity	Pack size
🔎 Project Workflow
1️⃣ Database Setup

Created a PostgreSQL table and loaded the dataset.

CREATE TABLE zepto(
sku_id SERIAL PRIMARY KEY,
category VARCHAR(120),
name VARCHAR(150) NOT NULL,
mrp NUMERIC(8,2),
discountPercent NUMERIC(5,2),
availableQuantity INTEGER,
discountedSellingPrice NUMERIC(8,2),
weightInGms INTEGER,
outOfStock BOOLEAN,
quantity INTEGER
);
🧹 Data Cleaning

Performed data quality checks and preprocessing:

Checked row counts and sample records
Identified NULL values
Removed products with invalid pricing (MRP = 0)
Converted paise → rupees for pricing columns
📊 Exploratory Data Analysis
Inventory Health
Total products in stock vs out of stock
Duplicate product names across SKUs
Unique product categories
Pricing & Discount Analysis
Top products with highest discounts
High MRP but out-of-stock products
Products with low discount but high price
Revenue Estimation

Calculated potential revenue by category:

SUM(discountedSellingPrice * availableQuantity)
💡 Key Business Questions Answered
🥇 Top 10 Best-Value Products

Identified products offering the highest discount percentages.

📉 Stock Risk Analysis

Products with high MRP but out of stock were identified as potential lost-revenue items.

💰 Category Revenue Potential

Estimated revenue contribution per category based on current inventory.

🏷️ Discount Strategy Insights

Top 5 categories offering the highest average discounts.

⚖️ Value for Money Analysis

Calculated price per gram to identify best-value products.

📦 Inventory Segmentation

Grouped products into:

Low weight
Medium weight
Bulk products
⚖️ Inventory Load Analysis

Calculated total inventory weight per category to understand warehouse load.

📈 Example Insights (What a business could learn)
Which categories generate the highest revenue
Where discount strategies are strongest/weakest
Which premium products frequently go out of stock
Best value products for promotional campaigns
Inventory distribution by weight and category
🎯 Skills Demonstrated
SQL Data Cleaning
Aggregations & Grouping
CASE Statements
Business KPI Calculations
Data Exploration Techniques
Real-world Retail Analytics Thinking
🚀 How to Run This Project
Open PostgreSQL / pgAdmin
Create a new database
Run the table creation script
Import dataset
Execute the SQL queries in order
👨‍💻 Author

Prithvi Ashok

Data Analyst | SQL | PostgreSQL | Data Analytics
