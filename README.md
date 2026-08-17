# 🚀 Conversion Pilot AI

### E-commerce Customer Behavior & Conversion Analysis

Conversion Pilot AI is an e-commerce analytics project developed during a hackathon to analyse customer behaviour, identify conversion drop-off points, and generate actionable business insights.

The project combines **data preprocessing, business intelligence, machine learning, and product recommendation** to support data-driven e-commerce optimization.

---

## 📌 Project Overview

E-commerce platforms generate large amounts of customer interaction and transaction data. However, businesses may struggle to transform this data into timely and actionable insights.

Conversion Pilot AI was developed to help businesses:

* Analyse customer behaviour and transaction patterns
* Identify conversion funnel drop-off points
* Predict potential cart abandonment
* Recommend relevant products
* Generate actionable business insights

The project was developed by the **Hackaholics** team as part of a hackathon.

---

## 👩‍💻 My Role

### Data Analysis & Business Intelligence

My main contribution focused on **data preprocessing and Power BI analytics**, particularly using **Google Colab and Power BI**.

### Google Colab

* Performed data cleaning and preprocessing using Python
* Removed duplicate records
* Handled missing values
* Converted timestamp data into datetime format
* Merged datasets into a unified dataset
* Selected relevant features for analysis
* Prepared the cleaned dataset for Power BI visualization

### Power BI

* Developed interactive dashboards for e-commerce performance analysis
* Created KPI metrics for customer and purchase analysis
* Developed DAX measures for conversion calculations
* Performed conversion funnel analysis
* Analysed revenue and sales performance
* Analysed customer behaviour and traffic sources
* Analysed geographic performance
* Identified key trends and business opportunities
* Translated data findings into actionable business recommendations

---

## 🛠️ Tools & Technologies

* **Python**
* **Google Colab**
* **Power BI**
* **DAX**
* **Machine Learning** *(team project component)*
* **FastAPI** *(team project component)*
* **Next.js** *(team project component)*

---

## 📊 Dataset

The project uses an e-commerce clickstream dataset obtained from Kaggle.

### Dataset Overview

| Metric                  |    Value |
| ----------------------- | -------: |
| Total Users             |   19,945 |
| Total Events            |  760,000 |
| Overall Conversion Rate |   27.98% |
| Total Revenue           | $111.65M |
| Total Sessions          |     120K |

### Key Features

* `user_id` — Unique user identifier
* `event_type` — Page view, add to cart, checkout, purchase
* `product_id` — Product interaction
* `event_timestamp` — Time of interaction

The project documentation identifies the dataset as synthetic and notes that it has limited real-world behavioural complexity.

---

# 🔄 Data Preparation

Data preprocessing was performed using Python in Google Colab.

The workflow included:

```text
Raw E-commerce Data
        ↓
Remove Duplicates
        ↓
Handle Missing Values
        ↓
Convert Timestamps
        ↓
Merge Datasets
        ↓
Select Relevant Features
        ↓
Cleaned Dataset
        ↓
Power BI Analysis
```

The cleaned dataset was subsequently imported into Power BI for visualization and business intelligence analysis.

---

# 📈 Power BI Dashboard

The Power BI dashboard was developed to provide an overview of e-commerce performance and customer behaviour.

### Dashboard Areas

* Revenue & Sales Performance
* Conversion Funnel
* Geographic Analysis
* Product & Category Performance
* Traffic Sources
* User Behaviour
* Customer Insights

### Dashboard Preview

<img width="1380" height="770" alt="image" src="https://github.com/user-attachments/assets/15026aca-2a1a-4e70-b5b3-f61303aa485c" />


---

## 💰 Revenue & Sales Analysis

Key findings from the dashboard include:

* Total revenue reached **$111.65M**
* Average order value was **$357.61**
* The United States generated the highest revenue at approximately **$21M**
* The United Kingdom and India were also among the significant markets

<img width="1370" height="771" alt="image" src="https://github.com/user-attachments/assets/a4b99a78-98af-4cb5-a924-5ee79a684284" />



---

## 🔎 Conversion Funnel Analysis

The customer journey was analysed through four main stages:

```text
Page View
    ↓
Add to Cart
    ↓
Checkout
    ↓
Purchase
```

The analysis identified a significant drop-off between the **Add to Cart** and **Checkout** stages.

This highlighted checkout as an important area for potential optimization, with possible factors including checkout complexity, cost concerns, and user experience issues.

---

## 👥 Traffic & User Behaviour

The dashboard analysed customer activity and traffic sources.

### Key Findings

* Total sessions: **120K**
* Peak activity occurred around **12 AM**
* Organic and direct channels were among the top traffic sources
* Average interactions per user: **38.15 clicks**

<img width="1377" height="772" alt="image" src="https://github.com/user-attachments/assets/c4c9bb42-c561-45c7-96b8-c1069645dd6a" />


