# XGBoost Regression: Predicting House Prices 🧠

## Project Overview 📌 

This project demonstrates the end-to-end implementation of a **regression pipeline** using **XGBoost** to predict house prices. The process includes data preprocessing, model training, hyperparameter tuning, performance evaluation, and feature importance analysis.

## Dataset 📁 
* The dataset used contains various features related to housing (e.g., number of rooms, location, square footage, etc.).
* The target variable is the **house price**.

## Technologies Used ⚙️
* Python 3
* Jupyter Notebook
* pandas, numpy, matplotlib, seaborn
* scikit-learn
* xgboost

## Workflow 🔄 

**1. Data Preprocessing**
* Missing values handled
* Categorical variables encoded
* Numerical features scaled
* Feature selection via **.var()** and correlation analysis
* Final dataset: **X_train_reduced, y_train, X_test, y_test**

**2. Model Building**
* **XGBRegressor** was wrapped inside a **Pipeline** object
* Pipeline included preprocessing and the model

**3. Model Evaluation**
* Evaluated on the test set using:
* **Mean Squared Error**
* **R² Score**
* Visualized predictions with a Real vs Predicted scatter plot

**4. Cross-Validation**
* Applied 5-Fold Cross Validation using cross_val_score
* Achieved an average R² of ~0.82

**5. Hyperparameter Tuning**
* Used GridSearchCV with the following param grid:
param_grid = {
    'xgbregressor__n_estimators': [100, 200],
    'xgbregressor__max_depth': [3, 5, 7]
}
* Best params:
     * n_estimators = 100
     * max_depth = 3
* Best R² from Grid Search: 0.863

**6. Feature Importance**
* Feature importance values were extracted and plotted
* Top features were interpreted visually

## Results 📊 
* **Test R² Score: ~0.88**
* **Cross-Validated R² Score: ~0.82**
* Model shows **strong predictive power** with good generalization
* Key features driving the predictions were identified
