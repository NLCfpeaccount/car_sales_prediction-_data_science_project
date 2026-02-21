# car_sales_prediction-_data_science_project
# Car Sales Prediction 🚗💰

A Machine Learning regression project designed to estimate the potential sales price of vehicles based on various features like brand, mileage, year, and fuel type.

## 📌 Project Overview
Predicting the resale value of a car is essential for both dealerships and individual sellers. This project implements a supervised learning model to predict car prices with high accuracy, helping stakeholders make data-driven pricing decisions.

## 📊 Dataset Features
The model analyzes several key factors to determine the price:
* **Year**: The manufacturing year of the vehicle.
* **Mileage**: Total distance driven (KM).
* **Fuel Type**: Petrol, Diesel, CNG, or Electric.
* **Transmission**: Manual vs. Automatic.
* **Engine/Power**: Technical specifications of the vehicle.
* **Owner Type**: Number of previous owners.

## 🛠️ Tech Stack
* **Language:** Python
* **ML Framework:** `Scikit-learn`
* **Data Processing:** `Pandas`, `NumPy`
* **Serialization:** `Pickle` (for model deployment)

## 📈 Model Performance
After testing various regression algorithms (Linear Regression, Decision Trees, and Random Forest), the final model achieved:



| Metric | Value |
| :--- | :--- |
| **Model Score ($R^2$)** | **87%** |
| **Algorithm Used** | [Insert Algorithm Name, e.g., Random Forest Regressor] |

## 💾 Model Deployment
The final model has been serialized into a `.pkl` file for easy integration into web applications or APIs.

### How to use the saved model:
```python
import pickle

# Load the saved model
with open('model.pkl', 'rb') as file:
    model = pickle.load(file)

# Make a prediction
# Features: [Year, Mileage, Fuel_Type_Encoded, etc.]
prediction = model.predict([[2022, 15000, 1, 0, 120]])
print(f"Predicted Sales Price: ${prediction[0]:.2f}")
