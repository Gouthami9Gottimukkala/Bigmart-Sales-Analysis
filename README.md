# BigMart Sales Exploratory Data Analysis (EDA)

## Project Overview

This project performs an exploratory data analysis (EDA) on the BigMart sales dataset to uncover patterns, trends, and factors influencing sales. It involves data cleaning, visualization, and feature engineering using Python libraries such as Pandas, NumPy, Matplotlib, and Seaborn.

---

## Dataset Description

- **Rows:** 8,523  
- **Columns:** 12  
- **Features include:**  
  - Item details: `Item_Identifier`, `Item_Weight`, `Item_Fat_Content`, `Item_Visibility`, `Item_Type`, `Item_MRP`  
  - Outlet details: `Outlet_Identifier`, `Outlet_Establishment_Year`, `Outlet_Size`, `Outlet_Location_Type`, `Outlet_Type`  
  - Target variable: `Item_Outlet_Sales`

---

## Problem Statement

- Analyze the dataset to understand factors impacting sales in each outlet.  
- Identify anomalies and trends via charts and visuals.  
- Handle missing values and outliers effectively to clean the data.

---

## Data Cleaning and Preprocessing

- Missing values found in `Item_Weight` (~17%) and `Outlet_Size` (~28%).  
- Imputed missing `Item_Weight` with median; missing `Outlet_Size` with mode.  
- Corrected inconsistencies in `Item_Fat_Content` categories.  
- Combined multiple supermarket types into one category.

---

## Exploratory Analysis

- **Univariate Analysis:** Distribution plots for numerical columns and count plots for categorical features.  
- **Bivariate Analysis:** Relationships between features like `Item_Weight` vs `Item_Outlet_Sales`, `Item_Type` vs `Item_Outlet_Sales`.  
- **Multivariate Analysis:** Heatmaps of correlations and grouped bar plots for average sales by `Item_Type` and `Outlet_Type`.

---

## Key Insights

- Low Fat items have higher counts than Regular.  
- Fruits, Vegetables, and Snack Foods are fast-selling item types.  
- Supermarkets outperform grocery stores in sales, with Tier 3 locations having more outlets but similar median sales to others.  
- Medium-sized outlets are most frequent; small outlets generally show lower sales.  
- Price per unit weight correlates slightly with sales; higher MRP items tend to have higher sales.  
- Little to no correlation found between `Item_Visibility` and sales, indicating missing or zero visibility scores need further investigation.

---

## Feature Engineering

- Created `Price per Weight` feature (Item_MRP / Item_Weight).  
- Categorized `Item_MRP` into bands: Low, Medium, High, Very High.  
- Classified `Item_Type` into `Healthy-Consumable`, `Non Healthy Consumable`, and `Non-Cosumable`.

---

## How to Use

1. Load the data using:  
      df = pd.read_csv("BigMart_sales.csv")
2. Perform data preprocessing and cleaning as described.  
3. Visualize data and extract insights using the provided code snippets and charts.  
4. Follow feature engineering steps to enhance dataset for modeling or further analysis.

---

## Libraries Used

- numpy  
- pandas  
- matplotlib  
- seaborn
