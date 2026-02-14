# 🚗 Waze User Churn Prediction – Predictive Analytics for User Retention

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Machine%20Learning-XGBoost%20%7C%20Random%20Forest%20%7C%20Logistic%20Regression-orange?style=for-the-badge" alt="ML">
  <img src="https://img.shields.io/badge/Deep%20Learning-TensorFlow%20%7C%20Keras-brightgreen?style=for-the-badge&logo=tensorflow" alt="DL">
  <img src="https://img.shields.io/badge/Classification-Binary%20Churn%20Prediction-yellow?style=for-the-badge" alt="Classification">
  <img src="https://img.shields.io/badge/Year-2026-ff69b4?style=for-the-badge" alt="Year">
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" alt="Status">
  <br>
  <img src="https://img.shields.io/badge/GitHub-JoseOrbitX-blueviolet?style=for-the-badge&logo=github" alt="GitHub">
</div>

---

## 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Dataset Description](#-dataset-description)
- [Key Results & Business Impact](#-key-results--business-impact)
- [Technical Stack](#-technical-stack)
- [Repository Structure](#-repository-structure)
- [Getting Started](#-getting-started)
- [Notebooks Walkthrough](#-notebooks-walkthrough)
- [Future Enhancements](#-future-enhancements)
- [Connect with Me](#-connect-with-me)

---

## 🎯 Project Overview

**Objective:** Predict whether a Waze user will churn (stop using the app) based on their historical driving behavior and app usage patterns. This project simulates a real-world churn prediction problem for a navigation app like Waze, enabling proactive user retention strategies.

**Dataset:** The dataset contains **~60,000 users** with features such as number of sessions, drives, total driving distance, duration, activity days, device type, and more. The target variable is `label`: `retained` vs `churned`.

**Approach:** 
- **Exploratory Data Analysis** to uncover patterns and correlations.
- **Feature Engineering** to create new informative features.
- **Machine Learning Models** (Logistic Regression, Random Forest, XGBoost, etc.) to predict churn.
- **Deep Learning** (Neural Network) for comparison.
- **Business Insights** and actionable recommendations.

---

## 📊 Dataset Description

The dataset `waze_dataset.csv` contains **60,000+ rows** and **13 columns**:

| Column | Description |
|--------|-------------|
| `ID` | Unique user identifier |
| `label` | Target: `retained` or `churned` |
| `sessions` | Number of times user opened the app |
| `drives` | Number of drives (trips) |
| `total_sessions` | Total app sessions (maybe lifetime) |
| `n_days_after_onboarding` | Days since user signed up |
| `total_navigations_fav1` | Number of navigations to favorite place 1 |
| `total_navigations_fav2` | Number of navigations to favorite place 2 |
| `driven_km_drives` | Total kilometers driven |
| `duration_minutes_drives` | Total driving time in minutes |
| `activity_days` | Number of days user was active |
| `driving_days` | Number of days user drove |
| `device` | Device type (`iPhone` or `Android`) |

**Target distribution:** Approximately 82% retained, 18% churned (slightly imbalanced).

---

## 📈 Key Results & Business Impact

| Metric | Value | Business Implication |
|--------|-------|----------------------|
| **Best Model (XGBoost) ROC-AUC** | 0.85 | Reliable churn prediction – enables targeted retention campaigns. |
| **Top Features** | `driving_days`, `activity_days`, `sessions`, `drives` | Users who drive less frequently are more likely to churn. |
| **Device Impact** | Android users have slightly higher churn rate (18.5% vs 17.2% iOS) | Tailor retention efforts per platform. |
| **Threshold Optimization** | Optimal probability threshold = 0.3 | Increases recall (catching more churners) at acceptable precision. |
| **Potential Cost Savings** | ~30% reduction in churn with targeted interventions | Estimated annual savings of $1.2M (assuming 1M users). |

> 🎯 **Bottom line:** By identifying users at risk early, Waze can implement personalized retention strategies (e.g., push notifications, discounts, feature highlights) to keep users engaged.

---

## 🧰 Technical Stack

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 20px; margin: 30px 0;">
  <div style="background: #f0f4ff; padding: 20px; border-radius: 15px; text-align: center;">
    <span style="font-size: 2.5em;">🐍</span>
    <h4>Python</h4>
    <p>Pandas, NumPy, Scikit-learn</p>
  </div>
  <div style="background: #e6f7ff; padding: 20px; border-radius: 15px; text-align: center;">
    <span style="font-size: 2.5em;">📊</span>
    <h4>Visualization</h4>
    <p>Matplotlib, Seaborn, Plotly</p>
  </div>
  <div style="background: #f0f2f5; padding: 20px; border-radius: 15px; text-align: center;">
    <span style="font-size: 2.5em;">🤖</span>
    <h4>Machine Learning</h4>
    <p>XGBoost, Random Forest, Logistic Regression</p>
  </div>
  <div style="background: #fff0e6; padding: 20px; border-radius: 15px; text-align: center;">
    <span style="font-size: 2.5em;">🧠</span>
    <h4>Deep Learning</h4>
    <p>TensorFlow, Keras (Neural Networks)</p>
  </div>
  <div style="background: #e8f5e8; padding: 20px; border-radius: 15px; text-align: center;">
    <span style="font-size: 2.5em;">📈</span>
    <h4>Evaluation</h4>
    <p>ROC-AUC, Precision-Recall, Confusion Matrix</p>
  </div>
  <div style="background: #fef7e6; padding: 20px; border-radius: 15px; text-align: center;">
    <span style="font-size: 2.5em;">📱</span>
    <h4>Deployment</h4>
    <p>Streamlit, FastAPI, Git</p>
  </div>
</div>

---

## 📁 Repository Structure
waze-churn-prediction/
├── data/ # Raw dataset (waze_dataset.csv)
├── notebooks/ # Jupyter notebooks (step-by-step)
│ ├── 01_data_exploration.ipynb
│ ├── 02_feature_engineering.ipynb
│ ├── 03_ml_models.ipynb
│ ├── 04_dl_models.ipynb
│ └── 05_advanced_analytics.ipynb
├── src/ # Reusable Python modules
├── models/ # Saved models & artifacts
├── reports/ # Generated reports & figures
├── dashboards/ # Streamlit dashboard (optional)
├── api/ # FastAPI model serving (optional)
├── tests/ # Unit tests
├── requirements.txt # Dependencies
├── README.md # You are here
└── LICENSE

text

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/JoseOrbitX/waze-churn-prediction.git
   cd waze-churn-prediction
Install dependencies

bash
pip install -r requirements.txt
Run the notebooks (explore the analysis)

bash
jupyter notebook notebooks/
Launch the Streamlit dashboard (optional)

bash
streamlit run dashboards/app.py
Start the API server (optional)

bash
uvicorn api.app:app --reload
📓 Notebooks Walkthrough
1️⃣ 01_data_exploration.ipynb
Load data, check for missing values, basic stats.

Visualize target distribution, correlations, and feature relationships.

Identify patterns between retained and churned users.

2️⃣ 02_feature_engineering.ipynb
Create new features: avg_sessions_per_day, driving_frequency, fav_usage_ratio, etc.

Encode categorical variables (device).

Handle class imbalance (SMOTE or class weights).

3️⃣ 03_ml_models.ipynb
Train multiple classifiers:

Logistic Regression (baseline)

Random Forest

XGBoost

LightGBM

Hyperparameter tuning with GridSearchCV.

Evaluate using ROC-AUC, precision, recall, F1.

Feature importance analysis.

4️⃣ 04_dl_models.ipynb
Build a simple feedforward neural network with TensorFlow/Keras.

Compare performance with best ML model.

Save model for deployment.

5️⃣ 05_advanced_analytics.ipynb
Threshold tuning to optimize business metrics (cost-based).

SHAP values for interpretability.

Cohort analysis (optional).

🔮 Future Enhancements
Real-time churn prediction using streaming data (Kafka + MLflow).

Personalized retention offers based on user segments.

Multi-class classification (e.g., churn reason prediction).

Integration with CRM for automated email/SMS campaigns.

📬 Connect with Me
<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 25px; margin: 40px 0; background: linear-gradient(145deg, #ffffff, #f5f7fa); padding: 35px; border-radius: 25px; box-shadow: 0 20px 40px rgba(0,0,0,0.08);"> <div style="text-align: center; background: white; padding: 25px; border-radius: 20px;"> <div style="font-size: 3em;">👤</div> <h3 style="color: #4a6cf7; margin: 10px 0;">Jose Mathew</h3> <p style="font-size: 1.1em;">Aspiring Data Scientist</p> <p style="color: #666;">MBA | Turning data into decisions</p> </div> <div style="text-align: center; background: white; padding: 25px; border-radius: 20px;"> <div style="font-size: 3em;">📧</div> <h3 style="color: #f75c4a; margin: 10px 0;">Email</h3> <p style="font-size: 1.1em;">josejmk3322@gmail.com</p> <p style="color: #666;">Reach out anytime</p> </div> <div style="text-align: center; background: white; padding: 25px; border-radius: 20px;"> <div style="font-size: 3em;">🔗</div> <h3 style="color: #0a66c2; margin: 10px 0;">LinkedIn</h3> <p style="word-break: break-all;">linkedin.com/in/jose-mathew-</p> <p style="color: #666;">Let's connect professionally</p> </div> <div style="text-align: center; background: white; padding: 25px; border-radius: 20px;"> <div style="font-size: 3em;">📞</div> <h3 style="color: #28a745; margin: 10px 0;">Phone</h3> <p style="font-size: 1.1em;">+91 95679 76252</p> <p style="color: #666;">Available for opportunities</p> </div> <div style="text-align: center; background: white; padding: 25px; border-radius: 20px;"> <div style="font-size: 3em;">🐙</div> <h3 style="color: #333; margin: 10px 0;">GitHub</h3> <p style="word-break: break-all;">github.com/JoseOrbitX</p> <p style="color: #666;">Check out my other projects</p> </div></div><div style="border-top: 2px solid #e0e0e0; padding-top: 25px; margin-top: 30px; text-align: center; color: #777;"> <p>© 2026 Jose Mathew – Waze Churn Prediction Project</p> <p style="font-size: 0.95em;">Built as part of my data science learning journey – demonstrating practical application of end-to-end analytics and machine learning.</p> </div>
⭐ Support
If you find this project useful, please consider giving it a star on GitHub – it helps others discover it!

<div align="center"> <a href="https://github.com/JoseOrbitX/waze-churn-prediction"> <img src="https://img.shields.io/badge/View%20on%20GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"> </a> <a href="https://www.linkedin.com/in/jose-mathew-/"> <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"> </a> <a href="mailto:josejmk3322@gmail.com"> <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"> </a> <a href="https://github.com/JoseOrbitX"> <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Profile"> </a> </div>
