# **Fake Profile Detection using LightGBM & Optuna**

## **Overview**
This project trains a **LightGBM** model to detect **fake profiles** using Instagram account features. Hyperparameters are optimized with **Optuna** for best performance.

---

## **Setup**
Install dependencies:
```bash
pip install lightgbm optuna pandas scikit-learn


---

Dataset

instagram_df_train: Training data with profile features.

instagram_df_test: Test data for predictions.


Features

Numerical: nums/length username, nums/length fullname, description length, #posts, #followers, #follows

Binary: profile pic, name==username, external URL, private

Target: fake (0 = Real, 1 = Fake)



---

Model Training

1. Preprocess Data – Scale numerical features, split train/validation.


2. Tune Hyperparameters – Use Optuna to optimize LightGBM.


3. Train Final Model – Apply early stopping to prevent overfitting.


4. Make Predictions – Predict fake vs. real profiles.




---

Evaluation

F1-score – Optimized for balanced classification.

Binary Log Loss – Used for model validation.

Early Stopping – Prevents overfitting.