# MSCS 634 Lab 1

## Data Visualization, Data Preprocessing, and Statistical Analysis Using Python

**Student Name:** Pranavi Balakulla  
**Course:** MSCS 634  
**Assignment:** Lab 1  

## Purpose

The purpose of this lab is to demonstrate data collection, visualization, preprocessing, and statistical analysis using Python in a Jupyter Notebook. A retail sales dataset was analyzed using Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn.

## Dataset

The retail sales dataset contains 240 transactions and the following columns:

- Transaction_ID
- Date
- Category
- Region
- Store
- Quantity
- Discount_Percent
- Sales
- Customer_Rating

## Data Visualizations

A scatter plot was used to examine the relationship between quantity and sales. The visualization showed that transactions with higher quantities generally produced higher sales. Electronics transactions frequently had higher sales values.

A line plot was used to display monthly sales trends. Monthly sales changed throughout the observed period, showing increases and decreases over time.

## Data Preprocessing

The original dataset contained four missing Sales values and three missing Customer_Rating values. Missing Sales values were replaced with the median of 175.09, while missing Customer_Rating values were replaced with the mode of 4.2.

The IQR method identified 20 Sales outliers. After removing these records, the dataset was reduced from 240 rows to 220 rows.

Data reduction was performed using a reproducible 25% random sample and by removing the Transaction_ID and Store columns. Min-Max scaling transformed selected numerical variables to values between 0 and 1. Sales values were also discretized into Low, Medium, and High categories.

## Statistical Insights

The average Sales value after outlier removal was 186.82 dollars, while the median was 153.12 dollars. The average customer rating was 4.09.

Quantity and Sales had a moderate positive correlation of 0.59. This indicates that transactions containing more items generally generated higher sales. Other numerical variables showed weak correlations.

## Challenges and Decisions

Missing Sales values were replaced with the median because it is less affected by extreme values. Missing customer ratings were replaced with the mode because it represents the most frequently occurring rating.

The IQR method was selected for outlier detection because the original Sales data contained several unusually large values. A random state of 42 was used during sampling to make the result reproducible.

## Repository Contents

- `MSCS_634_Lab_1.ipynb` — completed Jupyter Notebook
- `retail_sales_data.csv` — original dataset
- `retail_sales_data_cleaned.csv` — cleaned dataset
- `screenshots/` — screenshots of required outputs and visualizations
