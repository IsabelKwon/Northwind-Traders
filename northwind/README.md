# Northwind Traders SQL Analysis

## About

This project is based on a Dataquest guided project, using their provided database schema and starter questions as a foundation. Beyond the original prompts, I extended the analysis further whenever a result raised a new question — for example, smoothing noisy month-over-month growth rates with a 3-month moving average, or visualizing customer order distributions with Python (pandas and matplotlib) to better understand patterns that weren't obvious from the SQL output alone.

## Tools

- **PostgreSQL** — database (Northwind sample dataset)
- **SQL** (via [JupySQL](https://jupysql.ploomber.io/)) — querying, CTEs, window functions
- **Python** (pandas, matplotlib) — data visualization and further exploration

## What's covered

- Combining customers, orders, and order details into reusable views
- Ranking employees by total sales, overall and within job title
- Monthly sales trends: running totals, month-over-month growth rate, and a 3-month moving average to reduce noise
- Visualizing growth rate trends with matplotlib
- Customer order frequency vs. average, and what the distribution shape reveals about customer segments

## Files

- `northwind_query.ipynb` — main analysis notebook (SQL queries, explanations, and Python visualizations)
- `northwind.sql` — database schema/seed data

## Status

Work in progress — this notebook grows as new questions come up during analysis.
