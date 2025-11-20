<p align="center">
  <img src="assets/banner_airbnb.png" alt="Airbnb Revenue Optimization Banner" width="100%">
</p>

# 🔥 Airbnb Revenue Optimization: Decision Models + Machine Learning  
**Author:** Cecilia Ledesma  
**GitHub:** https://github.com/ceciagro  
**Role:** Data Scientist – Professional Portfolio Project  

## 🔗 Dataset Source

This project uses the public **Airbnb NYC Open Data** provided by *Inside Airbnb*.

- Source: https://insideairbnb.com/get-the-data/  
- File used: **listings.csv.gz** (Detailed Listings Data – NYC)
- License: Open access for research and educational purposes  
- Notes: The dataset was cleaned before analysis (missing values, feature selection, demand segmentation).
---

## 🚀 1. Project Overview

This project combines **Decision Analysis**, **Uncertainty Modeling**, and **Machine Learning** using real Airbnb NYC data.

The primary business question is:

### **“How many rental units should a host offer to maximize monthly revenue under uncertain demand?”**

To answer this, the project follows an end-to-end analytical workflow:

- Exploratory data analysis and demand segmentation  
- Construction of payoff matrices  
- EMV (Expected Monetary Value)  
- EVPI (Expected Value of Perfect Information)  
- Decision Tree classifier  
- XGBoost advanced model  
- SHAP interpretability  
- Fully reproducible ML pipeline  

This project is designed to demonstrate senior-level analytical thinking, modeling ability, and decision-science expertise for Data Scientist roles.

---

## 📊 2. Dataset

The dataset is a cleaned subset of the publicly available **Airbnb NYC Listings**.

Relevant features:

- `latitude`, `longitude`  
- `minimum_nights`  
- `availability_365`  
- `number_of_reviews`, `reviews_per_month`  
- `room_type`  
- `neighbourhood_group`  
- `price`  

Dataset size: **36,111 listings**.

---

## 🧠 3. Decision Models Under Uncertainty

The analysis begins with a structured decision-making framework that evaluates revenue outcomes under different demand scenarios.

### ✔️ Demand states  
- Low demand  
- Medium demand  
- High demand  

Demand was extracted from real pricing distribution using quantile segmentation.

### ✔️ Payoff Matrix (Data-Driven)

Based on real estimated occupancy and average price:

- **Low inventory** → 1 unit  
- **Medium inventory** → 3 units  
- **High inventory** → 5 units  

### ✔️ EMV (Expected Monetary Value)

| Decision         | EMV (USD) |
|------------------|-----------|
| Low inventory    | 56.83     |
| Medium inventory | 170.51    |
| **High inventory** | **284.18** |

**Optimal strategy:** **High inventory (5 units)**.

---

## ✔️ EVPI (Expected Value of Perfect Information)

The EVPI measures how valuable it would be to know future demand perfectly before choosing an inventory strategy.

Steps included:

1. Best payoff per demand state  
2. Empirical demand probabilities  
3. Expected Value with Perfect Information (EVwPI)  
4. EVPI = EVwPI − EMV_current  

This helps determine whether investing in forecasting systems would be justified.

---

## 🌲 4. Decision Tree Classifier

A Decision Tree model was trained to classify demand states.

Pipeline includes:

- Train/test split  
- `ColumnTransformer` preprocessing  
- One-hot encoding  
- Model training and evaluation  
- Feature importance visualization  
- Graphviz decision tree export  

---

## ⚡ 5. XGBoost Advanced Model

To achieve a higher-performance predictive model, XGBoost was implemented.

Highlights:

- Integrated preprocessing pipeline  
- Hand-tuned hyperparameters  
- Classification report  
- Confusion matrix  
- Improved accuracy and stability  

---

## 🔍 6. Model Explainability with SHAP

Explainability is key in professional ML workflows.

SHAP analysis includes:

- Summary plot of global feature importance  
- Bar plot ranking predictors  
- Per-feature SHAP decomposition  
- Interpretation of model behavior  

This demonstrates expert-level transparency and interpretability.

---

## 📁 7. Project Structure

decision_models_project/
│
├── notebooks/
│   └── decision_tree_emv.ipynb
│
├── listings.csv
├── README.md
├── requirements.txt
└── .gitignore

---

## 🧪 8. Tech Stack

- Python 3.11  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- SHAP  
- Matplotlib, Seaborn  
- Graphviz  
- Jupyter Notebook  

---

## 🎯 9. Key Results

- Optimal inventory strategy: **High inventory (5 units)**  
- XGBoost significantly improves prediction  
- SHAP provides transparent explanations  
- Combined decision-science + ML approach  

---

## 👩‍💻 10. How to Run This Project

```bash
git clone https://github.com/ceciagro/decision_models_project.git
cd decision_models_project

python3 -m venv .venv
source .venv/bin/activate    # macOS / Linux

pip install -r requirements.txt

jupyter notebook

notebooks/decision_tree_emv.ipynb
```

## 📬 11. Professional Contact

**Name:** Cecilia Ledesma  
**GitHub:** https://github.com/ceciagro  
**Email:** cecledesma@gmail.com 
**Location:** Argentina (available for fully remote roles)

### 🔎 Open to:
- Data Scientist (Junior–Mid)
- Machine Learning Engineer (Junior)
- Data Analyst (Advanced SQL + Python)
- AI/ML freelance projects
- Remote roles in US/EU companies
- Contract or long-term engagements

### 🎯 Specializations:
- Machine Learning (Scikit-learn, XGBoost, SHAP)
- Decision Science & Optimization
- NLP (Transformers, summarization, feature extraction)
- Financial modeling & forecasting
- Geospatial Analysis (GIS, Remote Sensing)
- Dashboarding (Streamlit, Power BI, Python)

### 🧩 Strengths:
- End-to-end ML project development
- Clean, reproducible pipelines
- Excellent documentation and communication
- Strong analytical foundation (statistics + modeling)
- High adaptability + rapid learning curve
- Professional portfolio with real, applied projects
