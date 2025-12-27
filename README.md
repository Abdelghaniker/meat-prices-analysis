# Meat Prices Analysis (1990–2020)

This project explores monthly meat price trends from 1990 to 2020 to understand price changes over time and identify possible reasons behind major price fluctuations. The goal is to build a strong foundation for future price hike prediction and better grocery budget planning.

## Objectives
- Get a basic understanding of the dataset (structure, data types, missing values)
- Clean percentage change columns stored as text (remove `%` and convert to numeric)
- Handle missing values using rule-based logic (drop minimal missing, impute significant missing)
- Convert the Month column into a datetime index for time-series analysis
- Visualize long-term trends and volatility for each meat type:
  - Chicken
  - Beef
  - Lamb
  - Pork
  - Salmon

## Dataset
File: `data/Meat_prices.csv`  
Rows: 361  
Columns: 11  
Time range: Monthly data from 1990 to 2020

Columns include price levels and percentage price changes for each meat type.

## Data Cleaning Steps
1. **Fix percentage columns**
   - Removed the `%` sign from percentage change columns
   - Converted percentage change columns to numeric values

2. **Missing value handling**
   - Dropped rows with missing values in:
     - `Chicken price % Change`
     - `Beef price % Change`
     (only 1 missing value each)
   - Replaced remaining missing values (Lamb, Pork, Salmon related columns) using **median imputation**

3. **Datetime conversion**
   - Converted `Month` from object to datetime using the format `%b-%y`
   - Set `Month` as the index for time-series plotting

## Analysis & Visualizations
The notebook generates time-series plots for each meat type:
- **Price** over time
- **Percentage change** over time

These plots help identify periods of strong volatility and long-term price trends.

## Project Structure
