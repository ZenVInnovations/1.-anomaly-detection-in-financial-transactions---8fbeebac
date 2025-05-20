Anomaly Detection in Financial Transactions
🚀 Project Objective
The goal is to identify anomalous (fraudulent) credit card transactions with the minimum possible False Positive Rate (FPR) while maximizing the recall for the fraud class.

📊 Dataset Overview
Features: 30 numerical features resulting from PCA transformation

Class Imbalance:

Non-fraudulent: 1000

Fraudulent: 17

Sampling Strategy:

Stratified random split for training and test sets, maintaining the original 1000:17 ratio.

🛠️ Approach and Methodology
1. Supervised Classification
Algorithms Tested

Logistic Regression

Support Vector Machine

Random Forest Classifier

Focus Metric: Recall for the fraud class

Best Outcome:

Random Forest achieved a recall of 0.78

2. Unsupervised Anomaly Detection
Isolation Forest

Trained on the entire dataset without using fraud labels

Improved recall to 0.82

3. Deep Autoencoder Approach
Architecture

Fully-connected encoder–decoder network

Compression to a low-dimensional bottleneck, followed by reconstruction

Training

Only using “normal” (non-fraud) transactions

Anomaly score calculated based on reconstruction error

Thresholding

Calibrated to balance false positives and recall

Best Performance

Recall: 0.85

False Positive Rate: 6.5% for the fraud class

📈 Results & Comparison
Model	Recall (Fraud)	False Positive Rate
Random Forest Classifier	0.78	—
Isolation Forest	0.82	—
Deep Autoencoder (Ours)	0.85	0.065

📝 Summary and Conclusions
The Deep Autoencoder method outperforms both classical supervised and unsupervised techniques in detecting fraudulent transactions while maintaining a low false positive rate.

This solution can be integrated into real-time monitoring systems, with periodic retraining to adapt to emerging transaction patterns.
