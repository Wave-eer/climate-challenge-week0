# Climate Vulnerability Analysis — Week 0 Challenge

## Overview
This project analyzes climate patterns across five African countries (Ethiopia, Kenya, Sudan, Tanzania, Nigeria) to assess relative climate vulnerability using historical weather data.

The goal is to produce data-driven insights to support Ethiopia’s position at COP32.

---

## Objectives
- Compare temperature trends across countries
- Evaluate precipitation variability
- Measure extreme heat and drought frequency
- Build a climate vulnerability ranking

---

## Project Structure
climate-challenge-week0/
│
├── data/                     
├── notebooks/
│   ├── task2_cleaning.ipynb
│   └── compare_countries.ipynb
├── app/                      
├── dashboard_screenshots/    
├── README.md
└── requirements.txt

---

## Setup

### Clone repository
git clone <https://github.com/Wave-eer/climate-challenge-week0>
cd climate-challenge-week0

### Create environment
python -m venv venv
venv\Scripts\activate

### Install dependencies
pip install -r requirements.txt

---

## Methodology

### Data Cleaning
- Replaced -999 with NaN
- Handled missing values (forward fill)
- Created DATE column from YEAR and DOY
- Standardized all datasets

### Analysis
- Monthly temperature trends (T2M)
- Precipitation variability (boxplots)
- Extreme heat (T2M_MAX > 35°C)
- Dry days (PRECTOTCORR < 1 mm)
- ANOVA test for statistical significance

### Vulnerability Index
Combined:
- Temperature mean and variability
- Precipitation variability
- Extreme heat frequency
- Dry day frequency

Normalized using MinMax scaling and summed into a final score.

---

## Key Results
- Temperature patterns differ across countries
- Rainfall variability is uneven
- Extreme events are concentrated in specific regions
- Statistical tests confirm differences are significant

---

## COP32 Insights
- Climate risk varies significantly across countries
- High variability increases vulnerability
- Ethiopia shows moderate relative risk
- Most vulnerable countries should be prioritized for climate finance

---

## Dashboard (Optional)
Streamlit app includes:
- Country selector
- Year range filter
- Interactive visualizations

---

## Deliverables
- Clean datasets (not tracked in Git)
- Analysis notebooks
- Final report (PDF)
- GitHub repository

---

## Author
Arsema Nekre
