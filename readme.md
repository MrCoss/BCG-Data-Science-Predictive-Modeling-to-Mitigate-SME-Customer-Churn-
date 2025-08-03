# Project Report: Predictive Modeling to Mitigate SME Customer Churn  
**Client:** PowerCo  
**Date:** August 3, 2025  
**Status:** Final Analysis & Recommendations  

---

## 1. Executive Summary: Proactively Identifying Churn Risk to Protect Revenue  

### Background  
PowerCo is currently facing a significant challenge with customer churn within its Small and Medium Enterprise (SME) division. To address this, a data-driven project was initiated to move from a reactive to a proactive retention strategy by developing a solution to identify at-risk customers before they leave.  

### Key Findings  
Our analysis has culminated in a predictive machine learning model that successfully identifies 35% of all customers who are likely to churn. More importantly, we have isolated the key business drivers that influence this behavior: customer tenure, profitability (net margin), and price volatility.  

### Business Impact  
The model provides a targeted, actionable list of high-risk customers, enabling PowerCo to launch focused and efficient retention campaigns. This data-driven approach improves the return on investment (ROI) of retention spending and will have a direct, positive impact on the company's bottom line by protecting a critical revenue stream.  

---

## 2. Project Implementation Steps  

The project followed a structured, four-phase data science methodology to ensure robust and reliable outcomes.  

### Phase A: Exploratory Data Analysis (EDA)  
We began by conducting a deep dive into the historical customer and pricing data. This phase focused on understanding the data's structure, identifying initial trends, and forming early hypotheses. A key discovery was the 9.7% churn rate, confirming a significant class imbalance that guided our subsequent modeling strategy.  

### Phase B: Feature Engineering  
To enhance the predictive power of our data, we engineered a new set of features by expanding and combining existing columns. This included creating features to represent:  

- **Time-Based Metrics:** Such as customer tenure_days.  
- **Price Sensitivity:** Including price_volatility and year-end price changes.  
- **Consumption Patterns:** Capturing recent deviations from average consumption.  

### Phase C: Predictive Modeling  
We trained several machine learning models to predict customer churn. We started with a Random Forest baseline and progressed to a more powerful LightGBM (Gradient Boosting Machine) model, which is known for its high performance on tabular data.  

### Phase D: Model Evaluation & Tuning  
To address the class imbalance, we implemented the SMOTE (Synthetic Minority Over-sampling TEchnique), which created a more balanced training dataset. Models were evaluated using metrics appropriate for this business problem, including Recall, F1-Score, and AUC. The final LightGBM model was selected as the best performer based on its superior ability to identify true churners.  

---

## 3. Key Drivers of Customer Churn  

The predictive model has identified three primary factors that are most influential in determining whether a customer will churn. Understanding these drivers is crucial for developing effective retention strategies.  

### Customer Tenure (The "Danger Zone")  
**Finding:** The risk of churn is highest for customers who have been with PowerCo for 4 to 5 years. This suggests that the mid-point of the customer lifecycle is a critical period where loyalty may waver, and proactive engagement is most needed.  

### Customer Profitability (Net Margin)  
**Finding:** There is a strong, inverse relationship between a customer's profitability and their likelihood to churn. Customers who generate a lower net margin for PowerCo are significantly more likely to switch providers.  

### Price Volatility  
**Finding:** Price stability is a key factor in customer satisfaction. Our analysis shows that customers who have experienced greater instability and volatility in their energy prices are at a higher risk of churning, even if their average price is competitive.  

---

## 4. Recommendations and Strategic Next Steps  

Based on these findings, we recommend a phased approach to leverage the model's insights and address the root causes of churn.  

### Phase 1: Deploy a Targeted Retention Campaign (Immediate)  
Utilize the model's predictions to launch a pilot retention campaign focused on the highest-risk customer segments. We recommend developing tailored offers that directly address the key pain points identified:  

- Offer loyalty discounts or special plans for customers in the 4–5 year tenure "danger zone."  
- Provide stable, fixed-price contract options for customers who have been impacted by price volatility.  

### Phase 2: Enhance and Integrate the Model (Next 3 Months)  
Continuously improve the model's accuracy by incorporating new data sources as they become available. The primary goal of this phase is to begin the process of integrating the model into PowerCo's CRM system. This will provide account managers with real-time churn risk scores, empowering them with the data needed for proactive, informed client conversations.  
<img width="1005" height="710" alt="model_comparison_metrics" src="https://github.com/user-attachments/assets/1816c8fc-5b3b-4c4d-9442-05a83d33450e" />
<img width="1686" height="1569" alt="before_correlation_heatmap" src="https://github.com/user-attachments/assets/3919cff5-7296-4139-8eb2-28e63925f7da" />
<img width="1635" height="1519" alt="after_correlation_heatmap" src="https://github.com/user-attachments/assets/432f48b8-17a2-4181-863a-633031015e9a" />

### Phase 3: Conduct a Strategic Review (Long-Term)  
Use the insights from the model to conduct a strategic review of the business operations that correlate with high churn. This includes analyzing the performance of different sales channels and reassessing pricing structures that may be creating the volatility that drives customers away. This long-term approach will help address the root causes of churn, not just its symptoms.  
