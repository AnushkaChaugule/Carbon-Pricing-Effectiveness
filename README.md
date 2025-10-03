Analyzing the Effectiveness of Carbon Pricing Across Industries & Regions
📄 Project Summary

This repository contains an analysis of how carbon pricing mechanisms (via effective carbon rates) correlate with emissions and GDP across industries and geographic regions. The goal is to assess whether carbon pricing is effective in reducing emissions, controlling for economic growth.

Key datasets include GDP data, emission statistics, and effective carbon rate (ECR) data from OECD and World Bank sources.

🧾 Data Sources
Dataset	Description	Link
GDP Data	National GDP / sector-level GDP measures	Google Sheets – GDP Data

Emission Data	Emissions by country / industry	World Bank – Emissions Data

Effective Carbon Rate (ECR)	Net effective carbon tax / price rates	OECD Data Explorer – ECR

Combined Datasheet	Pre-merged dataset used for analysis	Google Sheets – Combined
📂 Repository Structure
.
├── analysis.ipynb                # Jupyter Notebook with the full analysis
├── data/                         # Raw and processed data files
│   ├── gdp.csv
│   ├── emissions.csv
│   ├── ecr.csv
│   └── combined.csv
├── figures/                      # Visual outputs (charts, plots)
├── requirements.txt              # Python dependencies
└── README.md                     # This file

🛠 Methods & Workflow
1. Data Ingestion & Cleaning

Load GDP, emissions, and ECR datasets.

Clean and standardize formats (e.g. date formats, country/industry labels).

Handle missing values, duplicates, and potential inconsistencies.

2. Data Merging & Feature Engineering

Join datasets into a combined table keyed by country / year / industry.

Create derived metrics (e.g. emissions per GDP unit, carbon rate per unit emission).

Create lagged features or growth rates where relevant.

3. Exploratory Data Analysis (EDA)

Summary statistics and distributions.

Correlation analyses among ECR, emissions, and GDP.

Visualizations: time series trends, scatter plots, heatmaps, industry-level comparisons.

4. Modeling / Statistical Tests

Regression models (e.g. fixed effects, panel regressions) to test the effect of ECR on emissions, controlling for GDP growth.

Diagnostics and validation (residuals, multicollinearity, goodness-of-fit).

Robustness checks (e.g. lagged independent variables, sub-sample analyses).

5. Interpretation & Policy Insights

Interpreting coefficient estimates: Does a higher carbon rate lead to lower emissions?

Heterogeneity across industries or regions.

Policy relevance: how strong are the effects? Are they economically meaningful?

🎯 Key Findings & Implications

(Fill this section after your analysis — here are example placeholders.)

Carbon pricing effectiveness: A statistically significant negative association between ECR and emissions intensity (emissions/GDP) in several industries.

Heterogeneity: The carbon rate effect is stronger in heavy-polluting sectors (e.g. energy, transportation) than in service industries.

Economic trade-offs: Some countries show mild GDP growth dampening effects under higher ECR but overall net benefit in long-term decarbonization.

Policy implications: Suggest phased increases in carbon rates with sector-specific targeting, accompanied by subsidies or offsets in sensitive sectors.

🧩 How to Run / Reproduce

Clone the repository:

git clone https://github.com/AnushkaChaugule/Carbon-Pricing-Effectiveness.git
cd <repo-name>


Install dependencies:

pip install -r requirements.txt


Ensure your data/ folder has the CSV or sheet exports of GDP, emissions, ECR, and combined data.

Launch Jupyter:

jupyter notebook analysis.ipynb


Run each section in sequence to reproduce the workflow, figures, and results.

📋 Dependencies

Example requirements.txt may include:

pandas
numpy
matplotlib
seaborn
statsmodels
linearmodels
scipy

📚 Acknowledgments & References

World Bank – Emissions data source

OECD – Net Effective Carbon Rate data

Any academic papers or reports you referenced in justification

External tutorials or packages used
