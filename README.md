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
![Data Model](images/Data_Model.png)

# Executive Summary
**Top 10 LGUs house nearly 60% of the population, while provincial growth slows to 1.04%.**

The dashboard reveals a highly concentrated population distribution. Out of 40 LGUs analyzed, the top 10 (led by **Sariaya** and **Candelaria**) account for **60%** of the province's total inhabitants. Additionally, the province is experiencing a "Demographic Dividend," with a strong **62.05%** of the population falling within the working age (15-64 years old), suggesting high economic potential if employment opportunities are met.

**High-Level Metrics:**
* **Total Population (2020)**: 1.95 Million
* **Population Density**: 223 people per KM²
* **Total Barangays**: 1,209

![Dashboard Overview](images/Dashboard.png)

# Insights Deep Dive
### The "60/40" Urban Concentration
* The population is not evenly spread. Developing hubs like Sariaya (161k) and Candelaria (137k) carry the bulk of the density, while rural municipalities remain sparsely populated.
* Infrastructure projects and public services should be prioritized in these top 10 high-density LGUs to prevent congestion, while development incentives are needed in rural areas to balance migration.

![Dashboard Overview](images/UrbanConcentration.png)

### A Deceleration in Growth
* The province's growth rate has steadily declined over the last decade.
  * **2015 Growth**: 1.24%
  * **2020 Growth**: 1.04% (Slowest recorded in the 5-year span analysis).
* This slowing growth suggests a stabilizing population, which can relieve pressure on public resources like schools and hospitals in the long term

![Dashboard Overview](images/Deceleration.png)

### Strong Labor Force Potential
* The dependency burden is relatively low.
  * **Working Age (15-64)**: 62.05%
  * **Young Dependents (<15)**: 33.14%
  * **Old Dependents (>64)**: 4.80%
* Quezon Province has a massive available workforce. The challenge is ensuring local industries (agriculture, tourism, BPO) can absorb this supply to prevent brain drain to Metro Manila.

![Dashboard Overview](images/LaborForce.png)

# Recommendations
* **Job Creation in Key Hubs**: Focus economic zones in the top 10 populated LGUs (like Candelaria and Tayabas) to capitalize on the 62% working-age population.
* **Rural Development Programs**: Launch initiatives in the 30% least populated municipalities to improve density balance and reduce strain on major towns.
* **Senior Care Planning**: While the elderly population is currently low (4.8%), the slowing birth rate suggests this demographic will grow. Long-term planning for geriatric care should begin now.
