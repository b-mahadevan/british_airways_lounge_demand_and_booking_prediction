# ✈️ British Airways – Lounge Demand & Booking Prediction

This project was completed as part of the **British Airways Data Science Virtual Experience Program** hosted on [Forage](https://www.theforage.com/). It simulates real-world airline industry tasks involving demand forecasting and customer behavior modeling to enhance strategic planning at British Airways.

---

## 📌 Project Overview

The project is divided into two key tasks:

### 1️⃣ Lounge Demand Estimation (Task 1)

**Goal:** Estimate lounge demand at Heathrow Terminal 3 by forecasting eligibility across Tier 1, 2, and 3 travelers — without needing detailed future flight schedules.

- Grouped over **2 million seats** by time of day and haul type (e.g., Morning Long, Afternoon Short).
- Calculated lounge eligibility using customer tier-level flags to derive average access percentages:
  - **Tier 1:** 0.18% – 0.39%
  - **Tier 2:** 2.67% – 4.55%
  - **Tier 3:** 10.26% – 17.28%
- Built a reusable **lookup table** to help Airport Planning teams anticipate lounge demand under evolving flight schedules.
- Justified assumptions logically based on customer segments, time-of-day patterns, and destination haul types.

---

### 2️⃣ Booking Prediction Model (Task 2)

**Goal:** Predict whether a customer will complete a booking based on their attributes, enabling targeted marketing and product decisions.

#### 🔍 Exploratory Data Analysis (EDA)
- Analyzed **50,000 booking records**:
  - Overall booking rate: **14.96%** (imbalanced)
  - Internet users booked more frequently (**15.48%**) than Mobile (**10.84%**)
  - Round Trips had **3×** higher conversion rates than One Way/Circle Trips

#### 🧠 Feature Engineering & Preprocessing
- Encoded categorical variables: `sales_channel`, `trip_type`, `route`, `booking_origin`
- Mapped `flight_day` to numerical values (Mon–Sun → 1–7)
- Addressed class imbalance using **SMOTETomek**:
  - Increased training data from **40,000 to 66,702 rows**

#### ⚙️ Modeling & Evaluation
- Models used: **Random Forest** and **XGBoost**
- Optimized with class weighting and **threshold tuning** for recall improvement
- Evaluation Metrics:

| Model          | F1-Score (Class 1) | Recall (Class 1) | Accuracy |
|----------------|--------------------|------------------|----------|
| Random Forest  | 0.39               | 0.54             | 0.74     |
| XGBoost        | **0.41**           | **0.63**         | 0.72     |

- **Feature Importance** was used to interpret which variables influenced booking predictions the most.

---

## 🛠️ Tools & Technologies
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Scikit-learn
- XGBoost
- imbalanced-learn (SMOTETomek)
- Jupyter Notebook
- PowerPoint (for stakeholder reporting)

---

## 📊 Key Skills Demonstrated
- Demand forecasting and customer segmentation
- Handling imbalanced data (SMOTETomek, class weighting)
- Supervised learning (classification models)
- Feature engineering and EDA
- Model evaluation and interpretation
- Business insight communication through visualization

---

## 🏆 Certificate

This project was completed as part of the [British Airways Virtual Experience Program on Forage](https://www.theforage.com/simulations/british-airways/data-science-yqoz) and awarded a certificate of completion.

---

## 🎓 About the Program

> _“A risk-free way to experience work on the job with us at British Airways. Practice your skills with example tasks and build your confidence to ace your applications.”_  
> — **British Airways (Forage)**

---

