# Task 02: Heart Disease Classification & Custom Ensemble Learning

## 🎯 Objective
This project focuses on predicting the presence of heart disease in patients using a variety of classification algorithms. The core achievement of this task is the **from-scratch implementation of a Random Forest classifier**, demonstrating a deep understanding of ensemble methods, bagging, and feature subspace sampling.

## 📊 Dataset Information
The dataset comprises clinical patient data (`data.csv` for training/validation and `evaluation.csv` for blind testing).

**Clinical Features Include:**
* **Demographics:** Age, Sex.
* **Vitals & Labs:** Resting Blood Pressure, Cholesterol, Fasting Blood Sugar, Max Heart Rate.
* **Cardiac Metrics:** Chest Pain Type, Resting ECG results, Exercise Angina, Oldpeak (ST depression), ST_Slope.
* **Target Variable:** `Heart Disease` (1 = High Risk/Disease present, 0 = Normal).

## 🛠️ Project Pipeline

### 1. Data Preprocessing & EDA
* **Data Splitting:** Applied a rigorous Train/Validation/Test split to evaluate model generalization properly.
* **Feature Transformation:** Converted categorical variables (e.g., Chest Pain Type, Resting ECG) into machine-readable numerical formats using appropriate encoding techniques.
* **Scaling:** Experimented with Standardization/Min-Max scaling, specifically optimizing distance-based models like kNN.
* **Exploratory Visualizations:** Analyzed feature distributions and target correlations to inform preprocessing decisions.

### 2. Custom Algorithm Implementation & Model Selection
The focal point of this project was building and comparing ensemble and baseline models. Hyperparameters were rigorously tuned to maximize **Accuracy** on the validation set.

* **Custom Random Forest:** Implemented the core logic of the Random Forest algorithm from scratch, handling decision tree aggregation and randomized feature selection.
* **AdaBoost:** Utilized adaptive boosting to evaluate sequential ensemble performance.
* **Decision Tree:** Used as a standalone baseline for the ensemble methods.
* **k-Nearest Neighbors (kNN):** Evaluated as a distance-based baseline.
* **Logistic Regression:** Evaluated as a linear probability baseline.

### 3. Comprehensive Evaluation
To ensure the models were not just accurate but also robust across different thresholds and class balances, the following metrics were computed for the optimized models:
* **Accuracy & F1-Score**
* **Receiver Operating Characteristic (ROC) Curve**
* **Area Under the Curve (AUC)**

## 🚀 Results & Predictions
* **Target Metric:** The objective was to build a final model capable of exceeding an **80% accuracy** threshold on unseen clinical data.
* **Final Output:** The best-performing model (based on cross-validated metrics) was selected to evaluate the `evaluation.csv` dataset. Predictions were exported to `results.csv`, mapping patient `ID` to the predicted `HeartDisease` class.

> **Note on Methodology:** The Jupyter Notebook contains detailed Markdown commentary explaining architectural decisions, the mathematical intuition behind the custom Random Forest, and interpretations of the ROC/AUC visualizations.
