# Socioeconomic Predictors of Average ACT Scores Across U.S. States

> Examining how socioeconomic factors relate to average ACT scores across U.S. States.

---

## Project Overview

Provide a short and concise overview of the project. Mention the problem it solves, the data used, and the key outcomes or findings.

- **Objective:** To analyze how socioeconomic factors such as household income, unemployment, and family structure relate to average ACT scores across U.S. high schools.
- **Domain:** Education
- **Key Techniques:** Regression, Data Imputation, Exploratory Data Analysis

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** https://github.com/brian-fischer/DATA-5100/blob/main/EdGap_data.xlsx , https://www.dropbox.com/scl/fi/fkafjk8902sq8ptxh94r2/ccd_sch_029_1617_w_1a_11212017.csv?rlkey=gucrdz5f6e38bezz2y3yalxbw&dl=0 , https://github.com/vtc03/education/blob/main/data/Stfis170_1a.xlsx
- **Description:** The dataset combines information from the National Center for Education Statistics (NCES) and EdGap, containing socioeconomic and school-level data across 20 states. All data are stored in CSV and Excel format and merged into a single DataFrame for analysis.
- **License:** (if applicable)

---

## Analysis

The analysis imports three sources: EdGap_data.xlsx (EdGap/ACT and sociodemographics), Stfis170_1a.xlsx (NCES state finance), and ccd_sch_029_1617_w_1a_11212017.csv (NCES school directory).Then cleans types, removes invalid IDs and out-of-range ACT values, and merges records by school ID and state. Exploratory work includes summary statistics, pair plots, and a correlation heatmap to assess relationships among socioeconomic variables. A clean data file is saved as education_clean.csv. Missing predictor values are addressed with a multivariate Iterative Imputer, preserving an unaltered copy for reference. A cleaned dataset is exported as education_clean.csv. Modeling proceeds from single-predictor linear and quadratic regressions using median income to a multiple linear regression including the selected socioeconomic features. Performance is evaluated with R squared, MAE, and RMSE, with residual plots and standardized coefficient for easy interpretation. 

---

## Results

The analysis shows that socioeconomic factors strongly influence ACT performance. Areas with more college-educated adults tend to have higher ACT scores, while higher unemployment and larger percentages of students on free or reduced lunch are linked to lower scores. Median income alone is a weak predictor, and state total revenue shows little to no positive effect. Overall, education level and economic stability appear to be the most meaningful predictors of student achievement.

---

## Authors

- Vincent Chan - [@vtc03](https://github.com/vtc03)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Tools/libraries used: pandas, NumPy, matplotlib, seaborn, statsmodels
- Tutorials or papers referenced
- Inspiration or collaborators: Brian Fischer
