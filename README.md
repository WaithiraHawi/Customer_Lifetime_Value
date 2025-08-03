# Customer Lifetime Value (CLV) Analysis

## Objective
The goal of this project is to **identify high-value customers** by calculating their **Customer Lifetime Value (CLV)** and segmenting them into actionable categories for marketing and retention strategies.

---

## Dataset Overview
- **Number of Customers:** 100  
- **Key Features:**
  - `Customer ID` – Unique customer identifier  
  - `Purchase_Frequency` – Average monthly purchases  
  - `Average_Purchase_Amount` – Average amount spent per purchase  
  - `Membership_Tenure` – Customer tenure in years  
  - `Website_Visits_per_Month` – Proxy for engagement  

---

## CLV Calculation
CLV is calculated using the formula:

\[
CLV = Average\ Purchase\ Amount \times Purchase\ Frequency \times Membership\ Tenure
\]

This gives an **estimate of the total revenue a customer generates** during their relationship with the company.

---

## Customer Segmentation
Customers are segmented into **Low**, **Medium**, and **High CLV tiers** using quantiles (bottom 33%, middle 33%, top 33%).

| CLV Segment | Description | Strategy |
|-------------|------------|----------|
| **High**    | Top 33% revenue-generating customers | Retention campaigns, loyalty programs |
| **Medium**  | Mid-tier customers | Upsell / cross-sell to increase value |
| **Low**     | Lower revenue contribution | Nurture or automated retention efforts |

---

## Key Insights
- Most customers fall into the **Low and Medium CLV categories**, confirming a **Pareto distribution** where a small group of customers generates the majority of revenue.  
- **High CLV customers** are prime targets for loyalty and retention initiatives.  
- The **CLV distribution is right-skewed**, indicating a concentration of value in a few customers.

---

## Visualizations

# CLV Distribution
Shows how customer values are distributed, highlighting the skew toward lower CLV customers.  

# CLV Segmentation
Displays the number of customers in Low, Medium, and High CLV tiers.  


---

## Deliverables
- **`CLV_Segmented_Customers.xlsx`** → Customer IDs with calculated CLV and segment  
- **`clv_distribution.png`** → CLV distribution plot  
- **`clv_segmentation.png`** → Customer segmentation visualization  

---

## Next Steps
1. Flag **Top 20% VIP customers** for personalized campaigns.  
2. Integrate **predictive CLV modeling** using BG/NBD + Gamma-Gamma models.  
3. Schedule the **pipeline to run automatically** for new incoming data.  

---
This project helps businesses identify, retain, and maximize value from their most profitable customers.
