# Financial Risk Analytics @ Stanford

- My final project of Financial Risk Analytics (MS&E246) @ Stanford University.
- Instructor: @ Kay Giesecke
- Language: Python

## SBA Loan Default Risk Project

This repository analyzes SBA loan default risk from end to end: data cleaning, macro-data integration, exploratory analysis, feature engineering, binary modeling, survival modeling, and simulation.

### Repository Structure

- `MS&E246_final_report.pdf`  
  My final project report.

#### `data/`

Primary raw SBA input files:

- `data/foia-504-fy1991-fy2009-asof-251231.csv`
- `data/foia-504-fy2010-present-asof-251231.csv`

These are the core raw loan data sources downloaded from [SBA website](https://data.sba.gov/en/dataset/7-a-504-foia). Additional folders such as `data/macro_clean/` contain cleaned macro data inputs.

#### `codes/`

- `1_data_cleaning.ipynb`  
  Cleans raw SBA loan records, standardizes field formats, handles missing values, and builds base variables.

- `2_macro_merge.ipynb`  
  Merges macroeconomic indicators (e.g., GDP, CPI, unemployment) with loan-level data by time and geography.

- `3_exploratory_data_analysis.ipynb`  
  Performs EDA with visualizations (default-rate time series, sector/state patterns, borrower characteristics, macro linkages).

- `4_feature_engineering.ipynb`  
  Builds modeling features and preprocessing pipelines for downstream models.

- `5_binary_model.ipynb`  
  Trains and evaluates binary default prediction models (`default` vs `non-default`).

- `6_survival_model.ipynb`  
  Runs competing risk survival modeling to study time-to-default dynamics.

- `7_simulation.ipynb`  
  Performs simulation and scenario analysis (including portfolio/tranche-related outputs).

