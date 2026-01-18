# Data Model Overview

This project uses a hybrid data model combining open-source retail datasets with synthetically engineered customer-level data to simulate an omnichannel analytics environment for a lifestyle brand like Nicobar.

The objective of the data model is to enable:

- Customer segmentation and persona discovery

- Revenue and CLV analysis

- Channel behavior comparison (online vs in-store)

- Product affinity and engagement analysis



# Source Datasets

The foundational datasets were sourced from publicly available grocery retail repositories:

- **Product Family Mapping** – Used as the base for synthetic customer generation

- **Product Information** – Category hierarchy and product attributes

- **Demand and Shopping Behaviour** – Spend, frequency, and category demand

- **In-store Customer and Online Order Arrivals** – Channel-level traffic patterns



# Engineered Analytical Tables

From the raw and proxy datasets, the following core analytical tables were engineered using Python:

## 1. customers_master

**Grain:** One row per customer  

Contains:

- Customer ID

- Cluster assignment

- Loyalty score

- Engagement index

- Online purchase ratio

- Churn risk proxy

This table acts as the central spine of the data model.



## 2. revenue_by_cluster

**Grain:** Cluster level  

Used to assess:

- Revenue contribution by behavioral segment

- Identification of high-value vs high-risk clusters



## 3. clv_proxy

**Grain:** Customer / Cluster level  

Derived using frequency, spend, and engagement metrics to estimate long-term value.



## 4. product_affinity

**Grain:** Cluster × Product Category  

Captures dominant cross-category buying patterns to support:

- Collection design

- Cross-sell strategy

- Intent-based merchandising



## 5. Supporting Tables

- marketing_effectiveness

- operational_efficiency

- arrivals_summary

- demand_summary

- behaviour_overview



# Join Logic (Conceptual)

- customers_master.customer_id
  → joins to all customer-level tables

- Cluster ID acts as a shared key across:

  - revenue

  - CLV

  - product affinity

  - channel preference



# Design Philosophy

- Star-schema inspired analytical model

- Customer-centric grain

- Optimized for segmentation, not transactions

- Suitable for CRM, strategy, and experience design use cases

This model is intentionally designed to be **brand-strategy friendly**, rather than ERP- or accounting-oriented.
