# Bank Term Deposit Subscription Prediction (XGBoost)

This project solves a binary classification problem from the **Kaggle Playground Series**, where the goal is to predict whether a bank client will subscribe to a term deposit.  
The solution uses **XGBoost**, a powerful gradient boosting algorithm, and is evaluated using **ROC-AUC**.

---

## 📌 Problem Statement

Given client-related features from a banking dataset, predict the **probability** that a client will subscribe to a bank term deposit.

- **Target Variable:** `y`  
  - `1` → Client subscribes  
  - `0` → Client does not subscribe
- **Evaluation Metric:** ROC-AUC
- **Output:** Probability of subscription for each test sample

---

## 📂 Dataset

The dataset consists of three files:

- `train.csv` → Training data with features and target (`y`)
- `test.csv` → Test data with features only
- `sample_submission.csv` → Sample format for submission

> The datasets are synthetically generated but preserve real-world feature semantics.

---

## 🛠️ Technologies Used

- Python 3
- Pandas
- NumPy
- Scikit-learn
- XGBoost

---

## 🔄 Machine Learning Pipeline

1. Data Loading
2. Exploratory Data Inspection
3. Feature–Target Separation
4. One-Hot Encoding for Categorical Variables
5. Train–Validation Split (Stratified)
6. Model Training using XGBoost
7. Model Evaluation using ROC-AUC
8. Retraining on Full Dataset
9. Test Prediction
10. Submission File Generation

---

## 🚀 Model Used

### XGBoost Classifier
- Handles non-linear relationships
- Performs well on tabular data
- Outputs probabilities required for ROC-AUC

Key parameters:
- `n_estimators = 300`
- `max_depth = 6`
- `learning_rate = 0.05`
- `subsample = 0.8`
- `colsample_bytree = 0.8`

---

## 📊 Evaluation Metric

**ROC-AUC (Receiver Operating Characteristic – Area Under Curve)**  
- Measures how well the model separates positive and negative classes
- Threshold-independent
- Suitable for imbalanced datasets

---

## 📁 Project Structure

├── train.csv
├── test.csv
├── sample_submission.csv
├── xgb_submission.csv
├── xgboost_model.py
└── README.md


---

## ▶️ How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/bank-term-deposit-xgboost.git
Install dependencies:

pip install pandas numpy scikit-learn xgboost
Run the script:

python xgboost_model.py
Upload xgb_submission.csv to Kaggle.

✅ Output
A valid Kaggle submission file:

xgb_submission.csv
Contains:

id → Test sample identifier

y → Predicted probability of subscription

🧪 Results
The XGBoost model achieves a higher ROC-AUC compared to baseline Logistic Regression.

Suitable as a strong baseline for Kaggle leaderboard improvement.

📌 Conclusion
This project demonstrates a complete end-to-end machine learning workflow for a real-world inspired classification problem.
XGBoost effectively captures complex feature interactions and improves predictive performance.

🙌 Acknowledgements
Kaggle Playground Series

Scikit-learn & XGBoost documentation

📜 License
This project is for educational and research purposes.

