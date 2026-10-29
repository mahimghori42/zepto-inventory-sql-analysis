# Zepto Inventory Analysis (SQL)

An end-to-end SQL analysis of a Zepto (quick-commerce) product inventory dataset using **PostgreSQL**. The project covers data exploration, data cleaning, and eight business questions on pricing, discounts, stock availability, and category performance.

## Objective

Quick-commerce platforms depend on pricing, discounting, and stock availability. This project uses SQL to answer questions such as:

- Which products carry the biggest discounts?
- Which high-value products are out of stock?
- Which categories hold the most inventory value and weight?
- Which products give the best value per gram?

## Dataset

- **Source:** [Zepto inventory dataset on Kaggle](ADD-LINK-HERE)
- **Table:** `zepto`

| Column | Description |
|---|---|
| `sku_id` | Unique product ID (primary key) |
| `category` | Product category |
| `name` | Product name |
| `mrp` | Maximum retail price (originally in paise) |
| `discountPercent` | Discount percentage |
| `availableQuantity` | Units available in stock |
| `discountedSellingPrice` | Selling price after discount (originally in paise) |
| `weightInGms` | Product weight in grams |
| `outOfStock` | Whether the product is out of stock |
| `quantity` | Units per pack |

## Tools Used

- PostgreSQL
- SQL: `GROUP BY`, `HAVING`, `CASE`, aggregate functions, `DISTINCT`, `ROUND`, `UPDATE`, `DELETE`

## Project Steps

### 1. Data Exploration
- Counted total rows
- Checked for null values across all columns
- Listed distinct product categories
- Compared in-stock vs out-of-stock products
- Found product names that appear under multiple SKUs

### 2. Data Cleaning
- Found products with a price of 0 and deleted rows where `mrp = 0`
- Converted `mrp` and `discountedSellingPrice` from paise to rupees

> Note: the paise-to-rupees `UPDATE` should be run only once.

### 3. Business Questions

| # | Question |
|---|---|
| Q1 | Top 10 best-value products by discount percentage |
| Q2 | High-MRP products (above ₹300) that are out of stock |
| Q3 | Estimated inventory value for each category |
| Q4 | Products with MRP above ₹500 and discount below 10% |
| Q5 | Top 5 categories with the highest average discount |
| Q6 | Price per gram for products of 100g or more, sorted by best value |
| Q7 | Grouping products into Low / Medium / Bulk by weight |
| Q8 | Total inventory weight per category |

## Key Findings

## What This Analysis Answers

- **Discounts:** Identifies the products and categories offering the highest discounts (Q1, Q5).
- **Stock-outs:** Flags high-MRP products (above ₹300) that are out of stock, showing where availability gaps hurt most (Q2).
- **Inventory value:** Estimates the value of stock held in each category (price × available quantity) to show where most capital is tied up (Q3, Q8).
- **Value for money:** Compares price per gram to find the best-value products (Q6).
- **Data quality:** Removed rows with an MRP of 0 and converted prices from paise to rupees so the analysis is reliable.










**Mahim A G**
BBA Finance & Analytics graduate | Aspiring Data Analyst
[LinkedIn](https://www.linkedin.com/in/mahim-ghori-00b241262/)
