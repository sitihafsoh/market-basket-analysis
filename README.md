# <h1 align="center"><b>Market Basket Analysis for Online Retail</b></h1>

## Project Overview

This project focuses on a Market Basket Analysis using the "Online Retail II" dataset. This dataset contains transaction data from a UK-based online retailer specializing in unique, all-occasion giftware. The primary goal of this analysis is to uncover relationships between different products sold by the retailer. By identifying which items are frequently purchased together, we can provide actionable insights for business strategies such as product placement, cross-selling campaigns, and personalized recommendations.

## Business Question

1. What items are most frequently bought together by our customers?
2. How do buying patterns change across different seasons?
3. Which products should be bundled or cross-promoted to maximize sales revenue?
4. How can we increase the number of items a customer buys in a single transaction?

## Dataset

The dataset used is the "Online Retail II" from the UCI Machine Learning Repository. It contains transaction data from a UK-based online retailer between 01/12/2009 and 09/12/2011.

**Variable Informations:**

- `InvoiceNo`: Invoice number. Nominal. A 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation.
- `StockCode`: Product (item) code. Nominal. A 5-digit integral number uniquely assigned to each distinct product.
- `Description`: Product (item) name. Nominal.
- `Quantity`: The quantities of each product (item) per transaction. Numeric.
- `InvoiceDate`: Invoice date and time. Numeric. The day and time when a transaction was generated.
- `UnitPrice`: Unit price. Numeric. Product price per unit in Pound Sterling (£).
- `CustomerID`: Customer number. Nominal. A 5-digit integral number uniquely assigned to each customer.
- `Country`: Country name. Nominal. The name of the country where a customer resides.

**Link Dataset:**

https://archive.ics.uci.edu/dataset/502/online+retail+ii

## Exploratory Data Analysis (EDA)

### 📈 Total Sales by Month (2009-2011)

Sales exhibit a predictable, strong seasonal cycle, peaking massively in November (Holiday preparation, $\text{£}260,713.96$)—the critical sales period. Secondary peaks consistently align with the beginning of each season (Winter, Spring, Summer kickoff). The lowest sales period is confirmed as February 2010 ($\text{£}94,705.60$), marking the slowest post-holiday lull.

