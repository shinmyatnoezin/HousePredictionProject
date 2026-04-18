# House Price Prediction in Bristol Using Geospatial Features

## 📌 Project Overview

This project investigates the use of machine learning techniques to predict residential property prices in Bristol using **geospatial features only**.

Unlike traditional models that rely on structural attributes (e.g., number of rooms, floor area), this study focuses on **location-based modelling** due to the limitations of publicly available datasets.

The project demonstrates that meaningful predictive performance can be achieved using **latitude, longitude, and derived spatial features**, even in data-limited scenarios.

---

## Objectives

* Collect and integrate housing transaction data and postcode data
* Perform data cleaning and exploratory data analysis (EDA)
* Engineer meaningful geospatial features
* Train and evaluate machine learning models
* Investigate non-linear spatial relationships using advanced techniques

---

## Dataset

### 1. HM Land Registry Price Paid Data

* Source: UK Government
* Period: **2020 – 2025**
* Contains:

  * Property prices
  * Transaction dates
  * Postcodes

### 2. UK Postcode Dataset

* Provides:

  * Latitude
  * Longitude

### 🔗 Data Integration

Datasets are merged using **postcode** to enrich transaction data with geographic coordinates.

---

##  Methodology

### 1. Data Preprocessing

* Removed missing values
* Filtered dataset for Bristol properties (e.g., BS postcodes)
* Converted variables into appropriate formats

---

### 2. Feature Engineering

Key features used in the model:

*  **Latitude & Longitude**
*  **Distance to City Centre** (using Haversine formula)
*  **Spline Transformations** (to capture non-linear spatial patterns)
*  **Log Transformation of Price** (to reduce skewness)

---

### 3. Machine Learning Model

* Model used: **Random Forest Regressor**
* Reason:

  * Handles non-linear relationships
  * Robust to noise
  * Works well with limited feature sets

---

### 4. Model Evaluation

The model was evaluated using:

* **R² Score**
* **RMSE (Root Mean Squared Error)**
* **MAPE (Mean Absolute Percentage Error)**

---

## Results

* Best model achieved:

  * **R² ≈ 0.63**

### Key Findings:

* Geospatial features alone can provide **meaningful predictive power**
* **Spline transformations** significantly improve performance
* Distance-based features help capture location influence
* Log transformation improves model stability and relative error


## Visualisations

The project includes:

* Actual vs Predicted Plot
* Residual Plot
* Feature Importance Plot

These visualisations help interpret model performance and spatial patterns.


## Limitations

* No structural features (e.g., number of rooms, floor area)
* Reduced accuracy for high-value properties
* Model relies heavily on location

## Future Work

* Incorporate structural and socio-economic data
* Explore advanced models (e.g., XGBoost, LightGBM)
* Add time-series analysis for price trends
* Apply model to other cities


## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib / Seaborn

##  References

* Rosen, S. (1974). Hedonic Prices and Implicit Markets
* Breiman, L. (2001). Random Forests
* Géron, A. (2022). Hands-On Machine Learning
* Hastie, T., Tibshirani, R., Friedman, J. (2009)
* James, G. et al. (2021)

