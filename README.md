# Phishing Attack Detection using Machine Learning

## Project Overview
Phishing remains one of the most widespread and damaging cybersecurity threats, targeting users through deceptive URLs and websites. Traditional blacklist and rule-based methods often fail against evolving phishing tactics.  

This project applies **machine learning techniques** to detect phishing URLs, offering a scalable and adaptive defense. The pipeline integrates **data preprocessing, feature engineering, model training, and evaluation**, with a focus on balancing accuracy, precision, and recall.

## ⚙️ Features & Methodology

### Dataset
- Combined multiple public phishing datasets: **PhishStrom-URL, ISCX-URL2016, Malicious URL Dataset**  
- Final cleaned dataset: **96,018 URLs** (balanced 50% phishing, 50% benign using SMOTE):contentReference[oaicite:1]{index=1}  

### Data Preprocessing
- Duplicate removal & null handling  
- Class balancing via **SMOTE**  
- Feature engineering:
  - **Length & count-based**: URL length, digit counts, special characters  
  - **Boolean flags**: suspicious TLDs, redirection, encoded URLs  
  - **Statistical metrics**: entropy, malicious probability  
- Feature selection via **correlation filtering** and **Random Forest importance**  

### Models Implemented
- Logistic Regression  
- Decision Trees  
- Random Forest  
- Gradient Boosting  
- XGBoost  
- LightGBM  
- **Ensemble Methods**: Stacking & Soft Voting  

---

## 📊 Results
- **Best model**: **XGBoost**, achieving:
  - **Accuracy** > 95%  
  - **Precision** ~94.8%  
  - **Recall** ~86%  
  - **F1-score** ~87%  
  - **ROC-AUC** ~0.98:contentReference[oaicite:2]{index=2}  
- **Ensemble Stacking** also performed strongly, balancing false positives and negatives.  

---

