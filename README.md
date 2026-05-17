# A/B Test Results Analysis
### E-commerce Conversion Rate Study | Python, Statistics, Logistic Regression

---

## Project Overview

This project analyzes the results of an A/B test conducted by an e-commerce company that developed a new web page intended to increase the number of users who convert (i.e., decide to purchase the product). The goal is to determine whether the company should implement the new page, keep the old page, or run the experiment longer before making a decision.

The analysis covers descriptive statistics, probability, hypothesis testing via simulation, and logistic regression modeling — providing both statistical and practical conclusions.

---

## Key Question

> Should the e-commerce company switch to the new landing page based on the A/B test data?

**Conclusion: No.** There is no statistically significant evidence that the new page leads to higher conversion rates. The p-value of 0.394 is well above the 0.05 significance threshold, and logistic regression confirms this result (p = 0.754). Country of origin also had no meaningful effect on conversion.

---

## Dataset

| Feature | Description |
|---|---|
| `user_id` | Unique identifier for each user |
| `timestamp` | Time of the visit |
| `group` | Whether the user was in `control` or `treatment` |
| `landing_page` | Whether the user saw `old_page` or `new_page` |
| `converted` | 1 if the user converted, 0 if not |
| `country` | Country of the user (US, UK, CA) |

- Total observations: **294,478**
- Control group: **147,239** users
- Treatment group: **147,239** users

---

## Methods Used

- Descriptive Statistics
- Conditional Probability
- Hypothesis Testing (Simulation / Bootstrapping)
- Logistic Regression (statsmodels)
- Dummy Variable Encoding
- Data Visualization (matplotlib)

---

## Tools and Libraries

| Tool | Purpose |
|---|---|
| Python 3 | Core programming language |
| pandas | Data manipulation and analysis |
| NumPy | Numerical computing and simulation |
| matplotlib | Data visualization |
| statsmodels | Logistic regression modeling |
| Jupyter Notebook | Interactive analysis environment |

---

## Results Summary

### Descriptive Statistics
- Overall conversion rate: **11.90%**
- No missing values in the dataset
- Users distributed across three countries: US (70%), UK (17%), CA (13%)

### Conversion Rates by Group and Country

|           | US    | UK    | CA    |
|-----------|-------|-------|-------|
| Control   | 11.8% | 12.3% | 12.0% |
| Treatment | 12.0% | 11.7% | 12.0% |

### Hypothesis Test (Simulation)

| Metric | Value |
|---|---|
| Control conversion rate | 11.88% |
| Treatment conversion rate | 11.92% |
| Observed difference | +0.04% |
| Simulated p-value | 0.394 |
| Significance threshold | 0.05 |
| Decision | Fail to reject H0 |

### Logistic Regression

| Model | ab_page p-value | Conclusion |
|---|---|---|
| Page only | 0.754 | Not significant |
| Page + Country | 0.752 | Not significant |
| US coefficient p-value | 0.509 | Not significant |
| UK coefficient p-value | 0.940 | Not significant |

---

## Files in This Repository

| File | Description |
|---|---|
| `analyze_ab_test_results_COMPLETED.ipynb` | Completed Jupyter Notebook with all code and analysis |
| `Analyze_AB_Test_Results_COMPLETED.pdf` | Presentation deck summarizing the results |
| `Analyze_AB_Test_Results_COMPLETED.pptx` | Editable PowerPoint version of the presentation |

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/ab-test-analysis.git
   ```
2. Place `ab_data.csv` in the same folder as the notebook
3. Open the notebook in Jupyter:
   ```bash
   jupyter notebook analyze_ab_test_results_COMPLETED.ipynb
   ```
4. Run all cells from top to bottom

---

## Author

**Mukhtar Dualeh**  
