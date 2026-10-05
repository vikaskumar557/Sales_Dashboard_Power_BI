# Sales_Dashboard_Power_BI

1. Project Introduction

Project Name: Sales_Dashboard_Power BI

This project analyzes sales, profit, cost, and business performance using an interactive Power BI dashboard. It transforms raw data from multiple sources into meaningful insights to support data-driven business decisions.

Project Objectives
Analyze Total Sales, Total Profit, and Total Cost.
Understand monthly sales and profit trends.
Compare business performance across countries and cities.
Analyze store manager and product performance.
Evaluate quantity distribution and order delivery.
Identify sales trends and support better business decisions.

## 2. Key Technologies Used

📊 **Power BI Desktop:** Used to develop interactive reports, dashboards, and visualizations.
🔄 **Power Query Editor:** Used for data cleaning, transformation, and preparation.
🧮 **DAX (Data Analysis Expressions):** Used to create measures, calculate KPIs, perform conditional analysis, and analyze time-based trends.
🗂️ **Data Modeling:** Used to establish relationships between sales data and supporting tables.
📈 **Data Visualization:** Used KPI cards, charts, maps, tables, and slicers to present business insights.
📁 **File Formats:** Used `.pbit` for the Power BI template and `.pbix` for the working report file.

3. Data Connection in Power BI

In this project, I connected multiple data sources to Power BI Desktop using different file formats.

Product Details.txt: Imported product information for product-wise sales and profit analysis.
Other Detail.xlsx: Imported customer, sales region, store, and location details from Excel worksheets.
Sales Trans demo.txt: Imported sales transaction data for analyzing sales and business performance.
Sales Emp Details.pdf: Extracted sales employee information from PDF tables.
StoreInfo.accdb: Connected to a Microsoft Access database to import store-related information.
 kiya matlab ha iska 

4. Data Cleaning and Transformation in Power Query

I used Power Query Editor to clean and prepare the data before loading it into the Power BI data model.

4.1 Product Details.txt
Promoted the first row to headers.
Removed blank rows.
Replaced category values where required.
Corrected column data types.
Removed duplicate records.
4.2 Other Detail.xlsx
Imported data from multiple Excel sheets.
Promoted headers and removed blank rows.
Corrected column data types.
Removed duplicate records.
Renamed columns for better understanding.
4.3 Sales Emp Details.pdf
Extracted employee information from PDF tables.
Promoted headers and removed blank rows.
Checked and removed duplicate employee codes.
Prepared employee data for reporting.
4.4 Sales Trans demo.txt
Imported comma-separated transaction data.
Removed blank rows and error records.
Removed duplicate records where applicable.
Corrected date and numeric data types.
4.5 StoreInfo.accdb
Connected to the Access database.
Imported store-related information.
Removed duplicate records and blank rows.
Replaced null values where appropriate.
5. Append and Merge Queries
5.1 Append Queries

I used Append Queries to combine the Sales Transactions 2012–2019 and Sales Transactions 2017–2022 tables into a single table named ALL DATA.

This process combined transaction records with the same column structure into one table for consolidated sales analysis.

5.2 Merge Queries

I used Merge Queries to combine the ALL DATA table with the Product Details table using the Product Code column.

Join Type: Left Outer Join
Matching Column: Product Code
Purpose: To bring relevant product information into the sales transaction data.

This helped connect transaction records with product details for product-wise sales and profit analysis.

5. Data Modeling

I used Power BI Model View to organize the main sales table and supporting tables.

Established relationships between the sales table and Product, Customer, Store, Sales Region, Employee, and Date tables using common columns.
Connected the Transaction Date column with the Date Table for time-based analysis.
Organized DAX measures in a separate measure table for easier management.
Used the data model to support interactive filtering and analysis across different business dimensions.

6. DAX Implementation

I used DAX (Data Analysis Expressions) to create measures and calculations for business performance analysis.

6.1 Basic Measures

Created measures for:

Total Sales
Total Cost
Total Profit
Total Quantity
Average Quantity
Maximum and Minimum values
Delivered Orders
6.2 DAX Functions Used
SUM and SUMX: Used to calculate totals and row-wise aggregations.
AVERAGE, MAX, and MIN: Used for average, maximum, and minimum calculations.
RELATED: Used to retrieve related product prices and costs through established relationships.
CALCULATE: Used to evaluate measures under specific filter conditions.
FILTER: Used to apply conditions to data.
ALL and ALLSELECTED: Used for comparative and percentage-based analysis.
IF: Used to classify CPU performance based on specified conditions.
6.3 Time Intelligence

Used the following time intelligence functions to analyze sales over different periods:

TOTALMTD – Month-to-date analysis.
TOTALQTD – Quarter-to-date analysis.
TOTALYTD – Year-to-date analysis.
PREVIOUSMONTH – Previous-month comparisons.
6.4 Delivery-Date Analysis

Used USERELATIONSHIP to perform delivery-date-based analysis where an inactive relationship between the delivery date and the Date Table was available.

These DAX calculations helped analyze business performance across categories, products, and time periods.

7. Power BI Visualizations

I created the following visualizations to present sales data in an interactive and understandable format.

7.1 KPI Cards

Displayed Total Sales, Total Profit, Total Cost, Quantity, Average, and Delivered Orders to provide a quick overview of business performance.

7.2 Line and Clustered Column Chart

Compared monthly sales and profit trends to identify changes in performance over time.

7.3 Filled Map

Visualized geographical sales performance by country to compare sales across different markets.

7.4 Funnel Chart

Compared product-wise profit contributions to identify products contributing more or less to total profit.

7.5 Pie Chart

Displayed quantity distribution by customer gender to understand the proportion of quantities associated with different gender categories.

7.6 Table Visual

Displayed Product Category, Total Sales, Total Profit, Quantity, Average, and Total Cost in a structured tabular format.

7.7 Q&A Visual

Enabled users to explore data by entering questions in natural language and view answers as supported visualizations.

7.8 Decomposition Tree

Analyzed Total Sales by Country, State, City, Store Manager, and Store Name to explore sales performance at different levels.

7.9 Key Influencers

Analyzed factors associated with Total Sales, including Country and Product Name, to identify patterns linked to higher or lower sales.

8. Interactive Filters and Slicers

I added interactive slicers and filters to make the dashboard dynamic and user-friendly.

Year Slicer: Filters sales data by year.
Country Slicer / Buttons: Allows users to explore sales performance by country.
City Slicer: Filters the dashboard for selected cities.
Store Manager Slicer: Enables analysis of sales performance by store manager.

These interactive controls allow users to explore business performance according to their selected criteria.

