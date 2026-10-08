# Heart Failure Death Event Prediction

## 📌 Project Overview

This project focuses on predicting the death event of patients with heart failure using machine learning classification techniques.

The dataset is analyzed, preprocessed, balanced using SMOTE, and used to train multiple machine learning classification models. The models are then evaluated and compared to identify the best-performing model.

## 🎯 Objective

The main objective of this project is to build a machine learning model that can predict whether a patient belongs to the death event class (`0` or `1`).

## 📂 Project Structure

```text
heart-failure-prediction/
│
├── data/
│   ├── train.csv
│   └── test.csv
│
├── notebooks/
│   └── heart_failure_prediction.ipynb
│
├── prediction_results.csv
│
└── README.md
```

## 🔄 Project Workflow

The project follows these steps:

1. Dataset Loading
2. Exploratory Data Analysis (EDA)
3. Missing Value Analysis
4. Duplicate Record Analysis
5. Feature Correlation Analysis
6. Data Preprocessing
7. Train-Test Split
8. Feature Scaling using StandardScaler
9. Class Balancing using SMOTE
10. Model Training
11. Model Evaluation
12. Model Comparison
13. Best Model Selection
14. Final Prediction

## 🤖 Machine Learning Models

The following classification models were trained and evaluated:

- Logistic Regression
- Decision Tree
- Support Vector Machine (SVM)
- Gaussian Naive Bayes
- Multi-Layer Perceptron (MLP)

## 📊 Model Performance

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 89.58% | 75.00% | 100.00% | 85.71% |
| Decision Tree | 66.67% | 47.37% | 60.00% | 52.94% |
| SVM | 85.42% | 72.22% | 86.67% | 78.79% |
| Gaussian Naive Bayes | 85.42% | 75.00% | 80.00% | 77.42% |
| MLP | 83.33% | 68.42% | 86.67% | 76.47% |

## 🏆 Best Model

Based on the evaluation results, **Logistic Regression** achieved the best overall performance.

Performance:

- **Accuracy:** 89.58%
- **Precision:** 75.00%
- **Recall:** 100.00%
- **F1 Score:** 85.71%

Logistic Regression was selected as the final model and was used to generate predictions for the external test dataset.

## ⚖️ Class Imbalance Handling

The target variable was imbalanced:

- Class `0`: 162 samples
- Class `1`: 77 samples

SMOTE (Synthetic Minority Over-sampling Technique) was applied only to the training data to balance the two classes.

After SMOTE:

- Class `0`: 129 samples
- Class `1`: 129 samples

## 📁 Prediction Results

The final predictions generated using the selected Logistic Regression model are stored in:

```text
prediction_results.csv
```

The external test dataset contains 60 patient records, and predictions were generated for all 60 records.

## 🛠️ Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- Google Colab / Jupyter Notebook

## 🚀 How to Run

1. Clone or download this repository.
2. Open the notebook:

```text
notebooks/heart_failure_prediction.ipynb
```

3. Install the required Python libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn imbalanced-learn
```

4. Run the notebook from beginning to end.

## 📌 Note

The model performance reported in this repository is based on the train-validation split and preprocessing workflow used in the notebook.

This project is intended for educational and machine learning practice purposes and should not be considered a clinical decision-making system.
