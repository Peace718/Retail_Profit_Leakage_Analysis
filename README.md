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

**Orders:** Contains detailed transactional records including: Order ID, Order Date, Ship Date, Ship Mode, Customer ID, Location ID, Product ID, Sales, Quantity, Discount, Profit.

**Customers:** 
-  Contains customer information including: Customer ID, Customer Name, Customer Segment.
-  Customer segments include: Consumer, Corporate, Home Office.

**Products:** 
-  Contains Product information including: Product ID, Product Name, Category, Sub-Category, Pricing Code.
- Product categories include: Technology, Office Supplies, Furniture.

## Tools and Technologies
- Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)
- Microsoft Excel

## Data Preparation and Cleaning
The following data preparation steps were completed:
1. Imported the Orders, Products, and Customers tables.
2. Promoted headers where required.
3. Verified data types across all columns.
4. Confirmed there were no missing or error values.
5. Reviewed column distributions and uniqueness.
6. Validated key fields used for relationships.
7. Created a Date Table for time intelligence analysis.
8. Created calculated columns for Discount Bands and custom sorting.

## Data Modeling
A star-schema data model was implemented to support efficient analysis and reporting.

![Data Model](images/data_model.png)

## DAX Measures and KPIs
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

## Dashboard Design
### Executive Overview
![Executive Overview](images/dashboard_page1.png)
### Profit Leakage Analysis
![Profit Leakage Analysis](images/dashboard_page2.png)
### Key Insights & Findings
![Key Insights & Findings](images/dashboard_page3.png)

## Key Insights & Findings

**Strong Sales, Modest Profitability: ** Despite generating strong sales revenue, the business achieved an overall profit margin of only **approximately 12.5%**, indicating that revenue growth did not translate into equally strong profitability.

**High Discounts Reduce Profit: ** Orders with discounts above **approximately 20%** were associated with declining profitability, with the highest discount bands generating negative total profit.

**Furniture Has the Lowest Profitability: ** Compared with Technology and Office Supplies, the **Furniture** category recorded significantly lower profit margins, suggesting opportunities to improve pricing and discount strategies.

**Tables and Bookcases Are Major Sources of Profit Leakage: ** Within the Furniture category, **Tables** and **Bookcases** contributed the most to financial losses and should be prioritized for corrective action.

## Recommendations
- Review and limit discounts above approximately 20% to reduce unnecessary profit erosion.
- Reassess pricing and promotional strategies for Tables and Bookcases, which are major contributors to profit leakage.
- Improve the profitability of the Furniture category by reviewing pricing, discount policies, and product offerings.
- Apply discounts strategically to balance revenue growth with sustainable profit margins.
- Continuously monitor discount levels and profitability using dashboards to support timely, data-driven decisions.

## Conclusion
This analysis demonstrates that strong sales performance alone does not guarantee healthy profitability. The findings show that excessive discounting and underperforming product categories contribute significantly to profit leakage, particularly within the Furniture category and its Tables and Bookcases sub-categories.
By adopting a more strategic approach to discounting and focusing on the products driving losses, management can improve profit margins while maintaining sustainable sales growth.

# Project Files

- Power BI Report (`.pbix`)
- Project Report (`.pdf`)
- Dataset (`.xlsx`)





















