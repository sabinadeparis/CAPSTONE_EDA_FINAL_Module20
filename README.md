This repository contains PA 20.1
https://github.com/sabinadeparis/CAPSTONE_EDA_FINAL_Module20.git

PLEASE NOTE:
Please note, as previously discussed and agreed, my certification is sponsored by my company; therefore, I am required to complete the capstone project using an internal business use case.
Due to company confidentiality policies, I am not authorized to share the original dataset. However, I can provide a detailed description of the data, methodology, and results obtained throughout the project.

OVERVIEW
Life insurance companies must accurately project future policy lapses (surrenders) to ensure financial stability, precise budgeting, 
and compliance with stringent European regulatory frameworks like Solvency II (S2) and IFRS 17. 
If an insurance company underestimates surrenders, it may face sudden liquidity shocks (not having enough cash on hand to pay out exiting policyholders). 
If it overestimates them, it miscalculates its technical provisions and unnecessarily locks up capital that could otherwise be invested. 
The core objective of this capstone is a binary classification challenge: Predict whether a given policyholder will surrender (Yes = 1) or stay active (No = 0) 
within a given year, based on a mix of structural customer data and high-frequency macroeconomic indicators.

MAIN FINDING 
The baseline model uses Logistic Regression with time-based splitting because it is fast, interpretable, and suitable for both numerical and categorical insurance features; a Decision Tree Classifier will also be tested.
The main evaluation metric is the F1-Score, supported by PR-AUC, since the dataset is highly imbalanced (many active policies vs few surrendered policies).
Accuracy and ROC-AUC are not reliable here because a model predicting “no surrender” for all customers could still achieve very high accuracy.
The F1-Score balances Precision and Recall: Precision reduces unnecessary retention actions, while Recall ensures actual surrender risks are detected.
For example, an F1-score of 0.65 with 70% Precision and 61% Recall means the model correctly identifies most real lapse risks while limiting false alarms.
