## 🚗 Predicción de Precios de Coches de Segunda Mano

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com/?lines=Machine+Learning+with+R&center=true&width=850&height=45" alt="Typing SVG">
</p>

### 📌 Project Overview

This project aims to build a **machine learning model to predict the price of second-hand vehicles** using a real dataset from the Indian market.

The goal is to develop a **decision-support tool for car dealerships**, helping them estimate fair market prices based on vehicle characteristics.

The project includes:

- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Feature engineering
- Model training and comparison
- Model evaluation

➢ The best-performing model achieved an **R² score of 0.8621 on the test dataset**.

### 🗂️ El Dataset
We used the `car_price.csv` dataset, which contains around 7,400 records of used vehicles and 18 columns. Some of the key variables analyzed include:
* `yr_mfr`: Year of manufacture.
* `kms_run`: Kilometers driven.
* `body_type` and `fuel_type`: Body type and fuel type.
* `sale_price`: Our target variable.

### 🔄 Project Workflow

1. **Data Cleaning**
   - Handling missing values
   - Removing inconsistencies
   - Formatting variables

2. **Exploratory Data Analysis**
   - Distribution analysis
   - Correlation analysis
   - Visualization of key features

3. **Feature Engineering**
   - Encoding categorical variables
   - Feature selection

4. **Model Training**
   - StepBIC Regression
   - Decision Trees
   - Random Forest
   - Gradient Boosting

5. **Model Evaluation**
   - R²
   - RMSE
   - Cross-validation


### 📊 Principal Results
After evaluating the performance metrics on the training and test sets, the ensemble models demonstrated clear superiority:

* **Regresión StepBIC:**
  - $R^2$ Train = 0.7034 
  - $R^2$ Test = **0.7044** (No overfitting, but low predictive power).
* **Penalized model: (ENET-LASSO):** 
  - $R^2$ Train = 0.6850
  - $R^2$ Test = **0.6796**
* **Árbol Podado:**
  - $R^2$ Train = 0.6571.
  - $R^2$ Test = **0.6282.**
* **Random Forest:**
  - $R^2$ Train = 0.9066 
  - $R^2$ Test = **0.8475** 
* **🏆Gradient Boosting:** (Achieved best results, providing strong predictive performance without significant overfitting).
  - $R^2$ Train = 0.9150
  - $R^2$ Test = **0.8621**

> **Business Conclusion:** As the manufacturing year increases (newer vehicles), the average predicted value consistently rises across all body types. The *Gradient Boosting* model is the ideal candidate for deployment at the dealership. Besides achieving the best results in terms of predictive performance, the underlying complexity of this type of Machine Learning model allows for better adaptation to this kind of decision-making process.

---
*Work done by: Marcos Martínez, Laura López, Marina Parra, Verónica Yebra y Rodrigo Castillo.*
