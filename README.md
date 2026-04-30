# 🚖 Trip Completion & Cancellation Analysis

---

# 📌 Project Overview

This project analyzes trip booking data to understand **completion trends, cancellation patterns, and operational inefficiencies**.  
The goal is to support high-level strategic and operational decisions by identifying key drivers behind completed and canceled trips.

---

# 🧠 SCAN Framework

## 🎯 Stakeholder Goal
No immediate decision required.  
Focus is on understanding **high-level patterns in trip completion and cancellations**.

## 📊 Key KPI
- Completed Trips  
- Cancelled Trips  
  

## 🔍 Notable Segments
- Hour of the day  
- Day of the month  
- Cancellation reason  
- Pickup & drop-off location  
- Driver behavior  

---

You can  find the Tableau Dashboard [here](https://public.tableau.com/app/profile/mostafa.alali/viz/uber_trip_insight/drop_locaion_driver_cancel_reason1)

---

# 📊 Executive Summary

From **[poivet_tabel_1]**:

- Total bookings: **150K**
- Completed trips: **93K**
- Uncompleted trips: **9K**
- Cancelled trips:
  - Driver: **27K**
  - Customer: **10.5K** ⚠️

## 📌 Key Findings
- **July** has the highest number of bookings  
- Booking volume is relatively **stable across months**
- Distribution of booking states (completed / cancelled) is **consistent over time**
- **Driver cancellations represent a major issue (~48%)**

📌 Visual:
<img width="809" height="309" alt="poivet_tabel_1" src="https://github.com/user-attachments/assets/dbd181be-224b-46b4-b93a-455f32a9c723" />

---

# 🔍 Deep Dive Insights

## 1. Monthly Trends  
📌 From **[Tableau Tab → all_trip_month]**
- Trips are evenly distributed across months  
- Completed trips average **7K–8K per month**  
- Driver cancellations average **~2.5K per month**

📌 Insight:
No strong seasonality → time is not the main driver  

<img width="990" height="518" alt="all_trip_month" src="https://github.com/user-attachments/assets/b47a0915-b55a-4f09-8a17-b254b6f996fe" />


---

## 2. Hourly Demand Patterns  
📌 From **[Tableau Tab → all_trip_hour]**
- Demand increases starting **10:00 AM**
- Peak occurs at **18:00**
- Strong growth between **15:00–18:00**

📌 Insight:
Clear **rush-hour demand spike**

<img width="985" height="516" alt="all_trip_hour" src="https://github.com/user-attachments/assets/3fd265f9-e5fc-41c3-a35f-ad3391d75333" />


---

## 3. Cancellation Behavior  
📌 From **[Tableau Tab → all_cancel_trip_hour]**
- Driver cancellations account for **~48% of incomplete trips**

📌 Insight:
Driver behavior is the **primary bottleneck**

<img width="983" height="515" alt="all_cancel_trip_hour" src="https://github.com/user-attachments/assets/c4d0663e-552d-45a4-ac69-b9f95363d381" />

---

## 4. Consistency of Cancellation Patterns  
📌 From **[Tableau Tab → all_cancel_trip_month]**
- Driver cancellation rate (~48%) is consistent across:
  - Months  
  - Days  
  - Hours  

📌 Insight:
Indicates a **systematic issue**, not random behavior  

<img width="979" height="516" alt="all_cancel_trip_month" src="https://github.com/user-attachments/assets/f62f03b5-461d-4f74-8956-e56267760b0e" />

---

## 5. Daily Pattern Anomaly  
📌 From **[Tableau Tab → all_cancel_trip_day]**
- Drop in trips on the **30th day of the month**

📌 Insight:
Likely a **calendar effect**, not real demand drop  

<img width="986" height="511" alt="all_cancel_trip_day" src="https://github.com/user-attachments/assets/46c54e5f-e462-4a20-bc73-6a61bfc3df20" />

---

## 6. Cancellation Reason Analysis  
📌 From **[Tableau Tab → cancel_driver_month_d]**
- Cancellation reasons are **uniform across all dimensions**

📌 Insight:
Drivers may be selecting **default or inaccurate reasons**

<img width="988" height="512" alt="cancel_driver_month_days" src="https://github.com/user-attachments/assets/0cc0c057-fc1e-4b1b-bcc5-eac49bf0553b" />

---

## 7. Distance Impact (Critical Insight)  
📌 From **[Tableau Tab → distance_statue_seg]**
- **100% of driver cancellations occur for trips > 30km**

📌 Insight:
Distance is the **strongest driver of cancellations**


<img width="977" height="185" alt="distance_statue_seg" src="https://github.com/user-attachments/assets/395451d6-205a-4a82-b1e2-1f939c2c358b" />

---

## 8. Location vs Distance  
📌 From **[Tableau Tab → distance_statue_seg_dr]**
- No strong signal from pickup/drop-off locations  

📌 Insight:
Location is **not a key factor**


<img width="987" height="515" alt="distance_statue_seg_drop" src="https://github.com/user-attachments/assets/60cc12e3-6ea6-44da-9dcb-da8487fea488" />

---

# ⚠️ Final Takeaways

- No strong seasonality → problem is **not time-based**
- Driver cancellations (~48%) are the **main operational issue**
- Peak demand occurs at **15:00–18:00**
- Long-distance trips (>30km) are **systematically rejected**
- Cancellation behavior is **consistent → indicates structural issue**

---

# 📌 Recommendations by Team

## 🚖 Operations Team
- Investigate driver acceptance → cancellation flow  
- Rebalance supply during peak hours (15:00–18:00)  
- Redesign dispatch for long-distance trips (>30km)  

---

## 💰 Pricing / Strategy Team
- Re-evaluate pricing for long-distance trips  
- Introduce incentives for high-risk trips  
- Test surge or bonus models  

---

## 🧩 Product Team
- Improve matching algorithm (reduce low-intent acceptance)  
- Redesign cancellation reason selection  
- Shift product logic toward **distance-based trip classification**  

---

## 📊 Data / Analytics Team
- Validate data completeness (30th-day anomaly)  
- Build distance segmentation model:
  - 0–10 km  
  - 10–20 km  
  - 20–30 km  
  - 30+ km  
- Analyze full trip funnel (accept → complete / cancel)  

---

## 📣 Marketing Team
- Avoid monthly campaigns (no seasonality)  
- Focus on **peak-hour demand shaping (15:00–18:00)**  
- Align campaigns with operational capacity  

---

# 🚀 Tools Used
- Excel / Pivot Tables  
- Tableau  
- Data Analysis & KPI Modeling  

---

# 👨‍💻 Author
Mostafa Alali
