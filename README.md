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

> Replace these with real results from your queries.

- **Discounts:** The categories with the highest average discount are ______ and ______ (Q5).
- **Stock-outs:** ___ high-MRP products (above ₹300) are out of stock, mostly in ______ (Q2).
- **Inventory value:** ______ holds the highest estimated inventory value at ₹______ (Q3).
- **Value for money:** ______ gives the lowest price per gram (Q6).
- **Data quality:** ___ rows had a price of 0 and were removed during cleaning.



## Repository Structure

```
zepto-inventory-sql-analysis/
├── Zepto_inventory_analysis.sql
└── README.md
```



**Mahim A G**
BBA Finance & Analytics graduate | Aspiring Data Analyst
[LinkedIn](https://www.linkedin.com/in/mahim-ghori-00b241262/)
