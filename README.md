# Global Sales and Profit Analysis

## Project Overview

This project analyzes global sales performance, profitability, and demand patterns across countries, regions, product categories, and time.

The analysis covers the full workflow: data cleaning, transformation, exploratory data analysis (EDA), and visualization to uncover key business insights.

## Business Problem

The goal of this analysis is to understand:

* What drives revenue and profit
* Which regions and countries are the most important for the business
* How product categories perform in terms of sales and profitability
* How demand changes over time (seasonality and trends)
* How operational factors (e.g., delivery time) may impact performance

## Data Sources

The project uses three main datasets:

* `countries` — country names, regions, and subregions
* `events` — order data (dates, sales channels, quantity, price, cost)
* `products` — product categories

## Data Preparation

Key steps:

* Handling missing values:

  * Country Code → filled with `"Unknown"`
  * Other missing values → removed due to low proportion
* Data type transformation:

  * Date fields converted to datetime format
* Duplicate check and removal
* Feature engineering:

  * Revenue = Units Sold × Unit Price
  * Profit = Units Sold × (Unit Price − Unit Cost)
  * Delivery time (days)

## Key Metrics

* Total revenue and total profit
* Average revenue and profit per order
* Total units sold
* Number of countries and product categories
* Delivery time metrics

## Analysis & Insights

### Product Performance

* Some categories generate high volume but lower profit margins
* Others are less popular but more profitable

### Geographic Analysis

* A small number of countries generate the majority of revenue and profit
* Europe dominates in overall performance
* Regional performance is uneven

### Sales Channels

* Offline channel slightly dominates
* Differences between channels are relatively small → balanced strategy is optimal

### Delivery & Operations

* Delivery time varies by category and region
* Longer delivery may increase operational costs
* Faster delivery can improve customer satisfaction

### Time & Seasonality

* Sales show clear seasonal patterns
* Growth dynamics differ across categories and regions
* Weekly patterns indicate intra-week seasonality for some products

## Conclusions

* Revenue ≠ profit → margins differ significantly across products
* Business relies on volume rather than high-margin transactions
* High-demand categories ensure stable cash flow
* Key markets should be prioritized for logistics and marketing
* Demand forecasting and seasonal strategy are critical
* Delivery optimization can improve both cost efficiency and customer experience

## Tools Used

* Python (Pandas, NumPy)
* Data visualization (Matplotlib, Seaborn)
* Google Colab

## Project Structure

* `sales_performance_analysis.ipynb` — full analysis notebook
* `README.md` — project description
