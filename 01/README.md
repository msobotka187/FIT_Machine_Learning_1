# Task 01: Car Price Prediction & Regression Analysis

## 🎯 Objective
The primary goal of this project is to build a robust regression pipeline to predict the selling price (`Price`) of used automobiles. This task emphasizes handling messy, real-world data containing mixed feature types, missing values, and embedded units (e.g., extracting numeric engine displacement from text).

## 📊 Dataset Information
The project utilizes a dataset of vehicle sales (`data.csv` for training/validation and `evaluation.csv` for final blind predictions). 

**Key Features Include:**
* **Categorical:** Make, Model, Fuel Type, Transmission, Location, Color, Owner, Seller Type, Drivetrain.
* **Numerical/Text-Mixed:** Year, Kilometer, Engine (cc), Max Power, Max Torque, Dimensions (Length/Width/Height), Seating/Fuel Capacity.

## 🛠️ Project Pipeline

### 1. Data Preprocessing & EDA
* **Data Splitting:** Implemented a rigorous Train/Validation/Test split to prevent data leakage and ensure fair model evaluation.
* **Feature Engineering:** Extracted raw numerical values from string-based features (e.g., parsing "1500 cc" from the `Engine` column).
* **Missing Value Imputation:** Handled missing data points using methodical, non-leaky imputation strategies.
* **Scaling & Encoding:** Applied appropriate normalization techniques (Standardization/Min-Max Scaling) and encoded categorical variables for machine learning compatibility.

### 2. Model Selection & Hyperparameter Tuning
Four regression algorithms were evaluated to determine the best fit for this specific dataset. Each model underwent hyperparameter tuning optimized against **Mean Squared Error (MSE)** on the validation set.

* **Decision Tree Regressor:** Capturing non-linear relationships.
* **k-Nearest Neighbors (kNN):** Leveraging feature scaling to find similar vehicle profiles.
* **Linear Regression:** Establishing a baseline linear relationship.
* **Ridge Regression:** Applying L2 regularization to handle potential multicollinearity among car features.

### 3. Final Evaluation
The final model was selected based on validation performance. We estimated its generalization error using **Root Mean Squared Error (RMSE)** on the hold-out test set, ensuring the model's predictive power on unseen data.

## 🚀 Results & Predictions
* **Target Metric:** The objective was to achieve an RMSE strictly below **765,000** on the blind evaluation data.
* **Final Output:** The optimal model was used to predict prices for `evaluation.csv`, and the outputs were formatted and saved to `results.csv` (mapping `ID` to predicted `Price`).

> **Note on Methodology:** Detailed explanations, architectural choices, and visualizations are thoroughly documented within the Markdown cells of the Jupyter Notebook to ensure full reproducibility and clear methodology.
