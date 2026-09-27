# Energy Consumption Prediction in Smart Homes Using IoT Sensor Data and Machine Learning Techniques

**Student Name:** SAIM MOHAMMAD TABBANI  
**USN:** 23BTRC0020  
**University:** JAIN UNIVERSITY  
**Department:** IoT  

## Project Overview
This repository contains the implementation of a predictive framework designed to estimate future household energy consumption using IoT sensor data. Residential buildings consume a significant proportion of electricity, and traditional rule-based systems struggle to capture dynamic user behaviors and environmental variations. This project utilizes machine learning algorithms to identify hidden consumption patterns and generate accurate forecasts.

## Dataset
The study uses the **UCI Appliances Energy Prediction Dataset**. The dataset includes 10-minute measurements of:
*   Appliance energy consumption (Target Variable)
*   Indoor temperature and humidity
*   Atmospheric pressure
*   Wind speed
*   Lighting usage

## Methodology
1. **Data Preprocessing:** Handled missing values, dropped non-predictive features (timestamps, random variables), and normalized all continuous features using `MinMaxScaler`.
2. **Data Splitting:** Applied an 80/20 train-test split to evaluate model performance on unseen data.
3. **Modeling:** Implemented four distinct algorithms to compare baseline linear modeling against advanced ensemble and deep learning techniques. 
    *   **Linear Regression:** Baseline model for identifying linear relationships.
    *   **Random Forest:** Ensemble tree model for handling nonlinear interactions.
    *   **XGBoost:** Gradient boosting model providing strong predictive performance.
    *   **LSTM:** Deep learning recurrent architecture structured for sequence and time-series forecasting.

## Expected & Actual Results
As hypothesized, complex models (Random Forest, XGBoost, LSTM) outperformed the baseline Linear Regression model due to their capacity to capture nonlinear relationships in environmental and appliance usage data. Random Forest achieved the highest predictive accuracy, demonstrating the best R2 score and lowest error metrics.

| Model             |    RMSE |     MAE |   MAPE (%) |   R2 Score |
|:------------------|--------:|--------:|-----------:|-----------:|
| Linear Regression | 91.1717 | 52.5471 |    62.9209 |   0.169362 |
| Random Forest     | 67.8865 | 32.0357 |    32.8017 |   0.539469 |
| XGBoost           | 74.8267 | 38.2541 |    41.5820 |   0.440493 |
| LSTM              | 88.6146 | 47.5254 |    49.8915 |   0.215301 |

## Source Code
*   `Ml_pro.ipynb`: Complete Python notebook including data preprocessing, model training, and metric evaluation.
