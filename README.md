# Customer Shopping Behavior Analysis

An end-to-end data analytics project: cleaning raw retail transaction data in Python, answering business questions with SQL, and visualizing findings with Matplotlib.

## Overview

This project simulates a retail analytics workflow -- taking a raw customer transaction dataset and turning it into business insight through three stages:

1. **Data Preparation (Python / Pandas)** -- cleaning, imputing missing values, feature engineering (age groups, purchase frequency in days).
2. **Business Analysis (SQL / PostgreSQL)** -- 12 queries answering questions on revenue by segment, product performance, discount behavior, and customer loyalty.
3. **Visualization (Matplotlib)** -- charts translating query results into readable insight.

## Stack

Python, Pandas, PostgreSQL (Supabase), SQLAlchemy, Matplotlib, Jupyter Notebook

## Files

- `Customer_Shopping_Behavior_Analysis.ipynb` -- full workflow: load, clean, load to Postgres, query, visualize
- `customer_behavior_sql_queries.sql` -- all 12 SQL queries as a standalone script
- `customer_shopping_behavior.csv` -- source dataset
- `chart_*.png` -- exported visualizations

## How to Run

1. Clone the repo and install dependencies:
   ```bash
   pip install pandas sqlalchemy psycopg2-binary matplotlib jupyter python-dotenv
   ```
2. Create a Supabase project (or any Postgres instance) and grab the connection string from **Project Settings -> Database**.
3. Create a `.env` file in the project root (see `.env.example`) with your connection string in `SUPABASE_DB_URL`.
4. Open `Customer_Shopping_Behavior_Analysis.ipynb` and run all cells.
5. Or run the SQL directly against your loaded `customer` table using `customer_behavior_sql_queries.sql`.

## Key Findings

- Male customers accounted for roughly double the revenue of female customers in this dataset.
- Revenue is fairly evenly spread across age groups, with Young Adults and Middle-aged customers slightly ahead.
- Fall and Spring outperform Summer for total revenue -- likely a category mix effect (outerwear/layering vs. summer basics).
- Payment method has almost no effect on average spend per transaction -- not a useful segmentation variable on its own.
- Category leaders are stable: Jewelry/Sunglasses/Belts top Accessories, Pants/Blouses/Shirts top Clothing.

## Credit

Dataset and starting project structure adapted from a public MIT-licensed template ([source](https://github.com/amlanmohanty1/customer-trends-data-analysis-SQL-Python-PowerBI)); cleaning logic, SQL queries, visualizations, and findings are my own.
