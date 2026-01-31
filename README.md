<div align="center">
  <h1>🚲 Yulu Bike Rental Demand – Hypothesis Testing Analysis</h1>
  <p><strong>Identifying key factors driving electric cycle rentals in urban India</strong></p>

  <img src="https://socialify.git.ci/ravindrasudha/Yulu-Hypothesis-Testing/image?custom_language=Python&forks=1&issues=1&language=1&logo=https%3A%2F%2Fencrypted-tbn0.gstatic.com%2Fimages%3Fq%3Dtbn%3AANd9GcQ7kcOdkec7EPri4XE-Y53kVidR2_XSiOzxaQ%26s&name=1&owner=1&pulls=1&stargazers=1&theme=Light" 
       alt="Yulu Hypothesis Testing Project Banner" 
       width="720"/>

  <br/>

  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"/>
  <img src="https://img.shields.io/badge/Seaborn-FF6384?style=for-the-badge&logoColor=white" alt="Seaborn"/>
  <img src="https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=matplotlib&logoColor=white" alt="Matplotlib"/>
  <img src="https://img.shields.io/badge/Statistics-4CAF50?style=for-the-badge&logo=google-analytics&logoColor=white" alt="Statistics"/>
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter"/>
  <img src="https://img.shields.io/badge/Last%20Updated-Jul%202025-success?style=for-the-badge" alt="Updated"/>

</div>

<br/>

## 🎯 Problem Statement

Yulu — India’s leading micro-mobility platform — provides eco-friendly shared electric cycles for short urban commutes. Facing a significant revenue dip, Yulu needs to understand the key drivers of rental demand to optimize fleet allocation, pricing, and marketing.

**Business Questions**  
- Which factors (working day, season, weather, etc.) significantly influence the number of rentals?  
- How do environmental (temperature, weather) and calendar factors (season, holiday) affect demand?  
- Are there interdependencies among predictors (e.g., weather vs season)?

## 🚲 About Yulu

Yulu offers sustainable, app-based shared electric vehicles to reduce traffic congestion and enable convenient first/last-mile connectivity across metro stations, offices, residential areas, and more.

## 📊 Dataset Overview

- Hourly rental records  
- Key columns:  
  - `datetime`  
  - `season` (1=spring, 2=summer, 3=fall, 4=winter)  
  - `holiday` / `workingday`  
  - `weather` (1=clear → 4=heavy rain/snow)  
  - `temp`, `atemp`, `humidity`, `windspeed`  
  - `casual`, `registered`, `count` (total rentals)

## 🧪 Statistical Techniques Applied

- Bi-variate exploratory analysis (visualizations)  
- **2-sample T-test** — working day vs non-working day demand  
- **One-way ANOVA** — season & weather effects on rentals  
- **Chi-square test of independence** — season vs weather relationship

## 📈 Key Findings

- **Working day**: p-value = 0.2264 (> 0.05) → No statistically significant difference in average rentals  
- **Season**: ANOVA p-value < 0.0001 → Strong effect (peak in Fall & Summer)  
- **Weather**: ANOVA p-value < 0.0001 → Clear weather drives highest demand; severe weather reduces it sharply  
- **Season ↔ Weather**: Chi-square p-value < 0.0001 → Strong dependence (certain weather types more common in specific seasons)

**Conclusion**  
Season and weather are the primary demand drivers; working-day status adds little explanatory power.

## 💼 Business Recommendations

1. **Seasonal scaling** — Increase fleet & marketing in Summer/Fall; run promotions in Spring/Winter  
2. **Weather-adaptive operations** — Dynamic pricing, app weather alerts, proactive bike redistribution  
3. **Commuter focus** — Maintain high availability in office/metro zones year-round  
4. **Leisure opportunity** — Target weekends/holidays with recreational ride offers  
5. **Forecasting foundation** — Use season + weather features for predictive demand models

## 🖼️ Visual Highlights

<!-- Upload your plots to /screenshots folder and update paths -->

<div align="center">
  <img src="https://github.com/ravindrasudha/Yulu-Hypothesis-Testing/raw/main/screenshots/season_vs_count.png" alt="Rentals by Season" width="45%"/>
  <img src="https://github.com/ravindrasudha/Yulu-Hypothesis-Testing/raw/main/screenshots/weather_vs_count.png" alt="Rentals by Weather" width="45%"/>
</div>

## 🚀 How to Run

```bash
git clone https://github.com/ravindrasudha/Yulu-Hypothesis-Testing.git
cd Yulu-Hypothesis-Testing
pip install -r requirements.txt
jupyter notebook Yulu_Hypothesis_Testing.ipynb
