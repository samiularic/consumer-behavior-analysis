# consumer-behavior-analysis
Python-based regression analysis of digital purchase behavior among U.S. women's apparel consumers using 2019 transaction data.
Consumer Behavior Analysis: Domain-Level Demand in Online Women's Apparel

Overview
This repository contains Python-based regression analysis examining digital purchase behavior among U.S. women's apparel consumers using a 2019 transaction panel, a nationally representative U.S. consumer dataset. This research is conducted at the Feliciano School of Business, Montclair State University, under the supervision of Dr. Patrali Chatterjee, Chairperson, Department of Marketing. It targets publication in the Journal of Retailing and Consumer Services or Electronic Commerce Research and Applications. This work was presented at the Montclair State University Student Research Symposium on April 24, 2026.

Research Questions
RQ1: Does domain choice independently predict clothing spending after controlling for household demographics?
RQ2: Do loyal and multi-platform shoppers differ in annual spending intensity, clothing category breadth, and channel preferences?
RQ3: Do households at the same income level but different household structures show different domain preferences?

Dataset
Source: comScore 2019 Transaction Panel

Scope: Tens of thousands of women's apparel transactions across 9 major U.S. retail domains
Demographic variables: Income, education, age, household size, presence of children, census region
Behavioral variables: Domain-level purchase activity, basket totals, product totals
Note: The dataset is proprietary and not included in this repository.

Methods
OLS Regression (Models 1 and 2): Log-transformed basket total and log(prod_totprice + 1) as dependent variables. Amazon.com set as reference domain. Clustered standard errors at machine_id level to account for repeat household purchases. Seasonal and demographic controls included.
Logistic Regression (Model B): Predicts multi-platform brand-switching behavior using household demographics and census geography as predictors.
Brand Extraction: Regex applied in Python to extract brand-level information from product description fields.

Key Findings
RQ1: All 9 domain indicators are statistically significant predictors of spending. Demographic controls lose significance once domain dummies enter the model, directly answering RQ1. Blair.com and QVC.com show the highest spending coefficients. Q4 seasonality is a significant spending driver.
RQ2: 83% of households are loyal single-domain shoppers. 17% are multi-platform shoppers. Multi-platform shoppers show substantially higher transaction frequency and annual spend. Income, younger age, presence of children, and Southern or Western census region significantly predict multi-platform behavior.
Incidental Spend: In a majority of sessions, incidental spend exceeds clothing spend. Blair.com generates the highest incidental spend per session of any domain in the sample.

Tools
Python (Google Colab), Statsmodels, Pandas, NumPy
Regex for brand extraction
Excel for data preparation, dummy variable construction, and loyalty analysis

Status
RQ3 analysis and category breadth analysis are in progress. Full thesis integration ongoing.
