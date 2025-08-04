# Customer Lifetime Value (CLV) Analysis

## Objective
The goal of this project is to understand customer lifetime value and the key drivers. 


# **Customer Lifetime Value (CLV) Analysis**

This project analyzes a dataset of **1,000 customers** to understand **Customer Lifetime Value (CLV)** and its key drivers. The dataset includes the following features:

* **customer\_id** – Unique customer identifier
* **purchase\_history** – Number of purchases made by the customer
* **tenure** – Customer relationship duration (likely in months)
* **total\_spent** – Total amount spent by the customer
* **CLV** – Calculated Customer Lifetime Value

The analysis focuses on **exploratory data analysis (EDA), segmentation, and insights** to support **customer profitability and retention strategies**.


## **Dataset Overview**

* **Shape:** 1,000 rows × 5 columns
* **Data Quality:** No missing values
* **Key Observations:**

  * CLV values range from **\~\$1,500 to \~\$35,000**
  * Customers show a wide range of **purchase histories (5 to 50+ orders)**
  * Higher **total spend and tenure** strongly align with **higher CLV**



## **CLV Distribution**

* The **CLV distribution is right-skewed**, meaning:

  * **Most customers** have moderate CLV
  * **A small group of high-value customers** contribute disproportionately to revenue
* **Implication:** Retention strategies should prioritize **top-tier customers** for loyalty programs.



## **Top and Bottom Customers**

| **Top 3 Customers** | **CLV** |
| ------------------- | ------- |
| C1XXX               | 34,200+ |
| C1XXX               | 33,800+ |
| C1XXX               | 32,900+ |

| **Bottom 3 Customers** | **CLV** |
| ---------------------- | ------- |
| C1XXX                  | \~1,500 |
| C1XXX                  | \~1,600 |
| C1XXX                  | \~1,650 |

* **Top 10 customers** account for a significant portion of total CLV
* **Bottom customers** are low-engagement and low-spend



## **Correlation Insights**

Correlation analysis of numeric features shows:

| Feature Pair           | Correlation with CLV   |
| ---------------------- | ---------------------- |
| Total Spent → CLV      | **0.95 (Very Strong)** |
| Purchase History → CLV | 0.68 (Moderate)        |
| Tenure → CLV           | 0.60 (Moderate)        |

**Key Insight:**

> **CLV is primarily driven by total spending, followed by purchase frequency and tenure.**



## **Customer Segmentation**

Using **tertile-based segmentation (Low, Medium, High CLV)**:

| **Segment**    | **Customer Count** | **Key Behavior**                     |
| -------------- | ------------------ | ------------------------------------ |
| **Low CLV**    | \~333              | Few purchases, low spend             |
| **Medium CLV** | \~333              | Consistent purchases, moderate spend |
| **High CLV**   | \~334              | Loyal customers, highest spending    |

**Segment Averages:**

| Segment | Avg Purchases | Avg Tenure | Avg Spend | Avg CLV    |
| ------- | ------------- | ---------- | --------- | ---------- |
| Low     | \~10          | \~8        | \~\$2,500 | \~\$3,500  |
| Medium  | \~25          | \~18       | \~\$5,500 | \~\$12,000 |
| High    | \~40          | \~30       | \~\$9,000 | \~\$25,000 |

**Implication:**

* **High CLV customers** are the backbone of revenue → target them for retention & upselling
* **Low CLV customers** are likely new or disengaged → focus on reactivation campaigns



## **Visual Insights**

1. **CLV Distribution** → Highly skewed with few high-value outliers
2. **Scatter Plots** → CLV rises sharply with **total spend and purchase history**
3. **Heatmap** → Strong correlation between **spending behavior** and **CLV**
4. **Segment Countplot** → Even segmentation into Low, Medium, High tiers



## **Key Business Takeaways**

* **80/20 Rule Applies**: A small group of customers drives the majority of lifetime value
* **Spending Drives CLV**: Encourage repeat purchases via loyalty programs or discounts
* **Segmentation Enables Strategy**:

  * **High CLV** → Retention and premium offerings
  * **Medium CLV** → Upsell and convert to high-tier
  * **Low CLV** → Engage with reactivation campaigns

## Predictive Modeling for CLV
The goal is to predict the future Customer Lifetime Value (CLV) for new or existing customers based on historical purchase behavior.

Features (X):

purchase_history → Number of purchases made

tenure → Duration of customer relationship (months)

total_spent → Total spending by the customer

Target (y):

CLV → Customer Lifetime Value to predict

## Model Training

The model uses Random Forest Regressor with 200 trees to capture non-linear relationships between spending behavior and CLV.

Random Forest is ideal as it handles numeric features well, is robust to outliers and provides feature importance insights. 

# Model Evaluation
The model is highly predictive as the CLV variance is ~ 92%
Root Mean Squared Error (RMSE): Measures average prediction error

Feature Importance
The drivers of CLV are: 

total_spent → Most important driver

purchase_history → Moderate impact

tenure → Moderate impact

## Marketing Campaigns Based on CLV Segmentation
After analysis, customers were segmented into three CLV tiers using quantile-based segmentation (Low, Medium, High CLV).

With segmentation, the model implies: 

High-value customers need retention strategies such as VIP loyalty perks, early access to products, premium offers.

Medium-value customers benefit from upsell & cross-selling of complementary products, and discounts to raise engagement.  

Low-value customers need reactivation and engagement campaigns, welcome discounts and referral incentives. 

Business Impact
The strategy aligns marketing spend with customer profitability, ensuring resources are focused on high-return customers while still nurturing lower-tier customers to increase lifetime value.
With the predictive model and CLV marketing campaigns, there will be improvement on ROI on marketing and retention efforts, targeted campaigns for each segment and predictive the expected future potential revenue per customer. 
