# Food Demand Forecasting Using Prophet

## Project Overview
This project focuses on forecasting weekly demand for retail products, with a particular focus on the **foods category**. Using historical sales data, seasonal trends, and events such as holidays or promotions, the project employs **time series analysis with Prophet** to predict future demand. The goal is to enable data-driven inventory management, reduce stockouts, and optimize supply chain planning.

## Project Goals
- Capture trends and seasonality in food product sales.
- Forecast weekly demand for the foods category.
- Incorporate external factors (holidays) to improve forecast accuracy.
- Provide actionable insights for inventory and operational planning.

## Data
The project uses three datasets:

1. **Sales Data**  
   - Contains historical sales of products per store and category.    

2. **Sell Prices Data**  
   - Contains the selling price of products over time.   

3. **Calendar Data**  
   - Contains date-related information including events, holidays, and promotions.  


## Methodology
1. **Data Preprocessing**
   - Convert dates to datetime format.
   - Aggregate sales data weekly.
   - Filter for the foods category.
   - Identify and encode events/holidays.

2. **Modeling**
   - Use **Prophet** for time series forecasting and **LightGBM** and **XGBoost** for machine learning-based demand prediction.
   - Incorporate **weekly and yearly seasonality** and **holidays/events** in Prophet.
   - Generate future periods for prediction and compare forecasts from all models for accuracy.

3. **Forecasting**
   - For **Prophet**: produce `yhat` (predicted demand), `yhat_lower`, and `yhat_upper` (confidence intervals).  
   - For **LightGBM and XGBoost**: generate predictions using engineered features such as lagged sales, rolling averages, day-of-week, and promotions.  
   - Visualize trends, seasonality, and forecasts from all models to compare performance and interpret results.


