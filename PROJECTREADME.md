![Screenshot 2024-11-04 214723](https://github.com/user-attachments/assets/fbe7568a-bf12-49ea-b011-af76d3a45c5b)
## LITA_PROJECT
### OVERVIEW
This project conducts an in-depth analysis of sales Performance for a Retail Store  encompassing various Regions, product types, quantity sold, Order ID, Customer ID, Order date, and unit prices. The primary objective is to derive actionable insights on retrieving each product category's total sales, find the number of sales transactions in each region, find the highest-selling product by total sales value, calculate total revenue per product, calculate monthly sales totals for the current year, find the top 5 customers by total purchase amount, calculate the percentage of total sales contributed by each region, identify products with no sales in the last quarter. The goal is to produce an interactive Power BI dashboard that highlights these findings. 

### DATA COLLECTED
The dataset includes the following key column
1. Order ID
2. Customer ID
3. Product
4. Region
5. Order Date
6. Quantity
7. Unit price

### PROJECT OBJECTIVE
This project aims to address the following analyses:
1. Total Sales Revenue: Calculate the total sales revenue by multiplying the quantity by  price per unit to understand the overall sales performance.
2. Sales Trends Over Time: Use the date columns to analyze sales trends over different months, to identify peak and periods of low sales.
3. Region Performance Comparison: Compare sales across different 	regions to determine which locations are performing better. This can help identify top-performing branches and those that may need additional support.
4. Product Performance: Determine which products generate the most revenue or are sold most frequently using the product column. This can help in managing inventory and marketing efforts.
5. Top-Selling Products: Identify which products are sold most frequently (unit sold) to maintain adequate stock levels of materials.
6. Slow-Moving Inventory: Spot products with low sales that may require special promotions.
7. Branch-Level Stock Analysis: Understand which branches sell particular products faster and require frequent restocking of material.

### KEY METRICS
1. Total Revenue: This represents the overall income generated from sales, calculated as the sum of the revenue column.
2. Total Units Sold: This denotes the cumulative number of units sold, obtained by summing the units sold column.
3. Sales Growth Rate: This measures the percentage increase in sales revenue over a specific period (e.g., month-over-month, year-over-year).
4. Sales Performance Over Time: This involves analyzing trends over different time frames (daily, weekly, monthly) to identify peak sales periods.

### TOOLS AND METHODS
#### SPREADSHEET TOOL-EXCEL
The pivot table effectively summarizes total sales by product, region, and month, highlighting key trends. 
Additionally, Excel formulas are used to calculate average sales per product and total revenue by region, providing valuable insights into sales performance.![Screenshot 2024-11-04 214804](https://github.com/user-attachments/assets/a2910be5-fca9-4982-9b92-79718a942f9e)
![Screenshot 2024-11-04 214723](https://github.com/user-attachments/assets/9ac67167-8cb4-4840-bea1-ac7e9b044003)


	
#### STRUCTURED QUERY TOOL-SQL
SQL (Structured Query Language) was used to extract and analyze data from the retail store dataset.
1. Retrieve Total Sales for Each Product Category
Use SUM(sales_amount) to calculate total sales.
2. Group by category to get totals for each unique category.
Find the Number of Sales Transactions in Each Region
3. Use COUNT(*) to count all transactions.
Group by region for totals by region.
4. Find the Highest-Selling Product by Total Sales Value
Calculate total sales per product.
Use ORDER BY
5. Calculate Total Revenue per Product
Use SUM(sales_amount) and group by product_name.
6. Calculate Monthly Sales Totals for the Current Year
Filter by current year using WHERE.
Extract month with EXTRACT(MONTH FROM sale_date) and group by month.
7. Find the Top 5 Customers by Total Purchase Amount
Sum sales by customer_id.
Order by total in descending orde
8. Calculate the Percentage of Total Sales Contributed by Each Region
First, calculate regional sales using SUM.
Then divide by total sales using a subquery.
![Screenshot 2024-11-04 214853](https://github.com/user-attachments/assets/0fcd1714-7e54-40a0-aff7-a3cd46493203)![Screenshot 2024-11-04 214916](https://github.com/user-attachments/assets/60119811-7a54-4fe0-8318-40567106dfbe)


#### Data Preparation and Cleaning with Power Query
- Data Import: Import data from Excel
- Data Cleaning: Ensure unique records by removing duplicates, excluding irrelevant data through row filtering, and replacing or removing missing values if necessary.
- Data Transformation: Ensure consistency by changing data types (e.g date, number, text) and improving data structuring by merging columns.
- Data Normalization: Establish relationships between tables by defining primary and foreign keys.

#### Data Modeling
- Establish Relationships: Enable efficient querying and accurate visualizations by creating relationships between tables (one-to-many, many-to-many).
- Build a Date Table: Create a Date table with columns like Year, Quarter, Month, Day, etc., and relate it to the main data for time-based calculations (e.g., year-to-date, month-to-date).
- Use Star Schema or Snowflake Schema: Connect a sales fact table to dimension tables (e.g. Sales table linked to Product, Region, and Date tables).

#### CALCULATION AND ANALYSIS WITH DAX (Data Analysis Expressions)
- Creating Measures and Calculated Columns:
- Measures: Empower dynamic calculations based on report filters (e.g. total revenue, total quantity, and transaction).
- Calculated Columns: Utilize static calculations that don’t change based on report filters (e.g. Revenue, Day of week, Period of day).
- FORMULA USED:
- Revenue Calculation: Revenue = SUM(Sales[Quantity]) * SUM(Sales[Price per Unit])
- Total revenue: SUM('Sales Fact'[Revenue])
- Total of quantity: SUM('Sales Fact'[Quantity])
- Total orders: COUNT('Sales Fact'[Orders ID])

#### DATA VISUALIZATION
- Bar/Column Charts: Effectively compare quantities across categories.
- Line Charts: Clearly display trends over time.
- Donut Charts: Provide insights into percentage distribution.
- Tree Map: Offer detailed data views.
- Using Slicers and Filters: Enhance user-driven filtering by adding slicers (e.g., Region).
  ![Screenshot 2024-11-04 214647](https://github.com/user-attachments/assets/e975e967-ed75-4f64-b77f-9d5f890c5cc0)

   
#### RECOMMENDATIONS
1.	Focus on Region-specific strategies
The best-selling Region should have a meeting to speak on how they make large sales and what they do differently
2.	Optimize operations by time of day
More hands-on deck on Tuesday and Thursday since there’s a higher purchase at that time
3.	Promote top-selling Product
Put in more Revenue in the top-selling pizza to generate more Revenue
4.	Revamp, Promote or Remove the least-selling pizza
A sort of promo to the least product to boost the revenue and review the product.
5.	Day-of-the-week promotions
 A promo for Monday and Friday to boost sales or have a discount during those days.
