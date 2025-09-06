# 📊 Telecommerce Customer Churn Analysis  

## 📌 Project Overview  
Customer churn is a major challenge in the telecommunication industry. This project analyzes customer data to:  
- Identify the key drivers of churn  
- Build predictive models for churn classification  
- Provide actionable business insights to improve customer retention  

---

## 🗂️ Dataset  
The dataset contains customer-level attributes including demographics, service subscriptions, billing information, and churn status.  

**Key Columns:**  
- `customerID`  
- `gender`, `SeniorCitizen`, `Partner`, `Dependents`  
- `tenure`, `Contract`, `PaymentMethod`, `PaperlessBilling`  
- `PhoneService`, `InternetService`, `StreamingTV`, `StreamingMovies`  
- `MonthlyCharges`, `TotalCharges`  
- `Churn` (Target variable)  

---

## 🔍 Exploratory Data Analysis (EDA)  
- **Categorical Variables:** Analyzed with **Chi-Square test** to test association with churn.  
- **Numerical Variables:** Compared using **Mann-Whitney U test** (data is not normally distributed).  
- **Correlation:** **Spearman rank correlation** used to measure monotonic relationships.  

---

## ⚙️ Modeling Approach  

We trained and evaluated multiple machine learning models.  

| Model                 | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|------------------------|----------|-----------|--------|----------|---------|
| Logistic Regression    | **0.7991** | 0.6417    | **0.5508** | **0.5928** | **0.8394** |
| Random Forest          | 0.7814   | 0.6100    | 0.4893 | 0.5430   | 0.8175 |
| XGBoost                | 0.7885   | 0.6131    | 0.5508 | 0.5803   | 0.8206 |
| SVC                    | 0.7956   | **0.6558** | 0.4840 | 0.5569   | 0.7952 |
| MLP (Neural Net)       | 0.7921   | 0.6355    | 0.5080 | 0.5646   | 0.8392 |  

### ✅ Final Model Selection: Logistic Regression  
- Best **F1 Score (0.5928)** — balances precision & recall  
- Highest **ROC AUC (0.8394)** — strong class separation  
- Interpretable and efficient for business use  
- Hyperparameter tuning tested, but baseline model performed better  

---

## 📈 Model Evaluation Visualizations  
- Confusion Matrix  
- ROC Curve  
- Precision-Recall Curve  
- Feature Importance  

---

## 💡 Business Insights  

### Key Drivers of Churn  
- **Higher Churn Risk:**  
  - Fiber Optic Internet Service  
  - Month-to-Month Contracts  
  - Paperless Billing  

- **Lower Churn Risk:**  
  - No Internet Service  
  - Automatic Payment Methods (Credit Card, Bank Transfer)  

### Recommendations  
1. **Encourage Long-Term Contracts** → Offer discounts for 1-2 year commitments  
2. **Improve Fiber Optic Experience** → Investigate service quality & pricing issues  
3. **Engage Paperless Billing Customers** → Improve personalized communication  
4. **Promote Automatic Payments** → Incentivize auto-pay adoption  
5. **Targeted Retention Campaigns** → Identify & reach high-risk customers proactively  
6. **Continuous Monitoring** → Retrain churn model regularly for evolving trends  

---

## 🛠️ Tech Stack  
- **Language:** Python  
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost  
- **Statistical Tests:** Chi-Square, Mann-Whitney U, Spearman Correlation  
- **Modeling:** Logistic Regression, Random Forest, XGBoost, SVC, MLP  

---

## 🚀 How to Run  
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/telecom-churn-analysis.git
   cd telecom-churn-analysis
