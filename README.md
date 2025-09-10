# 🛒 BigMart Sales Exploratory Data Analysis (EDA)

## Table of Contents

- [Overview](#overview)
- [Project Objectives](#project-objectives)
- [Dataset Description](#dataset-description)
- [Data Cleaning & Preprocessing](#data-cleaning--preprocessing)
- [Feature Engineering](#feature-engineering)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Key Insights & Results](#key-insights--results)
- [Conclusion](#conclusion--results)

---

## Overview

This project presents an in-depth exploratory data analysis (EDA) of the BigMart Sales dataset. The goal is to uncover key drivers of product sales across outlets using advanced data cleaning, feature engineering, rigorous analysis, and clear visualization. These insights support business strategy and growth in the retail sector.

---

## Project Objectives

- Analyze and visualize BigMart sales data to understand trends, patterns, and anomalies
- Identify factors significantly impacting outlet sales
- Engineer new, informative features for deeper analysis
- Make clear recommendations for retail decision-making and future analytics

---

## Dataset Description

- **Rows:** 8,523
- **Columns:** 12 (plus engineered features)
- **Target:** `Item_Outlet_Sales` (sales amount per item-outlet)
- **Source:** [BigMart Sales Dataset on Kaggle](https://www.kaggle.com/datasets/yasserh/bigmartsalesdataset)
- **File:** `BigMart_sales.csv` (place in project root)

### Main Variables

| Column Name                | Description                                   |
|----------------------------|-----------------------------------------------|
| Item_Identifier            | Unique item code                              |
| Item_Weight                | Product weight (kg)                           |
| Item_Fat_Content           | Fat level (Low Fat/Regular)                   |
| Item_Visibility            | % shelf display in store                      |
| Item_Type                  | Category (Dairy, Household, etc.)             |
| Item_MRP                   | Maximum Retail Price                          |
| Outlet_Identifier          | Unique outlet/store code                      |
| Outlet_Establishment_Year  | Year outlet was established                   |
| Outlet_Size                | Outlet size: Small/Medium/High                |
| Outlet_Location_Type       | City tier: Tier 1/2/3                         |
| Outlet_Type                | Supermarket/Grocery Store                     |
| Item_Outlet_Sales          | Sales for this item-outlet (target variable)  |

---

### Prerequisites

- Python 3.x
- pandas, numpy, matplotlib, seaborn

---

## Data Cleaning & Preprocessing

- **Missing Values:**  
  - `Item_Weight`: Imputed using the column median  
  - `Outlet_Size`: Imputed using the column mode  
- **Category Corrections:**  
  - Standardized inconsistent fat content labels
  - Consolidated outlet types (merged all supermarket subtypes)
- **Data Types:**  
  - Assigned proper types to categorical and numerical columns
- **Duplicates:**  
  - No duplicate entries found

---

## Feature Engineering

- **Price per Weight:** Unit price of items (`Item_MRP`/`Item_Weight`)
- **MRP Categories:** Binned item price into Low, Medium, High, Very High
- **Item_Category:** Classified item as Healthy-Consumable, Non-Healthy Consumable, Non-Consumable

---

## Exploratory Data Analysis

- **Univariate Analysis:**  
  Distribution plots for numerical columns, count plots for categorical columns

- **Bivariate/Multivariate Analysis:**  
  - Boxplots and violin plots comparing sales by category, outlet type, and location
  - Scatter plots for sales versus weight, MRP, and visibility
  - Heatmap for numeric correlations

- **Key EDA Outputs Include:**  
  - Most items are labeled Low Fat  
  - Item_Weight has a nearly normal (symmetric) distribution with average around 12.8kg  
  - Higher MRP (price) correlates with higher sales  
  - Supermarkets and Tier 3 outlets generate significantly more sales  
  - Some outlet years underperform (notably, those opened in 1998)

---

## Key Insights & Results

- **MRP is the dominant driver of sales:** Higher MRP leads to higher outlet sales
- **Outlet Characteristics Matter:** Supermarkets and Tier 3 locations outperform others
- **Visibility Score Weakness:** Higher item display percentage is not always tied to higher sales
- **Category Leaders:** Starchy Foods and Seafood have the highest average sales among item types
- **Year of Establishment:** Outlets opened in 1998 display consistently lower revenues

---
## Conclusion
This analysis shows that product price (MRP), outlet type, and location tier are the main sales drivers for BigMart. Supermarkets in Tier 3 cities achieve higher sales, while item visibility on shelves does not directly impact sales significantly. Feature engineering enhanced understanding of sales patterns by categorizing products and pricing.

These insights can help optimize pricing and marketing strategies to improve sales. Future work could include building predictive models and incorporating external factors for more robust forecasting.
