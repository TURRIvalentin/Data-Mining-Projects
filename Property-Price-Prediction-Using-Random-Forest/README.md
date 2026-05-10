# Property Price Prediction in Buenos Aires 🏡📊

## 📌 Project Overview
This project focuses on predicting real estate prices in Buenos Aires (Capital Federal) using machine learning techniques. The core objective is to build a robust predictive model that estimates property prices based on features such as location, property type (House, Apartment, Parking), total surface area, and number of rooms. 

This repository contains an end-to-end Data Mining pipeline, from data ingestion and cleaning to feature engineering and predictive modeling using Random Forest.

## 🛠️ Tech Stack & Tools
- **Language:** Python 3
- **Libraries:** Pandas, NumPy, Scikit-Learn
- **Environment:** Jupyter Notebook / Google Colab
- **Algorithms:** Random Forest Regression

## 🧹 Data Processing & Feature Engineering
Real-world datasets are rarely clean. A significant portion of this project focuses on Data Preprocessing (AID & MD):
1. **Filtering & Standardization:** Filtered out properties outside Capital Federal and standardized all transaction currencies to USD (converting ARS using historical exchange rates).
2. **Missing Value Imputation:** 
   - Estimated missing `bedrooms` based on `rooms` (and vice versa).
   - Calculated missing `bathrooms` as the difference between rooms and bedrooms.
   - Mutually imputed `surface_total` and `surface_covered` to avoid dropping valuable records.
3. **Location Engineering:** Mapped micro-neighborhoods (e.g., "Distrito Audiovisual" -> "Chacarita") and grouped properties by location (`l3`, `l4`) to calculate the average price per square meter, avoiding outliers.

## 🤖 Modeling & Results
The core predictive model is built using a **Random Forest Regressor**. Random Forest was chosen for its ability to handle non-linear relationships and its robustness against overfitting in tabular data. 
*(For detailed hyperparameter tuning and evaluation metrics such as RMSE or MAE, please refer to the Jupyter Notebook outputs).*

## 🚀 How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/TURRIvalentin/Data-Mining-Projects.git
   ```
2. Navigate to this specific project directory.
3. Install the required dependencies:
   ```bash
   pip install pandas scikit-learn jupyter
   ```
4. Run the Jupyter Notebook:
   ```bash
   jupyter notebook "Property Price Prediction Using Random Forest.ipynb"
   ```

---
*Developed by Valentín Turri as part of the Master's in Data Mining & Knowledge Discovery (UBA).*
