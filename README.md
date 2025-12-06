#  Flight Price Prediction – Machine Learning Project

This project predicts flight ticket prices using machine learning.
It includes complete data cleaning, feature engineering, EDA, and model building.

---

##  Project Goal

To build a regression model that can accurately predict flight fares based on airline, source, destination, stops, duration, class, and timing.

---

##  Dataset

The dataset contains flight details such as:

- Airline

- Source & Destination

- Route

- Total Stops

- Duration

- Date of Journey

- Departure & Arrival Times

- Additional Info

- Ticket Price

Dataset File: **Flight_Fare.xlsx**

---

## 🧹 Data Cleaning

Steps performed:

- Fixed incorrect or inconsistent duration values

- Reconstructed missing arrival times

- Corrected unrealistic entries (e.g., 5-minute flights)

- Standardized class labels

- Simplified routes

- Converted 3 stops & 4 stops to “More than 3 stops”

- Converted date/time columns into separate numeric features

---

## 🛠️ Feature Engineering

Features created:

- Dep_Hour, Arr_Hour

- Journey_Day, Journey_Month, Journey_Weekday

- Duration_Minutes category

- Is_Layover_Flight

- Red_eye_Flight

- No_Check_in_baggage, No_meals

- Dep_Period, Arrival_Period (Morning, Evening, Night)

- Encoded Total Stops

- Simplified Route

- One-hot encoded Class

---

##  Exploratory Data Analysis

Included visualizations such as:

- Price distribution

- Airline vs Price

- Stops vs Price

- Duration vs Price

- Month/day/weekday trends

- Feature importance (XGBoost)

---

## Models Used
Model	RMSE ↓	R² ↑
Linear Regression	3019.85	0.5691
Random Forest	1965.23	0.8175
Random Forest (Tuned)	1944.32	0.8213
XGBoost	1832.09	0.8414
XGBoost (Tuned)	1775.84	0.8509

### Best Model: Tuned XGBoost (XGBRegressor)

---

## Hyperparameter Tuning

Performed using RandomizedSearchCV on:

- Random Forest

- XGBoost

Resulted in improved RMSE and R² scores.
