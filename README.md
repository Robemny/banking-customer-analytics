# 🏦 Banking Customer Analytics

## Executive Summary

This project analyzes banking customer and marketing campaign data to identify patterns in customer behavior and factors associated with successful term deposit subscriptions.

Using Python and Pandas, I explored customer demographics, financial characteristics, previous campaign interactions, and subscription outcomes. I then developed a Logistic Regression classification model to evaluate whether customer and campaign characteristics could help identify customers more likely to subscribe.

The project demonstrates an end-to-end analytics workflow, moving from raw data exploration and cleaning to visualization, predictive modeling, model evaluation, and business recommendations.

---

## 🎯 Business Problem

Financial institutions use customer data to better understand engagement and improve the effectiveness of marketing campaigns. Contacting customers without understanding which characteristics or behaviors are associated with successful outcomes can lead to inefficient outreach.

This analysis explores:

- Which customer characteristics are associated with successful subscriptions?
- How do account balance, age, occupation, and loan status relate to customer outcomes?
- How does previous campaign activity relate to subscription behavior?
- Where could customer segmentation improve campaign targeting?
- Can predictive modeling help identify customers with a higher likelihood of subscribing?

---

## 🛠️ Tools & Skills

**Python | Pandas | NumPy | Scikit-learn | Matplotlib | Data Cleaning | Exploratory Data Analysis (EDA) | Data Visualization | Customer Analytics | Logistic Regression | Predictive Modeling | Model Evaluation**

---

## 📊 Dataset

The analysis contains **4,521 customer records** and examines demographic, financial, and marketing campaign variables.

Key variables include:

- Age
- Job
- Marital status
- Education
- Account balance
- Housing loan status
- Personal loan status
- Contact method
- Campaign activity
- Previous campaign outcome
- Term deposit subscription outcome

This project uses a banking marketing dataset for educational and portfolio analysis.

**The dataset does not contain M&T Bank customer information or proprietary employer data.**

---

## 🔎 Exploratory Data Analysis

The exploratory analysis examined customer characteristics and marketing campaign outcomes to identify patterns associated with term deposit subscriptions.

The analysis included:

- Dataset structure and data quality review
- Missing value assessment
- Duplicate record checks
- Customer demographic analysis
- Account balance analysis
- Occupation-based segmentation
- Loan status analysis
- Previous campaign performance
- Subscription rate comparisons
- Data visualization

---

## 📈 Key Findings

### Overall Subscription Rate

Approximately **11.5%** of customers in the dataset subscribed to the term deposit.

### Previous Campaign Performance

Previous campaign outcomes showed a strong relationship with subscription behavior.

Customers whose previous campaign outcome was successful had a **64.3% subscription rate**, compared with:

- **12.9%** following a previous failure
- **9.1%** when the previous outcome was unknown

This suggests that previous campaign responsiveness may be an important indicator when prioritizing future outreach.

### Occupation

Subscription rates varied substantially across occupational groups.

- Retired customers: **23.5%**
- Students: **22.6%**
- Blue-collar customers: **7.3%**

These differences suggest that customer occupation may provide useful information for segmentation.

### Housing Loans

Customers without housing loans subscribed at approximately **15.3%**, compared with **8.6%** among customers with housing loans.

### Personal Loans

Customers without personal loans subscribed at approximately **12.5%**, compared with **6.2%** among customers with personal loans.

---

## 🤖 Predictive Modeling

To extend the exploratory analysis, I developed a **Logistic Regression classification model** to predict whether a customer would subscribe to a term deposit.

The target variable contained two outcomes:

- **0 — No Subscription**
- **1 — Subscription**

Categorical variables were transformed using **One-Hot Encoding**, while numerical variables were standardized using **StandardScaler**.

The dataset was divided into:

- **80% training data**
- **20% testing data**

Because subscription outcomes were imbalanced, the Logistic Regression model used balanced class weights to improve its ability to identify subscribers.

---

## 📊 Model Performance

The Logistic Regression model achieved:

| Metric | Result |
|---|---:|
| Accuracy | **82.3%** |
| ROC-AUC | **0.891** |
| Subscriber Recall | **78%** |
| Subscriber Precision | **37%** |
| Subscriber F1-Score | **0.50** |

The **ROC-AUC score of 0.891** indicates that the model demonstrated strong ability to distinguish between customers who subscribed and those who did not.

Of the **104 customers in the test set who actually subscribed**, the model correctly identified **81**, representing approximately **78% of actual subscribers**.

The model also classified 137 non-subscribers as potential subscribers. This demonstrates an important business tradeoff: the model captures a large portion of potential subscribers but may also result in outreach to customers who ultimately do not subscribe.

---

## 💼 Business Interpretation

The predictive results complement the exploratory analysis by demonstrating that customer and campaign characteristics contain useful information for identifying potential subscribers.

Rather than contacting customers without prioritization, a financial institution could use predictive analytics to rank customers by likelihood of subscription and focus campaign resources on higher-potential segments.

The model could serve as an initial customer-targeting tool while additional model tuning and testing are performed.

---

## 💡 Business Recommendations

Based on the exploratory findings and predictive modeling results, a financial institution could consider:

1. **Prioritizing previously responsive customers** when designing follow-up campaigns while continuing to evaluate whether historical responsiveness persists in new campaign data.

2. **Testing targeted strategies across occupational segments**, particularly groups that demonstrated higher subscription rates such as retired customers and students.

3. **Considering existing loan relationships during customer segmentation**, since customers without housing or personal loans demonstrated higher subscription rates in this dataset.

4. **Using predictive modeling to prioritize outreach** by ranking customers according to estimated subscription likelihood rather than contacting customers without segmentation.

5. **Improving the model through additional testing**, including feature engineering, threshold optimization, model tuning, and comparison with other classification algorithms.

---

## ⚠️ Model Considerations

While the model achieved strong recall and ROC-AUC performance, subscriber precision was lower at **37%**.

This means the model successfully identified many actual subscribers but also generated false positives.

For a real marketing campaign, the appropriate decision threshold would depend on business considerations such as:

- Cost of customer outreach
- Value of a successful subscription
- Campaign capacity
- Customer experience
- Acceptable false-positive rate

Further analysis could optimize the classification threshold based on these business requirements.

---

## 📁 Repository Contents

### `banking-customer-analytics.ipynb`

Complete Jupyter Notebook containing:

- Data loading
- Data inspection
- Data cleaning
- Exploratory data analysis
- Customer segmentation
- Data visualizations
- Key findings
- Logistic Regression modeling
- Confusion matrix
- ROC curve
- Model evaluation
- Business interpretation

### `README.md`

Executive overview of the project, methodology, findings, model performance, and business recommendations.

---

## 🚀 Future Improvements

Future versions of this project could include:

- Random Forest modeling
- Gradient Boosting models
- Feature importance analysis
- Cross-validation
- Hyperparameter tuning
- Classification threshold optimization
- Additional customer segmentation
- Interactive Power BI or Tableau dashboard
- SQL-based customer analysis
- Model deployment or scoring workflow

---

## 📌 Project Purpose

This project was developed as part of my data analytics portfolio to demonstrate practical skills in:

**Data Cleaning → Exploratory Analysis → Visualization → Predictive Modeling → Model Evaluation → Business Insights**

The goal is not only to build a predictive model, but to demonstrate how data analysis can translate customer information into actionable business recommendations.
