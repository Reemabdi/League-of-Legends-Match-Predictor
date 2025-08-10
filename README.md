# 🏆 League of Legends Match Predictor

This project predicts the outcome of League of Legends matches using **Logistic Regression** implemented in **PyTorch**.  
It processes match statistics, trains a binary classification model, and evaluates it using accuracy, confusion matrix, ROC curve, and feature importance.

---

## 📂 Features
- **Data Preprocessing**
  - Uses `pandas` & `scikit-learn` for cleaning and scaling features  
  - Splits dataset into training/testing sets  
- **Model**
  - Logistic Regression implemented from scratch with PyTorch  
  - L2 regularization with SGD optimizer  
- **Evaluation Metrics**
  - Accuracy (train & test)  
  - Confusion Matrix  
  - Classification Report  
  - ROC Curve & AUC  
  - Feature Importance Visualization  

---

## 📊 Dataset
The dataset contains match-level features:
- `gold_earned`
- `damage_dealt`
- `wards_killed`
- `deaths`
- `assists`
- `wards_placed`
- `kills`
- `cs`

**Target:** Binary label (0 = loss, 1 = win).

---
🚀 Model Training
-----------------
1. Load and preprocess the dataset.
2. Scale features using StandardScaler.
3. Convert data to PyTorch tensors.
4. Train Logistic Regression with SGD & L2 regularization.

📈 Results
----------
Training Accuracy: ~51.5%  
Testing Accuracy: ~44.5%

Confusion Matrix  
ROC Curve  
Feature Importance  

📌 Observations
---------------
- The dataset may be imbalanced or features may not be sufficient for high accuracy.
- ROC AUC (~0.44) suggests poor discriminatory power — further feature engineering or model tuning is needed.
- Top predictive features: gold_earned, damage_dealt, deaths.

🛠️ Next Improvements
----------------------
- Try more complex models (Random Forest, XGBoost, Neural Networks)
- Perform feature engineering (e.g., ratios, normalized stats)
- Tune hyperparameters with grid search
- Handle class imbalance with oversampling or weighting
----------------
requirements.txt
----------------
pandas
numpy
scikit-learn
torch
matplotlib
seaborn
## ⚙️ Installation & Setup
```bash
# Clone repository
git clone https://github.com/your-username/league-of-legends-match-predictor.git
cd league-of-legends-match-predictor

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook League_of_Legends_Match_Predictor.ipynb


