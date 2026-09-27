# Energy Consumption Prediction in Smart Homes Using IoT Sensor Data and Machine Learning Techniques

**Student Name:** SAIM MOHAMMAD TABBANI  
**USN:** 23BTRC0020  
**University:** JAIN UNIVERSITY  
**Department:** IoT  

## Project Overview
This repository contains the implementation of a predictive framework designed to estimate future household energy consumption using IoT sensor data. Residential buildings consume a significant proportion of electricity, and traditional rule-based systems struggle to capture dynamic user behaviors and environmental variations. This project utilizes machine learning algorithms to identify hidden consumption patterns and generate accurate forecasts.

## Dataset & Exploratory Data Analysis (EDA)
The study uses the **UCI Appliances Energy Prediction Dataset**, featuring 10-minute measurements of appliance energy usage, indoor environmental metrics (temperature, humidity), and outdoor weather conditions.

### EDA Findings:
* **Feature Distributions:** Temperature and humidity features show strong diurnal cycles.
* **Target Variance:** Appliance energy consumption exhibits high variance with frequent peak spikes during specific daily activity hours.
* **Correlations:** Environmental features (indoor/outdoor temperatures and humidity) show significant nonlinear correlations with energy usage, making linear models less effective.

## Methodology
1. **Data Preprocessing:** Handled missing values, dropped non-predictive features (`date`, `rv1`, `rv2`), and normalized all continuous features using `MinMaxScaler`.
2. **Data Splitting:** Applied an 80/20 train-test split.
3. **Model Implementation:**
    * **Linear Regression:** Baseline linear benchmark.
    * **Random Forest:** Ensemble tree approach capturing feature interactions.
    * **XGBoost:** Optimized gradient boosting regressor.
    * **LSTM:** Recurrent deep learning architecture for time-series sequences.

## Experimental Results
| Model             |    RMSE |     MAE |   MAPE (%) |   R2 Score |
|:------------------|--------:|--------:|-----------:|-----------:|
| Linear Regression | 91.1717 | 52.5471 |    62.9209 |   0.169362 |
| Random Forest     | 67.8865 | 32.0357 |    32.8017 |   0.539469 |
| XGBoost           | 74.8267 | 38.2541 |    41.5820 |   0.440493 |
| LSTM              | 88.6146 | 47.5254 |    49.8915 |   0.215301 |

## Comparison with Literature (20 Research Papers)
Across the 20 benchmark papers reviewed in smart home energy forecasting (e.g., Kaur et al., 2022; Mathumitha & Rathika, 2024; Li et al., 2022):
* **Literature Consensus:** Ensembles (Random Forest, XGBoost) and deep neural networks consistently outperform simple linear regression models in residential energy load forecasting due to complex nonlinear dependencies.
* **Our Findings Alignment:** Our experimental results strongly align with literature findings. Random Forest achieved the highest $R^2$ (0.539) and lowest RMSE (67.88), outperforming Linear Regression ($R^2$: 0.169), confirming that nonlinear tree-based ensembles are highly effective for smart meter sensor data.

## Source Code
* `Ml_pro.ipynb`: Python notebook containing EDA, data preprocessing, model implementations, and metric evaluation.
