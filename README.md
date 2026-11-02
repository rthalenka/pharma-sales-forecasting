# Pharmaceutical Sales Forecasting | Time Series Analysis in R

A time series forecasting project analyzing seasonal demand patterns in pharmaceutical retail sales. Using the Box-Jenkins methodology, SARIMA models and benchmark forecasting techniques, the project explores how historical sales data can support more informed demand planning and inventory management.

## Project Overview

Pharmaceutical demand is influenced by seasonal patterns, particularly for products associated with recurring conditions such as allergies. Understanding these patterns can help retailers anticipate fluctuations in demand and make better inventory planning decisions.

This project analyzes monthly sales volumes for systemic antihistamines (ATC category R06), applying statistical forecasting methods to identify seasonality, model historical trends and evaluate out-of-sample predictive performance.

## Key Results

- Identified and modeled seasonal patterns in monthly pharmaceutical sales.
- Applied a Guerrero-optimized Box-Cox transformation to stabilize variance.
- Used seasonal differencing and Augmented Dickey-Fuller testing to assess stationarity.
- Developed a SARIMA(1,0,1)(0,1,1)[12] forecasting model.
- Compared the final model against ETS, Seasonal Naïve and Historical Mean benchmarks.
- Evaluated model performance using a 16-month holdout period.
- Performed residual diagnostics, including Ljung-Box testing, to assess whether the model errors behaved like white noise.

## Methodology

The analysis follows a structured time series forecasting workflow:

1. **Data preparation:** Exploration, cleaning and aggregation of daily sales transactions into monthly observations.
2. **Exploratory analysis:** Identification of trend, seasonal patterns and variance characteristics.
3. **Transformation and stationarity:** Application of a Box-Cox transformation and seasonal differencing, supported by statistical testing.
4. **Model development:** Estimation and comparison of candidate SARIMA specifications.
5. **Benchmarking:** Comparison against ETS, Seasonal Naïve and Historical Mean forecasting methods.
6. **Model evaluation:** Assessment using a 16-month out-of-sample holdout period and RMSE-based comparisons.
7. **Residual diagnostics:** Ljung-Box testing to evaluate remaining autocorrelation.

## Dataset

The project uses the [Pharma Sales Dataset](https://www.kaggle.com/datasets/milanzdravkovic/pharma-sales-data) by Milan Zdravković.

- **Source:** Kaggle
- **Original data:** Daily pharmaceutical sales transactions
- **Time coverage:** Approximately six years
- **Analysis scope:** ATC category R06 – Antihistamines for systemic use
- **Analysis frequency:** Monthly

## Tools & Technologies

| Category | Technologies |
|---|---|
| Programming language | R |
| Forecasting | fpp3, fable |
| Time series analysis | tsibble |
| Statistical testing | urca |
| Data manipulation | lubridate |
| Reporting | R Markdown, rmdformats |

## Repository Structure

```text
pharma-sales-forecasting/
│
├── pharma-sales-forecasting-code.Rmd
├── pharma-sales-forecasting-report.html
├── pharma-sales-data.RData
├── salesdaily.csv
└── README.md
```

- `pharma-sales-forecasting-code.Rmd` – Annotated R Markdown source containing the analysis and forecasting workflow.
- `pharma-sales-forecasting-report.html` – Rendered report with visualizations, analysis and results.
- `pharma-sales-data.RData` – Saved R dataset.
- `salesdaily.csv` – Original daily sales dataset.

## How to Explore the Project

1. Review the R Markdown source file to understand the complete analytical workflow.
2. Open the rendered HTML report to explore the visualizations, model comparisons and diagnostic results.
3. Refer to the original dataset to understand the underlying sales observations.

[**View the interactive forecasting report →**](https://rthalenka.github.io/pharma-sales-forecasting/pharma-sales-forecasting-report.htm)

## Project Context

Academic project developed as part of the Information Management degree at NOVA IMS.

The analysis demonstrates the application of statistical time series methods to a practical business problem, combining data preparation, forecasting, model evaluation and analytical reporting.
