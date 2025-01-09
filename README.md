# Crown Case Study

## Overview
This repository contains the code and analysis for the **Crown Case Study**, conducted by **Swathi Subramanyan**. The project explores and analyzes sales data from a group of restaurants using Python, SQL-like queries, and Power BI visualizations.

### Objectives
- Perform data exploration, quality checks, and SQL-based analysis.
- Analyze restaurant operations to derive actionable insights.
- Create interactive visualizations to support decision-making.

## Dataset
The dataset details the operations of a group of restaurants and includes information on:
- Locations
- Types of restaurants
- Meal types
- Order details
- Membership details

**Source**: [Kaggle - Restaurants Customers Orders Dataset](https://www.kaggle.com/datasets/vainero/restaurants-customers-orders-dataset)

### Assumptions
1. The restaurants belong to "The Crown Group."
2. Members are awarded a paid membership with a monthly budget for free meals. Excess spending earns them a commission of 10-12%.

## Project Structure
### Table of Contents

1. [Data Cleaning](#data-cleaning)
2. [SQL-Based Analysis](#sql-based-analysis)
3. [Insights](#insights)
4. [Visualization](#visualization)

## Tools and Libraries
The following libraries are used in the project:
- `pandas` - For data manipulation.
- `pandasql` - To write SQL queries on pandas DataFrames.
- `Power BI` - For creating interactive dashboards.

## Data Cleaning
### Steps Taken
1. **Handling Missing Data**: 
   - Filled null values in key columns like `Order_ID` and `Member_ID` based on business rules.
   - Replaced missing restaurant types using the most frequent type per city.
2. **Removing Duplicates**: 
   - Identified and removed duplicate entries in `orders.csv` and `members.csv`.
3. **Consistency Checks**:
   - Standardized restaurant names and member IDs.
   - Verified numeric ranges for earnings and commission values.

## SQL-Based Analysis
The following SQL queries were analyzed using `pandasql`:
1. **Member Distribution**:
   - Number of members in each city.
2. **Meal Preferences**:
   - Cities with the most vegan meals by members and orders.
3. **Service Type Analysis**:
   - Proportion of serve types (e.g., dine-in, takeaway) for Italian restaurants.

## Insights
### Key Findings
1. **Earnings Analysis**:
   - February 2020 saw a 9% (49.58K) dip in member earnings compared to January.
   - Restaurants R19 (27.7%), R20 (25.7%), and R28 (25.06%) were most affected.
2. **Valuable Members**:
   - Most valuable members, such as M112 and M157, contributed significantly to group earnings (calculated as `0.7 * expense + 0.3 * order frequency`).
   - Promotions and loyalty rewards can target these high-value customers.
3. **Staffing Recommendations**:
   - Peak hours are from 12–1 PM and 7–10 PM. Evenings tend to be busier.
   - Staffing should prioritize restaurants like R13 (busiest) and adjust shifts accordingly.

## Visualization
Power BI dashboards were created to support the analysis:
1. **Earnings Trends**:
   - Monthly member earnings trendline highlighting dips and peaks.
2. **Member Value**:
   - Visual representation of top members by their contribution to earnings.
3. **Staffing Optimization**:
   - Heatmap showing peak hours across restaurants to assist in shift planning.
