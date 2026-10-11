# 🏥 Healthcare Operations: Optimizing Patient Post-Discharge Interventions & Predicting 30-Day Readmission Risk

## 📋 Executive Summary
 
This project delivers an end-to-end data pipeline and predictive modeling framework using the **Behavioral Risk Factor Surveillance System (BRFSS)** dataset. By identifying the core demographic and clinical drivers of readmission, this solution enables hospital administrators to accurately identify high-risk patients, allowing clinical teams to deploy targeted, cost-effective follow-up care.

---

## 🛠️ Tools & Skills Demonstrated
*   **Language:** R (v4.x)
*   **IDE:** RStudio / GitHub Desktop
*   **Key Packages:** `tidyverse` (data wrangling), `caret` or `tidymodels` (machine learning), `ggplot2` (data visualization), `ROCR` (evaluation)
*   **Domain Competencies:** Healthcare Operations, Predictive Analytics, Risk Stratification, Data Cleaning & Imputation

---

## 🔄 Data Pipeline & Architecture

### 1. Data Management & Preprocessing
*   **High-Volume Wrangling:** Filtered and cleaned survey data records from the BRFSS dataset.
*   **Feature Engineering:** Encoded categorical health indicators (e.g., physical activity) and handled class imbalances to ensure robust model training.

### 2. Statistical Analysis & Insights
*   Executed exploratory data analysis (EDA) to map out key correlations.
*   *Key Finding:* [Insert a quick 1-sentence insight here later, e.g., "Patients reporting 'Poor' general health combined with a history of diabetes showed a 3x higher likelihood of readmission."]

### 3. Predictive Modeling & Evaluation
*   **Methodology:** Deployed **Logistic Regression** for the binary classification of 30-day readmissions, and **Linear Regression** to analyze continuous operational metrics [e.g., length of stay, if applicable].
*   **Clinical Interpretability:** Selected regression-based frameworks over complex "black-box" models to ensure full interpretability of feature weights (Odds Ratios). This allows hospital stakeholders to transparently audit exactly which risk factors (such as chronic comorbidities or demographic elements) are driving the risk scores.

### 4. Feature Engineering & Clinical Data Rules 
The model handles complex health survey coding from the BRFSS codebook by transforming raw categorical responses into actionable mathematical variables:

*   **PERSDOC2 (Outcome Variable):** Classifies whether a patient has a primary care physician. Re-encoded into a binary target (`1` for Yes, `0` for No). Refusals (`7`, `9`) were cleanly omitted.
*   **POORHLTH (Predictor):** Captures the number of poor physical/mental health days in the past month. Standardized by converting code `88` (None) to `0` days, mapping `1-30` directly, and purging non-responses.
*   **MAXDRNKS (Predictor):** Quantifies heavy alcohol consumption (1-76 drinks). Removed statistical outliers using [Insert 1.5x IQR / 3SD here] to prevent extreme variances from breaking linearity assumptions.
*   **SMOKE100 (Predictor):** Categorical factor tracking if a patient has smoked >100 cigarettes. Processed as a binary indicator (`1` = Yes, `0` = No) to capture behavioral risk.


---

## 📈 Operational & Financial Impact
Instead of looking at data retroactively, this model gives hospital management a forward-looking tool:
*   **Resource Optimization:** Reduces administrative waste by routing home-health checkups and follow-up calls *only* to patients tracking above a specific risk threshold.
*   **Penalty Mitigation:** Directly addresses CMS HRRP financial risks by proactively preventing avoidable 30-day readmissions.

---

## 🚀 How to Run this Project
1. Clone the repository:
   ```bash
   git clone https://github.com
   ```
2. Open the project in **RStudio**.
3. Run `01_data_cleaning.R` to process the raw BRFSS data.
4. Run `02_modeling.R` to train the models and output performance metrics.

---

## Objectives
- Identify key factors associated with hospital readmission risk  
- Explore relationships between health behaviors and outcomes  
- Generate visual insights using R-based analysis  
- Lay groundwork for future GIS-based spatial analysis  

---

## Data Source
- Behavioral Risk Factor Surveillance System (BRFSS)
- Centers for Disease Control and Prevention (CDC)

---

## Methods
- Data cleaning and preprocessing in R  
- Exploratory Data Analysis (EDA)  
- Descriptive statistics and group comparisons  
- Data visualization using `ggplot2`  
- Summary interpretation of health trends  

---

## Tools & Libraries
- R / RStudio  
- tidyverse  
- ggplot2  
- dplyr  
- BRFSS dataset  

---

## Repository Structure
- **BRFSS_analysis/**  
  Contains the main R Notebook with full analysis and visualizations  

- **future_project_2/**  
  Placeholder for future analysis project  

- **future_project_3/**  
  Placeholder for future expansion (including GIS integration)

---

## Key Insights (to be updated after final review)
- [ main finding 1]  
- [ main finding 2]  
- [ main finding 3]  

---

## Future Work
- Integrate GIS mapping to identify and analyze geographic health disparities  
- Improve predictive modeling of health data and readmission probability    
- Expand dataset features for deeper analysis  
- Develop interactive dashboard including key findings 

---

## Author
Edlyn P.
