# Maximizing Taxi Revenue through Payment Type Analysis  

## Overview  
This project explores whether **payment methods (Card vs Cash)** have a significant impact on **fare amounts** in New York City Yellow Taxi rides.  

Using **NYC Yellow Taxi Trip Data**, we perform:  
- Data cleaning (handling missing values, duplicates, outliers).  
- Exploratory Data Analysis (EDA) to understand passenger behavior and payment distribution.  
- Statistical hypothesis testing (T-test) to test whether average fares differ between **Card** and **Cash** payments.  

The results aim to provide **data-driven recommendations for taxi drivers** to maximize revenue.  

---

## Problem Statement  
In the fast-paced taxi booking sector, maximizing revenue is essential for long-term success and driver satisfaction.  

We investigate:  
1) **Does the method of payment (Card vs Cash) influence the fare amount?**  
2) **Can nudging customers toward specific payment types increase driver revenue without affecting customer experience?**

---

## Methodology  
1. **Data Preprocessing**  
   - Converted datetime columns into trip durations.  
   - Selected relevant fields: passenger count, payment type, fare amount, trip distance, duration.  
   - Removed missing values, duplicates, and invalid entries (negative fares/distances).  
   - Handled outliers using IQR method.  

2. **Exploratory Data Analysis (EDA)**  
   - Distribution of **fare amounts & trip distances** by payment type.  
   - Passenger count vs payment method (stacked bar plots).  
   - Proportion of **Card vs Cash** users (pie chart).  

3. **Hypothesis Testing**  
   - **Null Hypothesis (H0):** No difference in mean fares between Card and Cash payments.  
   - **Alternative Hypothesis (H1):** There is a difference in mean fares between Card and Cash payments.  
   - Used **T-test (Welch’s t-test)** since fare amounts were not normally distributed.  

---

## Key Insights  
- **Outliers & invalid entries** (negative values, extreme fares) were removed to ensure robust results.  
- **Card payments** dominate over cash transactions.  
- Passengers paying with **Card** tend to have **higher average fares** compared to cash payers.  
- Hypothesis test results:  
  - **p-value < 0.05 → Reject H0.**  
  - Conclusion: **Significant difference in average fare amounts between Card and Cash payments.**  

 **Recommendation:** Encourage passengers to pay via **Card** to maximize revenue for drivers.  

---

## Dataset  
- **NYC Yellow Taxi Trip Records** (January 2020)  
- Source: [Kaggle - NYC Yellow Taxi Trip Data](https://www.kaggle.com/datasets/elemento/nyc-yellow-taxi-trip-data)  

Contains fields like pickup/dropoff datetime, passenger count, trip distance, fare amount, tip amount, and payment type.  

---

## ▶️ How to Run  
1. Clone this repository:  
   ```bash
   git clone https://github.com/AnjaniMalhotra/Maximising-Taxi-Revenue-Project.git
   cd Maximising-Taxi-Revenue-Project
