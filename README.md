# Facebook-vs-Google-Ads-A-B-Testing-Regression-Analysis
Analyzed Facebook and Google AdWords campaign performance using Python, evaluating clicks, conversions, CTR, and advertising costs. Applied EDA, correlation analysis, hypothesis testing, linear regression, and time-series analysis to identify performance trends, compare campaign effectiveness, and derive data-driven marketing optimization insights.

## Project Overview

This project analyzes and compares the performance of two digital advertising campaigns: **Facebook Ads and Google AdWords**.

The primary objective is to identify which advertising platform delivers better results in terms of clicks, conversions, and advertising cost-effectiveness.

Using Python and statistical techniques, this project explores campaign performance, identifies patterns in customer engagement, evaluates the relationship between clicks and conversions, and examines advertising cost trends over time.

The analysis is based on 365 days of campaign data from January 1, 2019, to December 31, 2019.

## Business Problem

Marketing agencies aim to maximize Return on Investment (ROI) while ensuring efficient utilization of advertising budgets.

Running campaigns across multiple platforms requires understanding which platform generates more conversions at a lower cost.

This project addresses the following business questions:

- Which platform generates more clicks and conversions?
- Which advertising platform has a higher conversion rate?
- Is there a strong relationship between ad clicks and conversions?
- Is the difference in campaign conversions statistically significant?
- How accurately can conversions be predicted based on clicks?
- How do campaign conversions and advertising costs vary over time?
- Which periods offer better cost efficiency?

## Dataset Description

The dataset contains daily performance metrics for Facebook and Google AdWords advertising campaigns throughout 2019.

**Dataset size:** 365 records and 17 columns.

### Key Features

| Feature | Description |
|---|---|
| Date | Daily campaign date |
| Ad Views | Number of ad impressions/views |
| Ad Clicks | Total clicks received |
| Ad Conversions | Number of conversions generated |
| Cost per Ad | Daily advertising expenditure |
| Click-Through Rate (CTR) | Percentage of views resulting in clicks |
| Conversion Rate | Percentage of clicks resulting in conversions |
| Cost per Click (CPC) | Average advertising cost per click |

## Technologies & Libraries

- Python
- Pandas – Data manipulation and analysis
- NumPy – Numerical computations
- Matplotlib – Data visualization
- Seaborn – Statistical visualization
- SciPy – Statistical hypothesis testing
- Scikit-learn – Linear regression and model evaluation
- Statsmodels – Time-series and cointegration analysis
- Jupyter Notebook – Interactive data analysis

## Project Workflow

### 1. Data Loading and Preprocessing

- Imported the campaign dataset using Pandas.
- Examined dataset dimensions, data types, and descriptive statistics.
- Converted the date column into datetime format.
- Cleaned currency and percentage columns.
- Converted categorical and numerical fields into appropriate formats.

### 2. Exploratory Data Analysis (EDA)

Performed exploratory analysis to understand campaign performance.

- Analyzed the distribution of clicks and conversions.
- Compared daily conversion frequencies across both platforms.
- Created conversion categories to identify high- and low-performing days.
- Used histograms, bar charts, and scatter plots to visualize campaign metrics.

### 3. Correlation Analysis

Investigated the relationship between advertising clicks and conversions.

**Facebook:**
- Correlation coefficient: 0.87

**Google AdWords:**
- Correlation coefficient: 0.45

Facebook demonstrated a stronger positive relationship between clicks and conversions in the analyzed dataset.

### 4. Statistical Hypothesis Testing

Conducted an independent two-sample Welch's t-test to evaluate whether Facebook generated significantly more daily conversions than Google AdWords.

**Hypotheses:**

- Null Hypothesis (H0): Facebook's mean daily conversions are less than or equal to AdWords.
- Alternative Hypothesis (H1): Facebook's mean daily conversions are greater than AdWords.

**Results:**

| Metric | Facebook | AdWords |
|---|---:|---:|
| Average Daily Conversions | 11.74 | 5.98 |

- T-statistic: 32.88
- P-value: 9.35 × 10⁻¹³⁴
- Significance Level: 0.05

The extremely low p-value provides strong statistical evidence that Facebook generated higher average daily conversions in this dataset.

### 5. Regression Analysis

Developed a Linear Regression model to predict Facebook ad conversions based on the number of ad clicks.

**Independent Variable:** Facebook Ad Clicks

**Dependent Variable:** Facebook Ad Conversions

**Model Evaluation:**

- R² Score: 76.35%
- Mean Squared Error: 2.02

**Sample Predictions:**

| Ad Clicks | Expected Conversions |
|---:|---:|
| 50 | 13.00 |
| 80 | 19.31 |

The model captures a substantial proportion of the variation in daily Facebook conversions.

### 6. Time-Series Analysis

Analyzed Facebook campaign performance over time to identify temporal patterns.

- Extracted month and weekday information from campaign dates.
- Compared conversion trends across weekdays.
- Analyzed monthly conversion performance.
- Examined monthly advertising expenditure and cost per conversion.
- Applied a cointegration test to investigate the long-term relationship between advertising expenditure and conversions.

The analysis identified variations in monthly conversions and advertising costs, highlighting opportunities for campaign optimization.

## Key Findings

1. **Higher Conversions:** Facebook generated approximately 11.74 average daily conversions compared to 5.98 for Google AdWords.

2. **Stronger Click-Conversion Relationship:** Facebook showed a correlation of 0.87, compared to 0.45 for AdWords.

3. **Statistical Significance:** Hypothesis testing provided strong evidence of a difference in average daily conversions between the two platforms.

4. **Predictive Analytics:** Linear Regression achieved an R² score of 76.35% when predicting Facebook conversions using clicks.

5. **Temporal Patterns:** Monthly and weekday analysis revealed fluctuations in campaign performance and opportunities to optimize advertising schedules.

6. **Cost Analysis:** Monthly cost-per-conversion calculations helped identify periods of relatively better advertising efficiency.

## Business Recommendations

Based on the analysis:

- Prioritize Facebook campaigns for further optimization and testing due to their higher observed conversion volume.
- Investigate Google AdWords targeting, keywords, and landing-page performance to improve conversion efficiency.
- Monitor conversion rates alongside click volume instead of evaluating campaign performance using clicks alone.
- Use predictive modelling to establish realistic conversion targets.
- Evaluate monthly cost per conversion before reallocating advertising budgets.
- Conduct controlled experiments before making large-scale budget allocation decisions.

## Project Structure

```text
Facebook-vs-Google-AdWords-Campaign-Analysis/
│
├── marketing_campaign.csv
├── Marketing_Campaign_Analysis.ipynb
├── README.md
```

## Future Improvements

- Perform A/B testing to compare campaign effectiveness.
- Develop advanced predictive models for conversion forecasting.
- Incorporate ROI and Return on Ad Spend (ROAS) calculations.
- Analyze audience demographics and campaign segmentation.
- Build an interactive Power BI or Streamlit dashboard.
- Perform time-series forecasting for future campaign performance.

## Conclusion

This project demonstrates how data analytics and statistical modelling can support digital marketing decisions.

Based on the analyzed 2019 dataset, Facebook outperformed Google AdWords in average daily conversions and demonstrated a stronger relationship between clicks and conversions.

However, higher conversion volume alone does not establish higher profitability. Actual ROI, revenue per conversion, and total acquisition costs should also be considered before making final budget allocation decisions.

---

**Author:** Archita Sinha

**Domain:** Data Analytics | Marketing Analytics | Statistical Analysis | Predictive Modelling
