# OptiChurn-Behavioral-Segmentation-Churn-Prediction-for-Telecom
An enterprise-grade analytics solution designed to combat telecom revenue loss through customer segmentation and churn prediction. Using K-Means clustering, the customer base is divided into behavioral risk cohorts. Advanced ML models then calculate individual churn probabilities, providing actionable data-driven insights to optimize retention ROI.

## 📌 Project Overview

Customer churn is one of the biggest challenges in the telecom industry. Acquiring new customers costs significantly more than retaining existing ones.

This project integrates:

- **Unsupervised Learning** → Customer Segmentation using K-Means Clustering
- **Supervised Learning** → Churn Prediction using ML models
- **Business Analytics** → Segment-wise churn analysis and retention insights

The system first groups customers into meaningful behavioral segments and then predicts the probability of churn using classification models.

---

# 🎯 Objectives

- Identify hidden customer segments using clustering
- Detect churn-prone customer groups
- Predict customer churn probability
- Improve retention strategy using business insights
- Compare multiple ML models for best performance

---

# 🧠 Problem Statement

Telecom companies face major revenue loss due to customer churn.

This project aims to:

✅ Segment customers based on behavioral patterns  
✅ Identify high-risk customer groups  
✅ Predict churn probability accurately  
✅ Generate actionable business insights

---

# ⚙️ Tech Stack

| Category | Tools / Libraries |
|---|---|
| Language | Python |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn, XGBoost |
| Imbalanced Data Handling | SMOTE |
| Dimensionality Reduction | PCA |
| Clustering | K-Means |
| Model Evaluation | ROC-AUC, F1-Score, Precision-Recall |
| Environment | Jupyter Notebook |

---

# 📂 Dataset Information

- Dataset: `Telco_Churn_Segmented.csv`
- Total Customers: **7043**
- Features: **24 Columns**

### Data Split

| Split | Percentage |
|---|---|
| Training | 70% |
| Validation | 10% |
| Testing | 20% |

---

# 🔄 Project Workflow

```text
Data Collection
       ↓
Data Preprocessing
       ↓
Exploratory Data Analysis
       ↓
Feature Engineering
       ↓
Customer Segmentation (K-Means)
       ↓
PCA Visualization
       ↓
Churn Prediction Modeling
       ↓
Model Evaluation
       ↓
Business Insights
```

---

# 🧹 Data Preprocessing

The following preprocessing steps were applied:

- Handling missing values
- Encoding categorical variables
- Feature scaling
- Data balancing using SMOTE
- Outlier handling
- Feature engineering

---

# 📊 Exploratory Data Analysis (EDA)

Key findings from EDA:

- Customers with lower tenure are more likely to churn
- High monthly charges increase churn probability
- Long-term customers show better retention
- Certain customer segments have significantly higher churn rates

### Important Correlations with Churn

| Feature | Correlation |
|---|---|
| MonthlyCharges | +0.19 |
| TotalCharges | -0.19 |
| Tenure | -0.35 |

---

# 👥 Customer Segmentation

## 🔹 Clustering Technique Used

- K-Means Clustering
- Optimal clusters determined using:
  - Elbow Method
  - Silhouette Score

### Final Number of Clusters: `K = 4`

---

## 📌 Customer Segments

| Segment | Description |
|---|---|
| Segment 0 | New customers on expensive plans |
| Segment 1 | Low-pay stable customers |
| Segment 2 | Medium-term churn-prone customers |
| Segment 3 | Loyal high-value customers |

---

# 📉 PCA Visualization

PCA was used to reduce dimensionality and visualize customer clusters in 2D space.

Benefits:
- Better cluster interpretation
- Visual separation of customer groups
- Reduced feature complexity

---

# 🤖 Churn Prediction Models

The following models were trained and evaluated:

- Logistic Regression
- Random Forest
- Gradient Boosting
- XGBoost

---

# 📈 Model Performance

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---|---|---|---|---|
| Logistic Regression | 0.755 | 0.529 | 0.714 | 0.608 | 0.823 |
| Random Forest | 0.786 | 0.595 | 0.612 | 0.603 | 0.826 |
| Gradient Boosting | 0.769 | 0.554 | 0.663 | 0.603 | **0.830** |
| XGBoost | 0.772 | 0.569 | 0.583 | 0.576 | 0.815 |

🏆 **Best Performing Model:** Gradient Boosting

---

# 🧪 Feature Engineering Experiments

Additional engineered features:

- `tenure_group`
- `customer_lifetime_value`
- `avg_monthly_spend`
- `total_services`
- `charges_category`

Total Features After Engineering: **32**

---

# 📊 Segment-wise Churn Analysis

Insights from segment analysis:

- Segment 2 had the highest churn rate
- Loyal customers showed lowest churn probability
- New customers with expensive plans required targeted retention campaigns

---

# 💼 Business Impact

### Immediate Actions (0–30 Days)

- Launch retention campaigns for high-risk customers
- Offer contract upgrade incentives
- Improve customer support quality

### Short-Term Actions (1–3 Months)

- Segment-specific marketing strategies
- Personalized retention offers
- Predictive churn monitoring dashboards

### Long-Term Actions (3–12 Months)

- Customer experience optimization
- Pricing strategy improvements
- Data-driven decision making

---

# 📸 Sample Outputs

## Customer Segmentation
- PCA Cluster Visualization
- Segment Heatmaps
- Churn Distribution Analysis

## Model Evaluation
- ROC Curves
- Precision-Recall Curves
- Confusion Matrix Comparison

---

# 📁 Project Structure

```bash
├── data/
│   └── Telco_Churn_Segmented.csv
│
├── notebooks/
│   └── customer_churn_segmentation.ipynb
│
├── images/
│   ├── pca_clusters.png
│   ├── roc_curve.png
│   ├── confusion_matrix.png
│   └── churn_analysis.png
│
├── models/
│   └── trained_models.pkl
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

# ▶️ Installation & Setup

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/customer-churn-segmentation.git
cd customer-churn-segmentation
```

---

## 2️⃣ Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux / Mac

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

# ▶️ Run the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
customer_churn_segmentation.ipynb
```

---

# 📦 Requirements

Example dependencies:

```txt
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
imbalanced-learn
jupyter
```

---

# 🔮 Future Improvements

- Deploy using Flask / FastAPI
- Real-time churn prediction pipeline
- Stream processing using Kafka
- Deep Learning-based churn prediction
- SHAP explainability integration
- Dashboard using Power BI / Streamlit

---

# 📚 Learning Outcomes

Through this project, I learned:

- Customer behavior analytics
- Unsupervised + supervised ML integration
- Handling imbalanced datasets
- Feature engineering techniques
- Model evaluation for business problems
- Translating ML outputs into business insights

---

# 👨‍💻 Author

## Pratik Sarkar

M.Sc. Data Science & Artificial Intelligence  
Ramakrishna Mission Vivekananda Educational and Research Institute (RKMVERI)

---

# ⭐ If You Like This Project

Give this repository a ⭐ on GitHub and share your feedback!
