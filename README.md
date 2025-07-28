# 🚖 AutomatiData - Predicting Generous Tippers in NYC Taxi Rides

This project aims to build a machine learning model that predicts whether a passenger is likely to give a generous tip on a NYC taxi ride.

---

## 🎯 Objective

To create a reliable classification model that predicts "generous tipping" behavior based on trip characteristics such as distance, duration, fare, and payment type.

---

## 🧠 Methods Used

1. **Data Preprocessing**
   - Converted pickup and dropoff timestamps into datetime objects
   - Derived trip duration
   - Removed irrelevant and duplicate columns
   - Filtered out outliers in distance and fare fields

2. **Feature Engineering**
   - Created a binary target variable: `generous_tipper` (1 if tip > 20% of fare)
   - One-hot encoded categorical variables (e.g. `payment_type`)
   - Normalized numerical features for consistent scale

3. **Modeling**
   - Split dataset into training and test sets
   - Trained baseline Logistic Regression model
   - Trained and tuned XGBoost classifier
   - Evaluated models using Accuracy, Precision, Recall, and F1 Score

---

## 🔑 Key Findings

- Passengers paying by **credit card** were more likely to tip generously.
- **Trip distance** and **fare amount** were strong predictors of tipping behavior.
- Shorter trips had **lower tipping probability**, especially when paid in cash.
- The model performed significantly better when using engineered features such as trip duration and fare ratios.

---

## 🏆 Best Model Results (XGBoost Classifier)

| Metric     | Score     |
|------------|-----------|
| Accuracy   | 0.721     |
| Precision  | 0.697     |
| Recall     | 0.828     |
| F1 Score   | 0.757     |

These results indicate that the XGBoost model is effective in predicting generous tippers, with a strong balance between precision and recall.

---

## 📌 Author

**Ali Krisht**  
