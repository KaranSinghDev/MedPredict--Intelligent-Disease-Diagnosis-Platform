# Disease Prediction Model Using Patient Profile and Symptom Data

## Description
This project develops an XGBoost-based predictive model trained on patient symptoms and demographic data to classify diseases. By applying SMOTE for balancing rare classes, the model achieves high accuracy across multiple disease categories, providing a streamlined solution for diagnosis based on symptoms and patient characteristics.

## Problem
In healthcare, early and accurate diagnosis is critical yet often complicated by similar symptoms across different diseases, rare conditions, and imbalanced data. Manual diagnosis can lead to delays and inconsistencies, particularly in complex cases.

## Solution
The Disease Prediction Model uses machine learning to predict diseases based on patient symptoms and demographic attributes, enhancing diagnostic accuracy and efficiency. Through SMOTE for data balancing and an XGBoost classifier, it achieves robust performance, outperforming manual diagnostics in consistency and helping reduce errors.

## Dataset Description
The dataset includes a comprehensive range of symptoms and patient attributes:
- **Columns**:
  - **Symptoms**: Fever, Cough, Fatigue, Difficulty Breathing (Yes/No format)
  - **Demographic Features**: Age, Gender
  - **Health Indicators**: Blood Pressure (Normal/High), Cholesterol Level (Normal/High)
  - **Target**: Disease label based on diagnosis
- **Source**: [Kaggle Disease Symptoms and Patient Profile Dataset](https://www.kaggle.com/datasets/uom190346a/disease-symptoms-and-patient-profile-dataset)

## Model
- **Algorithm**: XGBoost Classifier with `multi:softmax` objective for multi-class classification.
- **Hyperparameters**:
  - `n_estimators`: 100
  - `learning_rate`: 0.05
  - `eval_metric`: merror
- **Resampling**: **SMOTE** (k=3) for addressing class imbalance.
- **Cross-validation**: 50-fold, ensuring consistent accuracy.

## Evaluation
- **Cross-validation Mean Accuracy**: 0.87
- **Validation Set Accuracy**: 90%
- **Classification Report**: 

   | Metric       | Precision | Recall | F1-Score |
   |--------------|-----------|--------|----------|
   | Accuracy     | -         | -      | **0.90** |
   | Macro Avg    | **0.89**  | **0.90** | **0.89** |
   | Weighted Avg | **0.90**  | **0.90** | **0.90** |
