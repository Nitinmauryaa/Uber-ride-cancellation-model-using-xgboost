Predicting Uber Ride Cancellations
📌 Overview
This project aims to predict whether a booked Uber ride will be canceled before it begins, using only booking‑time information. Ride cancellations waste driver time, reduce revenue, and lower customer satisfaction. By applying machine learning models, we can identify high‑risk rides early and make proactive interventions such as notifying drivers or reallocating resources.

The models implemented include XGBoost and Random Forest, chosen for their strong performance and interpretability.

Problem Definition
Task: Binary Classification

Target Variable: target_customer_cancelled (1 = canceled, 0 = not canceled)

Challenge: The dataset is imbalanced (~7% cancellations), so recall and balanced evaluation metrics are crucial.

Dataset
The dataset includes detailed booking information such as:

Date and Time of booking

Pickup and Drop locations

Vehicle type and Ride distance

Driver Ratings and Customer Ratings

Payment Method

Booking Status (Completed, Canceled, Incomplete, No Driver Found, etc.)

Engineered Features: Hour, Day, Month, Weekday, Weekend Flag

👉 Only pre‑ride metadata was used to prevent target leakage.

Methodology
Data Preparation – Handling missing values, encoding categorical variables, creating time features.

Exploratory Data Analysis (EDA) – Understanding cancellation patterns across times, locations, and ratings.

Model Training – Random Forest and XGBoost applied with imbalance handling.

Model Evaluation – Metrics include Accuracy, Precision, Recall, F1, ROC‑AUC.

Interpretability – Feature importance to highlight key drivers of cancellations.

Results
XGBoost achieved the best performance for this imbalanced dataset.

Key predictors: time of booking, pickup location, customer/driver ratings.

Cancellations peak during certain hours and locations → targeted interventions can reduce inefficiency.

Tech Stack
Language: Python

Environment: Jupyter Notebook

Libraries: pandas, numpy, scikit‑learn, xgboost, matplotlib, seaborn

<img width="1880" height="935" alt="Screenshot 2025-08-18 120613" src="https://github.com/user-attachments/assets/4104b455-5ae4-4462-ab56-69c33196549d" />
