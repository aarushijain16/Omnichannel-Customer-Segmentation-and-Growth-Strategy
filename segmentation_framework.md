# Customer Segmentation Framework

This project applies behavioral segmentation to identify distinct customer personas relevant to a premium lifestyle brand like Nicobar.

The goal is not predictive accuracy, but **strategic interpretability**.



# Features Used for Segmentation

Clustering was performed using normalized customer-level features:

- Purchase frequency

- Average order value

- Engagement index

- Loyalty score

- Online vs in-store purchase ratio

- Churn risk proxy

All features were scaled using StandardScaler to ensure equal contribution.



# Clustering Methodology

- **Algorithm:** K-Means

- **Number of Clusters:** 5

- **Selection Method:** Elbow Method + Silhouette Score

- **Dimensionality Check:** PCA used for validation and visualization

K-Means was chosen for its interpretability and suitability for persona-driven analysis.



# Final Customer Personas

## Final Customer Personas

| **Cluster Name** | **Description** |
|:----------------:|:---------------:|
| Engaged Regulars | High engagement, frequent buyers, strong brand affinity |
| Transitional Shoppers | Moderate spend, inconsistent engagement |
| Premium but At-Risk | High value customers with rising churn risk |
| Occasional Premiums | Low frequency but high-value purchases |
| Price-Sensitive Shoppers | Low spend, promotion-driven behavior |




# Why This Segmentation Matters

This framework allows brands to:

- Design differentiated CRM journeys

- Balance exclusivity with accessibility

- Move beyond discount-driven retention

- Align storytelling with behavioral reality

The clusters are designed to be **actionable**, not statistically abstract.
