# Credit Card Fraud Detection

### Project Overview
This project builds and evaluates supervised and unsupervised machine learning models to detect fraudulent credit card transactions.  
The dataset is **highly imbalanced**, making fraud detection challenging and requiring techniques such as resampling and anomaly detection.

The goal is to compare traditional supervised classification with unsupervised anomaly detection for real-world fraud prevention use cases.

---

### Objectives
- Detect fraudulent transactions with high recall and minimal false positives  
- Compare supervised (XGBoost, Logistic Regression) vs. unsupervised (Isolation Forest) models  
- Handle extreme class imbalance using SMOTE and class-weighting  
- Evaluate performance using ROC-AUC, Precision-Recall, and confusion matrix  

---

### Methods & Tools
- **Python, scikit-learn, XGBoost, pandas, NumPy**
- **Techniques:**
  - Train/test pipeline with stratified splits  
  - SMOTE oversampling  
  - Isolation Forest anomaly detection  
  - Feature engineering and scaling  
  - Model comparison using ROC-AUC and PR curves  

---

### Model Development Steps
1. **Data Cleaning & Exploration**  
   Identified correlations, missing values, and distribution differences between fraud and non-fraud classes.

2. **Feature Engineering**  
   Created new features (e.g., transaction velocity, amount ratios) and scaled numerical attributes.

3. **Supervised Learning**  
   - Logistic Regression (baseline)  
   - XGBoost with tuned hyperparameters and class imbalance adjustments  

4. **Unsupervised Anomaly Detection**  
   - Isolation Forest  
   - Local Outlier Factor (optional extension)

5. **Evaluation & Comparison**  
   Analysed ROC-AUC, PR curves, precision/recall trade-offs, and false positive behaviour.

---

### Results
| Model | ROC-AUC | Precision | Recall |
|--------|---------|-----------|---------|
| Logistic Regression | 0.94 | 0.73 | 0.81 |
| **XGBoost** | **0.98** | **0.87** | **0.92** |
| Isolation Forest | 0.86 | 0.42 | 0.78 |

**XGBoost delivered the strongest performance**, particularly in improving recall for the minority fraud class.

---

### Learning Outcomes
- Strengthened knowledge of handling **highly imbalanced fraud datasets**  
- Improved skills in anomaly detection and supervised vs. unsupervised comparison  
- Developed evaluation techniques relevant to real banking fraud teams  

---

### Future Improvements
- Add sequence-based fraud detection using LSTM  
- Deploy model as an API with FastAPI or Flask  
- Integrate SHAP for model explainability  
