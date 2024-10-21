# Walmart-Sales-Analysis


### Walmart Sales Data Analysis

#### Overview

This project examines Walmart's sales data to identify top-performing branches and products, analsze sales trends, and understand customer behavior. The goal is to find ways to improve and optimise sales strategies. The dataset was sourced from the Walmart Sales Forecasting Competition on Kaggle.

> In this competition, participants were provided with historical sales data for 45 Walmart stores in different regions. Each store has several departments, and participants needed to forecast sales for each department. Additionally, holiday markdowns in the dataset added a challenge, as they affect sales unpredictably across departments.

#### Project Purpose

The main goal is to analsze Walmart’s sales data to uncover factors that influence the performance of different stores and products.

#### Dataset Information

The dataset, from the Walmart Sales Forecasting Competition on Kaggle, contains sales transactions from three Walmart branches located in Mandalay, Yangon, and Naypyitaw. It includes 17 columns and 1000 rows:

| Column              | Description                                      | Data Type         |
|---------------------|--------------------------------------------------|-------------------|
| invoice_id          | Sales invoice ID                                 | VARCHAR(30)       |
| branch              | Branch where sales occurred                      | VARCHAR(5)        |
| city                | City of the branch                               | VARCHAR(30)       |
| customer_type       | Type of customer                                 | VARCHAR(30)       |
| gender              | Customer's gender                                | VARCHAR(10)       |
| product_line        | Product category                                 | VARCHAR(100)      |
| unit_price          | Price of each product                            | DECIMAL(10, 2)    |
| quantity            | Number of items sold                             | INT               |
| VAT                 | Tax on the purchase                              | FLOAT(6, 4)       |
| total               | Total cost including VAT                         | DECIMAL(10, 2)    |
| date                | Date of purchase                                 | DATE              |
| time                | Time of purchase                                 | TIMESTAMP         |
| payment_method      | Payment method used                              | DECIMAL(10, 2)    |
| cogs                | Cost of Goods Sold                               | DECIMAL(10, 2)    |
| gross_margin_percent| Gross margin percentage                          | FLOAT(11, 9)      |
| gross_income        | Total gross income                               | DECIMAL(10, 2)    |
| rating              | Customer rating                                  | FLOAT(2, 1)       |

#### Analysis Goals

- **Product Analysis:** Investigate product categories, identify top sellers, and pinpoint areas for improvement.
- **Sales Analysis:** Examine sales trends to evaluate the effectiveness of sales strategies and suggest improvements.
- **Customer Analysis:** Understand customer segments, their purchasing habits, and profitability.

#### Approach

1. **Data Cleaning:** Identify and address missing or NULL values.
2. **Database Setup:** Create tables, insert data, and ensure no NULL values by setting constraints.
3. **Feature Engineering:** Create new columns such as:
   - **time_of_day** (Morning, Afternoon, Evening) to see when most sales occur.
   - **day_name** (Mon-Fri) to track which days are busiest for each branch.
   - **month_name** (Jan-Dec) to identify high-sales months.
4. **Exploratory Data Analysis (EDA):** Explore the data to answer key questions and achieve project goals.

#### Key Questions to Answer

**General**
- How many cities are represented in the dataset?
- Which branch is in each city?

**Product**
- How many product categories are there?
- Which payment method is most common?
- What are the top-selling products?
- Which month generated the highest revenue?
- What city brings in the most revenue?

**Sales**
- How do sales vary by time of day?
- Which customer type generates the most revenue?
- Which city has the highest tax percentage?

**Customer**
- What are the most common customer types?
- What is the gender distribution by branch?
- When do customers leave the most ratings?

#### Revenue and Profit Calculations

- **COGS (Cost of Goods Sold) = Unit Price × Quantity**
- **VAT = 5% × COGS**
- **Total (Gross Sales) = VAT + COGS**
- **Gross Profit = Total - COGS**
- **Gross Margin = (Gross Profit / Total Revenue) × 100**

**Example Calculation:**

- **Unit Price** = $45.79
- **Quantity** = 7
- **COGS = 45.79 × 7 = $320.53**
- **VAT = 5% × 320.53 = $16.03**
- **Total = $320.53 + $16.03 = $336.56**
- **Gross Margin = ($16.03 / $336.56) ≈ 4.76%**

This analysis provides insights into sales performance and helps develop more effective business strategies.
