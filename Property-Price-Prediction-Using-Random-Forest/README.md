# Property Price Prediction in Buenos Aires

## Project Overview
This project focuses on predicting real estate prices in Buenos Aires (Capital Federal) using machine learning techniques. The core objective is to build a robust predictive model that estimates property prices based on features such as location, property type (House, Apartment, Parking), total surface area, and number of rooms. 

This repository contains an end-to-end Data Mining pipeline, from data ingestion and cleaning to feature engineering and predictive modeling using Random Forest.

## Tech Stack & Tools
- Language: Python 3
- Libraries: Pandas, NumPy, Scikit-Learn
- Environment: Jupyter Notebook / Google Colab
- Algorithms: Random Forest Regression

## Data Processing & Feature Engineering
Real-world datasets are rarely clean. A significant portion of this project focuses on Data Preprocessing:
1. Filtering & Standardization: Filtered out properties outside Capital Federal and standardized all transaction currencies to USD.
2. Missing Value Imputation: Estimated missing bedrooms based on rooms, calculated bathrooms, and mutually imputed surface areas.
3. Location Engineering: Mapped micro-neighborhoods and grouped properties by location to calculate the average price per square meter.

## Modeling & Results
The core predictive model is built using a Random Forest Regressor. Random Forest was chosen for its ability to handle non-linear relationships and its robustness against overfitting in tabular data.

## How to Run the Project
1. Navigate to this specific project directory.
2. Install the required dependencies: pip install pandas scikit-learn jupyter
3. Run the Jupyter Notebook: jupyter notebook "Property Price Prediction Using Random Forest.ipynb"

---
Developed by Valentín Turri as part of the Master's in Data Mining & Knowledge Discovery (UBA).
