# Pharmaceutical Sales Demand Forecasting (SARIMA & ETS)

An applied time series forecasting analysis predicting monthly retail sales volumes for systemic antihistamines (ATC category R06) using the Box-Jenkins methodology in R (`fpp3`, `fable`).

## Executive Summary
* **Problem:** Antihistamine sales exhibit high variance tied to seasonal biological cycles, complicating inventory procurement and risk of stockouts.
* **Methodology:** Applied Guerrero-optimized Box-Cox transformation for variance stabilization, followed by seasonal differencing ($D=1$) to establish stationarity confirmed via ADF unit root tests (GTS procedure).
* **Modeling & Benchmarks:** Formulated and estimated candidate SARIMA models alongside benchmark algorithms (ETS, Seasonal Naïve, Historical Mean) and RMSE-weighted combinations.
* **Key Findings:** Residual diagnostic testing (Ljung-Box, $p > 0.05$) validated white-noise error distributions on the final SARIMA(1,0,1)(0,1,1)[12] specification, confirming strong out-of-sample predictive accuracy across a 16-month holdout window.

## Project Structure
* `pharma-sales-forecasting-code.Rmd` — Full annotated R Markdown code pipeline.
* `salesdaily.csv` — Point-of-sale transactional dataset aggregated to monthly frequency.

## Dataset & Provenance
* **Source:** [Pharma Sales Data on Kaggle](https://www.kaggle.com/datasets/milanzdravkovic/pharma-sales-data) by Milan Zdravković.
* **Scope:** 6 years of daily transactional Point-of-Sale records aggregated to monthly frequency, focusing on ATC category **R06** (Antihistamines for systemic use).
  

## Tech Stack & Libraries
* **Language:** R
* **Core Libraries:** `fpp3`, `fable`, `tsibble`, `urca`, `lubridate`, `rmdformats`


---
> **Interactive Report:** To view the formatted report with interactive tables and plots, download [`pharma-sales-forecasting-report.html`](./pharma-sales-forecasting-report.html) and open it in any web browser.
