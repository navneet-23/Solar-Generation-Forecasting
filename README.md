# Solar Power Forecasting using Time Series Models

This project focuses on forecasting solar power generation using both classical time-series methods and machine learning approaches.

---

## Dataset

The dataset consists of timestamped solar power generation values:

- **Timestamp**: Date-time of observation  
- **Value (MW)**: Power generated in megawatts  

The data is aggregated at different time scales (daily, multi-day, weekly, monthly) to analyze trends and seasonality.

---

## Approach

### 1. Data Preprocessing
- Converted timestamps to datetime format  
- Sorted data chronologically  
- Aggregated data at daily and multi-day levels  

---

### 2. Exploratory Analysis
- Visualized trends at:
  - Daily level  
  - Weekly level  
  - Monthly level  
  - Yearly level  
- Observed seasonality and long-term patterns  

---

### 3. Stationarity & Transformation
- Performed Augmented Dickey-Fuller (ADF) test  
- Applied differencing to achieve stationarity  
- Verified stationarity post transformation  

---

### 4. SARIMA Model
- Used SARIMAX for time-series forecasting  
- Selected parameters manually based on ACF/PACF analysis  
- Trained on 80% of data and tested on remaining 20%  

---

### 5. XGBoost Model
- Created lag-based features (previous time steps)  
- Trained gradient boosting model on structured data  
- Captured non-linear dependencies in the time series  

---

## Results

- Both models were evaluated using **RMSE (Root Mean Squared Error)**  
- SARIMA captures temporal structure and seasonality  
- XGBoost leverages lag features for flexible prediction  

The comparison highlights the trade-off between:
- Statistical models (structured, interpretable)  
- Machine learning models (flexible, data-driven)  

---

## Visualizations

- Time series plots across different granularities  
- ACF and PACF plots for correlation analysis  
- Forecast vs actual comparisons for both models  

---

## Conclusion

- Time-series data exhibits strong temporal dependencies and seasonality  
- SARIMA provides a structured baseline  
- XGBoost improves flexibility through feature-based learning  
- Combining statistical and ML approaches can be a powerful strategy
- SARIMA gave a better RMSE than directly applying XGBoost, proving the robustness and simplicity of statistical techniques.

---

## Notes

- The notebook follows a step-by-step pipeline from preprocessing to modeling  
- All experiments are reproducible within the notebook  
