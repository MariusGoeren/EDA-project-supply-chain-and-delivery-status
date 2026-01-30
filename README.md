# exploring the delivery status using a supply chain dataset

## Table of Content
- [Project Overview](#Project-Overview)
- [Context & Intent](#Context-&-Intent)
- [Key Features](#Key-Features)
- [Main Insights](#Main-Insights)
- [Tools & Techniques](#Tools-&-Techniques)
- [Project Structure](#Project-Structure)

## Project Overview
This project explores the relationships between **delivery status** and **market/number of products per order**, using the public dataset [DataCo Supply Chain Dataset | kaggle.com | by Evil Spirit05](https://www.kaggle.com/datasets/evilspirit05/datasupplychain/data).
The analysis focuses on understanding how factors like the destination and the number of products ordered correlate with the delivery status, which means whether the packages will be delivered late, early, on time or if the delivery was cancelled.

## Context & Intent
This project explores relationships between the delivery status and some other factors using data analysis as a tool for visualizing and calculating the correlations and making them easier to understand.
The goal is not to paint the current process in a bad light, but to improve it with simple measures where possible. Just to make it easier for those involved and maybe there is a chance to reduce the amount of work required.

## Key Features
- **Data Cleaning**:
  - Selecting the columns to focus on, related to the main column of the delivery status.
  - Checking for null values and duplicated rows/columns.
  - Checking for outliers.
  - Converting the column names to "snake_case".
- **Data Analysis**:
  - Exploring the distributions of categorical and numerical data.
  - Univariate Analysis to see the distribution of the unique values, focusing on the columns "delivery_status", "market", "order_item_quantity" and "discount_ratio"
  - Bivariate Analysis to examine relationships between variables, focusing on the correlation between columns "delivery_status" and "market"/"order_item_quantity".
- **Statistical Analysis**:
  - Chi-square tests to check if there is a correlation between "delivery_status" and "market"/"order_item_quantity".
  - Cramer's v tests to check the strength of the correlation between "delivery_status" and "market"/"order_item_quantity".
- **Visualization**:
  - Bar charts and pie charts to show the distribution of the categorical values market and the delivery status. 
  - Histplot to visualize the distribution of the numerical variable discount ratio.
  - Boxplots to show the distribution of the discount ratio and to display that there are no outliers.
  - Crosstab to visualize the normalized values for the different markets regarding the delivery status.

## Main Insights
- **"delivery_status" and "market"**:
  - The delivery status does not correlate with market. No matter which continent, the distribution for each delivery status is the same.
- **"delivery_status" and "order_item_quantity"**:
  - It does also not correlate with the number of products ordered. No matter how many products were ordered, the distribution for each delivery status is almost the same.
- **Result not as we expected it to be**:
  - We recommend to revise the scheduled days for the various delivery options, to make it more realistic (more than 50% of the orders were delivered late)

## Tools & Techniques
- **Programming Languages**: Python (Pandas, NumPy, Matplotlib, Seaborn).
- **Statistical Methods**: Chi-square and Cramer's v tests.
- **Data Sources**: DataCo Supply Chain Dataset found on kaggle.com.

## Project Structure
- `main.ipynb`: Jupyter Notebook with the full univariate and bivariate analysis.
- `supply_chain_eda_presentation.pdf`: PDF presentation summarizing the conclusions.
- `queries_supply_chain.sql`: SQL file containing sample queries related to the supply chain dataset.
