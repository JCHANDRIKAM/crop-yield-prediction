
# Predictive Model for Crop Yield Prediction using Machine Learning

## Overview

This project develops a **machine learning model** to predict crop yield using real-world agricultural and environmental data. The model helps estimate future crop yield accurately and provides insights into the factors affecting yield.


## Dataset

**Source:** [Kaggle - Crop Yield Prediction Dataset](https://www.kaggle.com/datasets/patelris/crop-yield-prediction-dataset/data)

The dataset contains features that impact crop yield, including environmental conditions, crop type, and historical yield data.

**Key Features:**
* Region or area of cultivation
* Crop type
* Year of record
* Crop yield (hg/ha)
* Average annual rainfall (mm)
* Pesticides applied (tonnes)
* Average annual temperature (°C)

These features enable the model to learn patterns influencing crop yield under different environmental and agricultural conditions.


## Data Preprocessing
* Handled missing values and outliers
* Encoded categorical features (e.g., crop type, region)
* Split dataset into **training (80%)** and **testing (20%)** sets
* Scaled or normalized numerical features to improve model performance



## Model Training
**Algorithm:** Random Forest Regressor (from `scikit-learn`)

**Why Random Forest?**
* Captures non-linear relationships
* Robust to noise and outliers
* Requires minimal feature engineering


**Training Steps:**
1. Split data into training and testing sets
2. Fit the Random Forest model on training data
3. Predict crop yields on testing data


##  Evaluation Metrics

| Metric       | Value          | Description                                         |
| ------------ | -------------- | --------------------------------------------------- |
| **MAE**      | 3616.61        | Average deviation of predictions from actual values |
| **MSE**      | 101,088,271.80 | Penalizes larger errors more heavily                |
| **R² Score** | 0.9863         | Model explains 98.63% of the variance in data       |

High R² indicates strong predictive performance. MAE and MSE are reasonable given the scale of crop yield values.



## Visualization

The scatter plot of **actual vs predicted yields** shows most points lie along the diagonal, confirming that the model predicts crop yield accurately.



## Results & Interpretation

The Random Forest model effectively captures relationships between environmental features and crop yield. Predictions closely follow actual values, demonstrating strong performance across diverse conditions in the dataset.