# The Discount Trap: How Discounts Impact Retail Profitability
### A Power BI Analysis of Discount-Driven Profit Leakage and Profitability Improvement Opportunities

## Project Overview
This project investigates how discounting affects retail profitability using an interactive Power BI dashboard.
Although the business generates strong sales revenue, management is concerned that excessive discounting may be reducing profits across products and categories. The dashboard analyzes sales performance, profit trends, discount behavior, and product profitability to identify areas of profit leakage and support data-driven pricing decisions.

## Business Problem
A retail company generates strong sales revenue but is concerned that its discount strategy may be reducing overall profitability.
Management lacks visibility into how discount levels affect profit across product categories and sub-categories, making it difficult to identify where profit leakage occurs and which areas require corrective action.
The company needs an analytics solution to evaluate the relationship between discounts and profitability and support better pricing decisions.

## Project Objectives
The dashboard was designed to:
- Evaluate the relationship between discounts and profitability, that is, discount impact on profit.
- Identify products and categories contributing to profit leakage.
- Monitor key business performance indicators.
- Compare profitability across customer segments.
- Support evidence-based pricing and discount decisions.
- Provide actionable insights for improving overall profitability.

## Dataset Overview
The dataset represents a fictional retail company and is structured using multiple related tables designed to simulate real-world business data.
**Orders: ** Contains detailed transactional records including: Order ID, Order Date, Ship Date, Ship Mode, Customer ID, Location ID, Product ID, Sales, Quantity, Discount, Profit.
**Customers: ** 
-  Contains customer information including: Customer ID, Customer Name, Customer Segment.
-  Customer segments include: Consumer, Corporate, Home Office.
**Products: ** 
-  Contains Product information including: Product ID, Product Name, Category, Sub-Category, Pricing Code.
- Product categories include: Technology, Office Supplies, Furniture.

## Tools and Technologies
- Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)
- Microsoft Excel

# Data Preparation and Cleaning
The following data preparation steps were completed:
- Imported the Orders, Products, and Customers tables.
- Promoted headers where required.
- Verified data types across all columns.
- Confirmed there were no missing or error values.
- Reviewed column distributions and uniqueness.
- Validated key fields used for relationships.
- Created a Date Table for time intelligence analysis.
- Created calculated columns for Discount Bands and custom sorting.

## Data Modeling
A star-schema data model was implemented to support efficient analysis and reporting.
![Data Model](images/data_model.png)

# DAX Measures & KPIs
Key measures created include:
- Total Sales
- Total Profit
- Profit Margin (%)
- Average Discount (%)
- Order Count
- Loss Orders
- Loss-Making Orders (%)

### Profit Margin
```DAX
Profit Margin =
DIVIDE(
    [Total Profit],
    [Total Sales]
)
```

### Loss-Making Orders (%)
```DAX
Loss-Making Orders =
DIVIDE(
    [Loss Orders],
    [Order Count],
    0
)
```


















