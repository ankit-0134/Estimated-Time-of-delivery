# 🍽️ Estimated Time of Delivery Prediction

## 📌 Overview
This project predicts **Estimated Time of Delivery (ETA)** for food orders using a **two-stage modeling pipeline**:

1. **Pickup Delay Prediction** – Time from order placement to pickup.  
2. **Post-Pickup Travel Time Prediction** – Time from pickup to delivery.

---

## 🚀 Features
- **Two-stage regression approach** for improved accuracy.
- **Feature engineering** from raw order data:
  - Extracted `pickup_hour`, `is_weekend`
  - Distance calculation from coordinates
  - Weather, traffic, festival, and city type encoding
- **Model comparison**:
  - RandomForestRegressor
  - GradientBoostingRegressor
  - Ridge Regression
- **Feature importance analysis** to interpret model decisions.

---

## 📊 Workflow
1. **Data Preprocessing** – Clean missing values, encode categorical features, scale numerical features if needed.  
2. **Stage 1 – Pickup Delay Model** – Predict time from order to pickup using order time, weather, traffic, festival, and city type.  
3. **Stage 2 – Post-Pickup Model** – Predict delivery time after pickup using driver age, ratings, vehicle condition, distance, traffic, and weather.  
4. **Evaluation** – Metrics: **MAE** and **RMSE**, compare RandomForest, GradientBoosting, Ridge.

---

## 📈 Results
**Pickup Delay Prediction**
| Model            | MAE   | RMSE  |
|------------------|-------|-------|
| GradientBoosting | 3.86  | 4.69  |
| RandomForest     | 3.93  | 4.76  |
| Ridge            | 4.04  | 4.87  |

**Post-Pickup Travel Time**
| Model            | MAE   | RMSE   |
|------------------|-------|--------|
| RandomForest     | 9.88  | 19.22  |
| GradientBoosting | 10.31 | 19.38  |
| Ridge            | 15.52 | 28.84  |

---

## 📌 Future Improvements
- Add quantile regression for uncertainty estimates.
- Optimize hyperparameters with RandomizedSearchCV.
- Integrate real-time traffic/weather APIs.
- Deploy as a public web app.

---

## ✨ Author
**Ankit** – Data Science Enthusiast  
📧 [ankitkd23@iitk.ac.in](mailto:ankitkd23@iitk.ac.in) | 🌐 [GitHub](https://github.com/ankit-0134)