---

## 🌍 Geographic & Product Insights

The analysis identified strong revenue concentration in selected markets, particularly the **United States**.

High-performing product categories included:

* Beauty
* Fashion
* Home & Kitchen

<img width="1370" height="772" alt="image" src="https://github.com/user-attachments/assets/04ef2863-a2af-447e-9fab-bc680062d679" />

---

# 🧮 DAX Measures

DAX was used to calculate key Power BI metrics, including customer conversion and session-based conversion.

### Customer Conversion Rate

```DAX
Total Customers =
DISTINCTCOUNT(user_Behaviour[customer_id])

Purchase Customers =
CALCULATE(
    DISTINCTCOUNT(user_Behaviour[customer_id]),
    user_Behaviour[event_type] = "purchase"
)

Customer Conversion Rate =
DIVIDE([Purchase Customers], [Total Customers])
```

### Purchase Conversion Rate — Session Based

```DAX
Total Sessions =
DISTINCTCOUNT(user_Behaviour[session_id])

Purchase Sessions =
CALCULATE(
    DISTINCTCOUNT(user_Behaviour[session_id]),
    user_Behaviour[event_type] = "purchase"
)

Purchase Conversion Rate =
DIVIDE([Purchase Sessions], [Total Sessions])
```

These measures were used to evaluate customer-level and session-level conversion performance.

---

# 🤖 AI Components

In addition to the analytics and Power BI components, the overall team project included AI-based components.

## Cart Abandonment Prediction

A **Random Forest Classification** model was developed to predict users who were likely to abandon their cart.

### Model Performance

| Metric   |     Result |
| -------- | ---------: |
| Accuracy |    **86%** |
| ROC-AUC  | **93.45%** |

The model was designed to support early identification of at-risk users and targeted intervention strategies.

---

## 🛍️ Product Recommendation System

The project also included an **item-based collaborative filtering** recommendation system.

The system analyses products that customers frequently add to their carts together and uses these relationships to generate product recommendations.

The recommendation engine returns the top recommended products based on co-cart behaviour.

---

# 💡 Key Insights

The analysis highlighted several important business insights:

### 1. High User Engagement

The dataset contained approximately **760,000 events**, indicating substantial customer interaction.

### 2. Conversion Opportunity

The overall conversion rate was **27.98%**, indicating opportunities to improve the conversion of customer interactions into purchases.

### 3. Checkout Drop-off

A significant drop-off occurred between **Add to Cart** and **Checkout**, highlighting checkout optimization as a key opportunity.

### 4. Geographic Concentration

Revenue was highly concentrated in selected countries, particularly the United States.

### 5. Product Category Performance

Beauty and Fashion were among the strongest-performing categories.

### 6. Customer Activity Timing

Customer activity peaked around **12 AM**, suggesting potential opportunities for targeted campaigns during high-activity periods.

---

# 💼 Business Recommendations

Based on the analysis, several recommendations were proposed:

* Optimize the checkout process to reduce customer friction
* Implement targeted cart abandonment campaigns
* Use personalized product recommendations
* Focus marketing efforts on high-performing markets
* Promote high-performing product categories
* Schedule campaigns around peak customer activity periods

---

# 📁 Project Structure

```text
conversion-pilot-ai/
│
├── README.md
│
├── notebooks/
│   └── data_preprocessing.ipynb
│
├── powerbi/
│   └── Conversion_Pilot_AI.pbix
│
├── images/
│   ├── system-architecture.png
│   ├── ecommerce-dashboard.png
│   ├── sales-analysis.png
│   ├── traffic-analysis.png
│   └── customer-insights.png
│
└── documentation/
    └── project-documentation.pdf
```

---

# ⚠️ Challenges & Limitations

The project had several limitations:

* The dataset was synthetic
* The dataset had limited real-world behavioural complexity
* Development was completed under hackathon time constraints

---

# 🚀 Future Improvements

Potential future improvements include:

* Real-time analytics and prediction pipelines
* Advanced recommendation algorithms
* Hybrid and deep learning-based recommenders
* Integration with live e-commerce platforms and APIs
* Customer churn prediction
* Customer Lifetime Value analysis
* Enhanced user-level personalization and behavioural segmentation

---

# 👥 Team

### Hackaholics

* **Nur Iliya Maisarah Binti Mustafa Kamal**
* **Muhammad Danial bin Sa'adon**
* **Asyraf Azmi**

**Project Date:** 11 April 2025

---

## 📄 Documentation

For the complete project documentation, see:

`documentation/project-documentation.pdf`

---

## ⚠️ Disclaimer

This project was developed as part of a hackathon and uses a synthetic e-commerce dataset. The analysis and models demonstrate potential applications of analytics and AI techniques for e-commerce optimization and may require further validation using real-world production data.
