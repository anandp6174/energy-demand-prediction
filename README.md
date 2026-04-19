# Energy Demand Forecasting using Machine Learning

## Overview

This project focuses on forecasting electricity demand using machine learning models based on weather and temporal features. The goal is to improve understanding of demand patterns and detect peak load periods for better energy management.

---

## Objective

* Predict electricity demand using historical and weather data
* Identify peak demand periods
* Build a robust machine learning pipeline for time-series based forecasting

---

## Dataset Description

The dataset contains historical electricity demand along with meteorological variables.

### Key Features:

* Temperature (min, max, average)
* Surface pressure
* Wind speed
* Precipitation
* Time-based variables (day, month, weekday, weekend)
* Lag features (previous demand values)
* Rolling statistics (moving averages, max values)

---

## Methodology

### 1. Data Preprocessing

* Handling missing values
* Removing duplicates
* Outlier treatment using IQR method
* Date-time conversion and sorting

### 2. Exploratory Data Analysis (EDA)

* Demand distribution analysis
* Time-series trend visualization
* Correlation heatmap analysis
* Weather vs demand relationship study

### 3. Feature Engineering

* Temperature transformations (square, cube)
* Temperature range calculation
* Cooling Degree Days (CDD)
* Heating Degree Days (HDD)
* Lag features (t-1, t-2, t-7)
* Rolling statistics (mean, max)
* Time-based encoding

---

## Models Used

The following machine learning models were implemented:

* Random Forest Regressor
* XGBoost Regressor
* LightGBM Regressor
* CatBoost Regressor

---

## 🔗 Ensemble Approach

Final predictions were generated using an ensemble of multiple models by averaging their outputs to improve stability and reduce variance.

---

## Evaluation Metrics

Models were evaluated using:

* R² Score
* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)

---

## Results & Insights

* Gradient boosting models performed best (XGBoost, LightGBM)
* Ensemble model improved prediction stability
* Temperature had strong correlation with electricity demand
* Lag features significantly improved forecasting performance
* Seasonal and time-based patterns strongly influenced demand

---

## Peak Demand Detection

* Peak demand identified using percentile-based thresholding
* Model evaluated using classification metrics:

  * Precision
  * Recall
  * Confusion Matrix

---

## Tech Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn
* XGBoost, LightGBM, CatBoost

---

## Project Structure

```id="x7lq9a"
energy-demand-forecast/
│
├── data/
├── notebooks/
├── outputs/
├── README.md
├── requirements.txt
```

---

## Future Improvements

* Hyperparameter tuning (GridSearch / Optuna)
* Real-time forecasting using APIs
* Deployment using Streamlit or Flask
* Deep learning-based time series models (LSTM/GRU)

---

## Conclusion

This project demonstrates how machine learning can be used for electricity demand forecasting. The models successfully capture temporal and weather-driven patterns, making them useful for energy planning and peak load management.
