# Project Background & Overview
The hospital administration requires a high-level strategic overview of Emergency Room (ER) operations to identify long-term trends in patient volume and care quality. This project transitions from short-term "firefighting" to long-term "planning." By consolidating 18 months of data, the dashboard allows stakeholders to see if operational issues are one-time events or recurring seasonal patterns.

**Key Business Questions:**
* Can the current ER infrastructure handle an average volume of ~500 patients per month over the long term?
* Does the Patient Satisfaction Score remain stable, or is it declining as patient volume increases?
* On a macro scale, what percentage of our total patient history meets the 30-minute wait-time target?

# Data Structure Overview
The consolidated dataset is a Time-Series collection of ER visits.

* **Source:** Kaggle Public Dataset
* **Scale:** Over 9,200 unique patient records.
* **Dimensions:** Time (Calendar/Date table), Geography (Referral sources), and Demographics (Age, Gender, Race).
* **Measures:** Calculated KPIs for Average Wait Time (Time-based) and Satisfaction (Ordinal/Integer based).

**Entity Relationship Diagram (ERD):**
![Data Model](images/datamodel.png)

# Executive Summary
Between April 2023 and October 2024, the ER processed **9,216 patients**. 

Long-term data shows a perfectly even **50/50** split between Admissions and Non-admissions. However, the satisfaction score has dipped below 5.00 **(4.99)**, indicating a systemic issue with patient experience. While 61.68% of patients are seen within the target time, the sheer volume on Sundays remains the primary operational bottleneck.

**High-Level Metrics (Consolidated)**
* **Total Patients**: 9,216
* **Avg. Wait Time**: 35.3 Minutes
* **Pat. Sat. Score**: 4.99 (Lower than the April monthly average)
* **No. of Patients Referred**: 3,816
* **Within Target Rate**: 61.68%

**Consolidated View**
![Dashboard Overview](images/consolidatedview.png)

**Monthly View**
![Dashboard Overview](images/monthlyview1.png)

# Insights Deep Dive
### Volume Analysis
* Sunday is consistently the busiest day of the week (**1,589 total patients**).
* The most dangerous "overload" periods occur between **00:00 and 04:00 on Mondays and Sundays**, where volume is consistently at its highest.

![Dashboard Overview](images/volumeanalysis.png)

### Demographic Equilibrium
  * Unlike the April-only view, the consolidated data shows that the **20-29** and **30-39** age groups are almost identical in volume (~1,200 each). This suggests the ER is a primary care source for young adults in this category.
![Dashboard Overview](images/demographic.png)

### Referral Source Impact
* While "None" (Walk-ins) is the largest group (**5.4K**), General Practice remains the most critical professional partner (**1.8K**).
![Dashboard Overview](images/referral.png)

### Monthly Story (April 2023 Deep Dive)
* When we filter down to April 2023, we see a "snapshot" of these problems. In April, the satisfaction was slightly higher (**5.30**) compared to the long-term average (**4.99**).
* This suggests that as the year progressed, patient satisfaction actually **decreased**, highlighting an urgent need for service intervention.


# Recommendations
* **Resource Scaling**: Implement a permanent "Weekend Night Shift" increase. The consolidated data proves that Sunday/Monday early mornings are a permanent trend, not a fluke.
* **Patient Experience Program**: Since the satisfaction score is trending downward (currently 4.99), the hospital should launch a "Fast-Track" program for low-acuity patients (the 50% not admitted) to get them out of the ER faster.
* **Partner Expansion**: Since General Practice sends so many patients, create a "Priority Triage" for GP-referred patients to reward the use of professional referral channels and reduce walk-in congestion.
