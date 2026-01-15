Project: Retention Analysis & Churn Risk Scoring System
Objective: Developed an end-to-end machine learning pipeline to predict customer churn in e-commerce, focusing on probability calibration and risk ranking to optimize retention budget allocation.

Methodology & Innovation:

Walk-Forward Validation: Implemented a rigorous time-series cross-validation strategy (training on historical windows, testing on future "Out-of-Time" data) to prevent data leakage and simulate real-world deployment scenarios.

Probability Calibration: Applied Isotonic Regression (Random Forest) and Sigmoid Scaling (Logistic Regression/KNN) to transform raw model outputs into accurate churn probabilities, essential for calculating financial risk (Expected Loss).

Leakage Prevention: Utilized GroupKFold to ensure strict separation of customer data between training and validation sets.

Feature Engineering:

Engineered temporal features describing trend dynamics (e.g., spending velocity, inter-purchase time changes).

Created behavioral indicators (RFM, basket diversity, returns ratio) and aggregated metrics across dynamic time windows.

Results:

Top Performance: The Random Forest model achieved an Average Precision (PR-AUC) of ~0.96 on the Out-of-Time test set, demonstrating exceptional capability in ranking high-risk customers.

Model Comparison: Benchmarked Random Forest against calibrated Logistic Regression and KNN, establishing robustness across linear and non-linear approaches.

Business Output: Delivered a segmented customer list ("High Risk" vs. "Safe") ready for integration with Power BI for actionable reporting.

Technologies: Python, Scikit-learn (Pipeline, Calibration, GridSearchCV), Pandas, NumPy, Matplotlib/Seaborn.

Models Evaluated:

Random Forest (Best Performer, Isotonic Calibrated)

Logistic Regression (Balanced, Sigmoid Calibrated)

K-Nearest Neighbors (KNN)

Authors:

Kamil Antkiewicz

Marcel Świdziński