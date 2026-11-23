# E-Commerce Data Analysis – DecodeLabs Internship Task 2

A data analysis project on e-commerce order data. It covers data cleaning, validation, exploratory analysis, visualization, and outlier detection using Python.

## Project Overview

The goal of this project is to clean and understand an online orders dataset, then find useful patterns in sales, customers, products, and payments.

## Dataset

- **File:** Dataset for Data Analytics.csv
- **Size:** 1,200 rows and 14 columns
- **Period:** January 2023 – June 2025
- **Columns:** OrderID, Date, CustomerID, Product, Quantity, UnitPrice, ShippingAddress, PaymentMethod, OrderStatus, TrackingNumber, ItemsInCart, CouponCode, ReferralSource, TotalPrice

## Tools and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Workflow

### 1. Data Cleaning
- Found missing values: 309 in `CouponCode`, filled with "NoCoupon"
- Checked for duplicate records: none found
- Converted the `Date` column to datetime format
- Removed extra spaces from text columns

### 2. Data Validation
- Checked that OrderID, CustomerID, and TrackingNumber follow the correct format
- Checked Quantity (1–5), UnitPrice, ItemsInCart (1–10), and TotalPrice for invalid values
- Confirmed `TotalPrice = Quantity × UnitPrice` for every row (0 mismatches)

### 3. Exploratory Data Analysis
- Summary statistics and distributions of Quantity, UnitPrice, TotalPrice, and ItemsInCart
- Time trends: monthly orders, monthly revenue, and revenue by day of week
- Customer behavior: top 10 customers by orders and by revenue
- Product performance: top products by orders and by revenue
- Payment method, order status, and referral source breakdowns

### 4. Relationship and Correlation Analysis
- Scatter plots: Quantity vs TotalPrice, UnitPrice vs TotalPrice, Quantity vs UnitPrice
- Correlation heatmap of numeric columns

### 5. Outlier Detection
- Box plots and the IQR method on all numeric columns
- Found **8 outliers** in `TotalPrice` and removed them to create a cleaned dataset (1,192 rows)

## Key Results

- The dataset is clean: no duplicates and no invalid IDs or values
- `TotalPrice` has a strong positive link with `UnitPrice` (0.72) and `Quantity` (0.62)
- `Quantity` and `ItemsInCart` are also positively linked (0.65)
- Only `TotalPrice` had outliers (8 orders with very high totals)

## How to Run

1. Clone this repository:
   ```
   git clone https://github.com/najeebullah240/decodelabs_data_analysis_intrenship_Task2.git
   ```
2. Install the required libraries:
   ```
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Open the notebook:
   ```
   jupyter notebook data_analysis_decodelabs_project_Task2.ipynb
   ```
4. Update the CSV file path in the "Load CSV File" cell to match your computer.

## Repository Files

| File | Description |
|------|-------------|
| `data_analysis_decodelabs_project_Task2.ipynb` | Main analysis notebook |
| `Dataset for Data Analytics.csv` | Dataset used in the analysis |
| `README.md` | Project documentation |
