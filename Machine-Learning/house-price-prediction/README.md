# 🏠 House Price Prediction: Advanced Regression & Feature Engineering

This project implements a high-precision Linear Regression model to predict real estate prices. The core strength of this project lies in its **Advanced Feature Engineering pipeline**, which transforms basic property data into powerful predictive indicators.

---

## 📈 Model Performance

The model achieves exceptional accuracy, demonstrating the effectiveness of the engineered features:

| Metric | Validation Set | Test Set (Final) |
| :--- | :--- | :--- |
| **R-squared (R2)** | **0.9988** | **0.9984** |
| **MAE** | $7,022.70 | $8,138.30 |
| **RMSE** | $8,868.68 | $10,116.65 |

---

## 🛠️ Advanced Feature Engineering

I developed a custom feature engineering suite to capture non-linear relationships and property value drivers:

* **Structural Metrics:** Created `House_Age`, `Total_Rooms`, and `Rooms_Density` to measure space utilization.
* **Luxury & Quality Indices:** Developed a `Luxury_Index` (combining Garage size, Bathrooms, and Neighborhood quality) and a `Structural_Value_Index`.
* **Economic Indicators:** Implemented a `Price_Size_Estimate` based on a $120/sqft baseline and a `Land_Value_Ratio`.
* **Decay & Modernity:** Added an `Age_Decay_Factor` (non-linear value diminish) and a `Modern_Ratio` to assess how amenities relate to the property's age.
* **Mathematical Transformations:** Used `log1p` transformations for the `Neighborhood_Space_Index` to reduce the impact of outliers in large square footage data.

---

## 🏗️ Technical Pipeline

1.  **Preprocessing:** Automated handling of missing values and scaling using a saved `joblib` pipeline.
2.  **Feature Generation:** A custom Python function `add_features` that injects 10+ domain-specific variables into the dataset.
3.  **Model:** Linear Regression (optimized for high-dimensional feature spaces).
4.  **Deployment Ready:** The entire pipeline (Preprocessing + Model) is serialized for real-time inference.

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, Joblib.
* **Techniques:** Linear Regression, Feature Engineering, Pipeline Serialization.
