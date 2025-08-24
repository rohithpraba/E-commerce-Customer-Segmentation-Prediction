# 🛒 E-Commerce Customer Segmentation & Prediction

This project applies data science and machine learning to analyze customer purchasing behavior using RFM (Recency, Frequency, Monetary) analysis.
It segments customers into meaningful groups and predicts future customer categories, enabling targeted marketing, churn reduction, and improved retention strategies.
The project also includes an interactive Gradio web app with PWA support (in progress) for real-time predictions.

---

## 📁 Project Structure

```
├── E_commerce_Customer_Segmentation_and_Prediction_Final.ipynb  # Main notebook with full pipeline
├── README.md                                                    # Project documentation
├── requirements.txt                                             # Python dependencies
└── data/                                                        # Dataset directory (place your CSV here)
```

---

## 📌 Objective

* Segment customers based on RFM analysis
* Perform EDA to understand purchasing behavior
* Build and evaluate models for customer classification
* Provide business insights for targeted marketing
* Deploy a web-based prediction tool (Gradio + PWA)

---

## 📦 Requirements

Make sure you have the following Python packages installed:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn shap eli5 gradio
```

---

## 🚀 How to Run

1. Clone this repository or download the notebook.
2. Place the dataset in the /data directory or update the path inside the notebook.
3. Open E_commerce_Customer_Segmentation_and_Prediction_Final.ipynb in Jupyter Notebook or VSCode.
4. Run the notebook sequentially to explore EDA, segmentation, modeling, and predictions.
5. To launch the Gradio app:

```bash
python app.py
```

The app will be available at: http://localhost:7860

---

## 📊 Methodology

* **Data Loading & Preprocessing:**
  * Removed duplicates, missing IDs, and invalid transactions
  * Engineered Recency, Frequency, Monetary (RFM) features
  * Applied scaling (StandardScaler) and one-hot encoding for Country
  * Used SMOTE to handle class imbalance

* **EDA (Exploratory Data Analysis):**

  * Analyzed top countries, spending patterns, and churn risks
  * Visualized distributions of RFM features
  * Cluster profiling to name customer groups
    
* **Segmentation (Unsupervised):**

  * Applied K-Means clustering
  * Chose optimal k using Elbow & Silhouette methods
  * Identified 4 clusters:
    1. Churning Customers
    2. One-time/New Customers
    3. Potential Loyalists
    4. High Loyal Customers

* **Prediction (Supervised):**

  * Models tested: Logistic Regression, Random Forest, KNN, SVM, XGBoost
  * XGBoost selected for best performance

* **Model Explainability:**

  * Eli5 Permutation Importance for global feature importance
  * SHAP values for local interpretability

---

## ✅ Results

* Best Model: XGBoost Classifier
* Performance Metrics: High accuracy and balanced F1-score across classes
* Top Features: Recency and Monetary value were the strongest predictors
* Key Insights:
  * High Loyal Customers → small segment but high revenue contribution
  * Potential Loyalists → best group to target for long-term ROI
  * Churning Customers → require reactivation offers
  * One-time Customers → onboarding campaigns critical

---

## 📈 Business Use Case

* Enables data-driven customer segmentation for personalized marketing
* Helps reduce churn by identifying at-risk customers early
* Provides a foundation for automated marketing campaigns through CRM integration
* Interactive Gradio + PWA app allows business teams to make predictions in real time

---

## 🧠 Future Work

* Finalize PWA support for mobile-first adoption (offline-ready, installable)
* Integrate with CRM systems to trigger campaigns automatically
* Experiment with deep learning models for behavioral prediction
* Continuously retrain models with live e-commerce data

---

## 📬 Contact

For questions or collaboration, please reach out:
📧 rohithpraba03@gmail.com











