# 🌍 MagNet Dst Prediction using Machine Learning

Predicting geomagnetic disturbances (Dst Index) from real-time solar wind observations using feature engineering and machine learning.

## Project Overview

This project was developed as the **final evaluation project** for the **Machine Learning with Python: Zero to GBMs** course by Jovian.

The goal is to predict the **Disturbance Storm Time (Dst) index**, an important indicator of geomagnetic storm intensity, using solar wind and space weather observations.

The project combines:

* Data preprocessing and analysis
* Feature engineering
* Time-series alignment
* Machine learning model development
* Hyperparameter tuning
* Performance evaluation against archived competition scores

---

## Problem Statement

Geomagnetic storms can impact:

* Satellite systems
* GPS navigation
* Communication infrastructure
* Electrical grids

This project aims to forecast future Dst values from solar wind measurements collected near Earth.

---

## Dataset

Dataset: **NOAA MagNet Challenge Dataset**

Main sources:

* Solar Wind Data
* Satellite Position Data
* Sunspot Data
* Dst Labels

Training data contained:

* ~8.4 million rows
* Minute-level observations
* Multiple space-weather measurements

---

## Project Workflow

### 1. Data Preparation

* Load and clean raw datasets
* Convert temporal information into aligned indices
* Handle missing values
* Merge multiple data sources

### 2. Exploratory Data Analysis

* Distribution analysis
* Correlation analysis
* Time-series visualization
* Geomagnetic storm behavior study

### 3. Feature Engineering

Engineered features included:

* Rolling statistics:

  * 1h
  * 3h
  * 6h
  * 12h
  * 24h

* Physics-inspired features:

  * Dynamic Speed
  * Electric Field Proxy
  * Southward Magnetic Field (Bz)
  * Magnetic Field Magnitude (B)

* Lag-based temporal features

### 4. Modeling

Models explored:

* Linear Regression
* Ridge Regression
* Random Forest
* XGBoost

### 5. Hyperparameter Tuning

Optimized:

* `n_estimators`
* `max_depth`
* `learning_rate`
* `subsample`

---

## Final Results

### Best Model: XGBoost

| Metric         | Result       |
| -------------- | ------------ |
| Test RMSE      | **13.6934**  |
| Estimated Rank | **#31 / 85** |
| Percentile     | **63.53%**   |

Key observations:

* Magnetic-field-based engineered features produced the strongest gains.
* Lower validation loss did not always improve leaderboard performance.
* Careful feature selection improved generalization.

---

## Repository Structure

```text
MagNet_DST_Prediction.ipynb
README.md
```

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* XGBoost
* Kaggle API

---

## Learning Outcomes

Through this project I gained experience in:

* Machine Learning Pipelines
* Feature Engineering
* Time-Series Data Processing
* Model Evaluation
* Hyperparameter Optimization
* Scientific Machine Learning

---

## Acknowledgements

* Jovian — Machine Learning with Python: Zero to GBMs
* NOAA MagNet Challenge
* Kaggle

---

⭐ If you found this project interesting, feel free to explore the notebook and share feedback.
