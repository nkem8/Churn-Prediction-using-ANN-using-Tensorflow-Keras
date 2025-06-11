# 📊 Customer Churn Prediction using Artificial Neural Network (ANN)

This project applies deep learning techniques to predict customer churn in the telecom industry using the Telco Customer Churn dataset. The goal is to identify customers who are likely to cancel their services so that proactive retention strategies can be implemented.

---

## 📁 Dataset Overview

- **Source**: Telco-Customer-Churn.csv  
- **Rows**: 7,043  
- **Columns**: 21 (including customer demographics, service plans, billing info, and churn labels)  
- **Target**: `Churn` (Yes/No)

---

## 🧠 Model Overview

The project builds an Artificial Neural Network (ANN) using TensorFlow and Keras to classify churn based on customer attributes. Both training and validation sets are used to assess generalization and detect overfitting.

---

## 🔧 Project Workflow

1. **Data Preprocessing**
   - Handled missing values in `TotalCharges`
   - Dropped `customerID`
   - Label encoded binary categorical features
   - One-hot encoded multiclass categorical features
   - Scaled numerical features (`tenure`, `MonthlyCharges`, `TotalCharges`)

2. **Model Development**
   - ANN with 2 hidden layers using ReLU activation
   - Dropout regularization to reduce overfitting
   - Sigmoid activation in the output layer for binary classification

3. **Training**
   - 50 epochs
   - Validation set split from training set
   - Optimizer: Adam
   - Loss: Binary Crossentropy

4. **Evaluation**
   - Accuracy, Precision, Recall, F1-Score
   - Confusion Matrix and Classification Report

---

## 📈 Results

- **Test Accuracy**: ~80%
- **Churn Class Precision**: 64%
- **Churn Class Recall**: 53%
- The model was able to correctly classify most non-churners, but recall for churners was moderate, indicating opportunity for further optimization.

---

## ✅ Conclusion

The ANN model showed strong performance and was able to identify patterns associated with customer churn. Regularization helped address overfitting, and evaluation metrics showed that while overall accuracy was good, the model could benefit from improvements in recall for the positive class (churn).

---

## 💡 Recommendations

- Apply class weighting or SMOTE to improve recall for churners
- Tune model hyperparameters using grid search or KerasTuner
- Explore ensemble models (e.g., Random Forest, XGBoost)
- Integrate the model with business tools for real-time churn prediction

---
