![Platform](https://img.shields.io/badge/Platform-Python_3.12-blue)
![Platform](https://img.shields.io/badge/Platform-PostgreSQL_16-blue)
![Tool](https://img.shields.io/badge/Tool-Jupyter_Notebook-orange)
![Tool](https://img.shields.io/badge/Tool-Power_BI-yellow)
![Tool](https://img.shields.io/badge/Tool-SQL-orange)
![Domain](https://img.shields.io/badge/Domain-Pharmacovigilance-lightgrey)
![Method](https://img.shields.io/badge/Method-Signal_Detection_ROR-green)
![Data](https://img.shields.io/badge/Data-FDA_FAERS_2022_2025-blue)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

# FDA Drug Adverse Event Signal Detection & Pharmacovigilance Analysis
## Identifying Safety Signals Across High-Volume Pharmaceutical Products | January 2022 to April 2025

## Project Overview
This project applies pharmacovigilance methodology to the FDA Adverse Event
Reporting System (FAERS) to detect drug safety signals across five high volume
pharmaceutical products: Aspirin, Ibuprofen, Paracetamol, Metformin and
Atorvastatin. Using the Reporting Odds Ratio (ROR), the industry standard
signal detection method used by regulatory data teams at major pharmaceutical
organisations, this project identifies statistically elevated adverse event
patterns, temporal trends, demographic risk profiles and drug specific reaction
signatures across 6,000 adverse event reports covering January 2022 to
April 2025.

## Objectives
- Assess the distribution of serious, fatal and hospitalisation adverse events across five pharmaceutical products
- Analyse patient demographic profiles including age group and sex distribution
- Identify the most frequently reported adverse reactions across all products combined
- Track serious event and death rate trends across the 2022 to 2025 period
- Examine the geographical distribution of adverse event reporting
- Compare serious event and death rates across all five pharmaceutical products
- Assess disabling and life threatening event rates by drug
- Identify drug specific adverse reaction profiles for each product
- Detect pharmacovigilance safety signals using Reporting Odds Ratio methodology
- Analyse age and sex interaction effects on serious event rates
- Present findings in a comparative drug heatmap and summary scorecard
- Execute 15 SQL analytical queries against a PostgreSQL 16 database
- Present key findings in an interactive Power BI dashboard

## Data Source
| | |
|---|---|
| **Publisher** | U.S. Food and Drug Administration |
| **Dataset** | FDA Adverse Event Reporting System (FAERS) |
| **Access** | openFDA API — open.fda.gov/apis/drug/event |
| **Coverage** | January 2022 to April 2025 |
| **Records** | 6,000 adverse event reports across five pharmaceutical products |
| **Frequency** | Quarterly updates |
| **Licence** | Public domain CC0 |

## Tools and Libraries
| Tool | Purpose |
|---|---|
| Python 3.12 | Core programming language |
| pandas | Data manipulation and transformation |
| numpy | Statistical calculations |
| matplotlib | Data visualisation |
| seaborn | Statistical visualisation and heatmaps |
| scipy | Signal detection statistics |
| requests | openFDA API data retrieval |
| SQLAlchemy | Python to PostgreSQL connection |
| psycopg2 | PostgreSQL database adapter |
| PostgreSQL 16 | Database storage and SQL analysis |
| Jupyter Lab | Interactive analysis environment |
| Power BI Desktop | Interactive dashboard |
| Git | Version control |

## Key Findings

### Mortality — Ibuprofen
Ibuprofen recorded the highest death rate at 20.50%, more than double the
next highest drug Metformin at 13.10%. The disproportionately high death rate
relative to its serious event rate of 79.60% may suggest that when ibuprofen
adverse events are serious they could be more likely to be fatal than
equivalent events for other drugs in the dataset.

### Serious Events
81.15% of all 6,000 adverse event reports were classified as serious.
Paracetamol recorded the highest serious event rate at 93.65% and Aspirin
recorded the lowest at 72.80%. The serious event rate increased consistently
from 80.42% in 2022 to 91.94% in 2025, an upward trend of 11.52 percentage
points over 3 years and 4 months. This trend could reflect a shift in the
reporting population towards higher acuity patients over the period.

### Hospitalisation
Atorvastatin recorded the highest hospitalisation rate at 40.80% and
Paracetamol recorded the lowest at 25.60%. The relatively low hospitalisation
rate for Paracetamol despite its high serious event rate may suggest that
serious Paracetamol adverse events could predominantly result in outcomes
other than hospitalisation such as disability or life threatening events.

### Disabling Events
Paracetamol recorded the highest disabling event rate at 22.25%,
significantly higher than Ibuprofen at 8.60% and Atorvastatin at 4.40%.
Aspirin recorded the lowest disabling event rate at 1.30%. The high disabling
rate for Paracetamol could be partially attributable to the opioid combination
product population captured within the dataset.

### Life Threatening Events
Life threatening event rates were broadly consistent across all five drugs
ranging from 3.70% for Aspirin to 5.60% for Paracetamol. This relatively
narrow range may suggest that life threatening outcomes could be distributed
relatively evenly across drug types regardless of their overall serious event
profiles.

### Death Rate Trend
The death rate declined from 11.00% in 2022 to 8.40% in 2024 before
increasing sharply to 12.90% in 2025. The 2025 increase of 4.50 percentage
points represents the largest single year on year change in the dataset and
could reflect emerging safety signals that may warrant further investigation
once complete 2025 quarterly data becomes available.

### Signal Detection — Reporting Odds Ratio
The strongest signal identified was Paracetamol (Drug withdrawal syndrome)
at ROR 777.39, supported by (Drug dependence) at ROR 176.88 and (Emotional
distress) at ROR 149.22. These signals may be consistent with opioid
combination products containing acetaminophen rather than plain paracetamol.
Metformin (Lactic acidosis) was identified at ROR 49.34, a signal consistent
with established medical literature on lactic acidosis risk in patients with
renal impairment. Ibuprofen signals included Joint swelling at ROR 8.25,
Hypersensitivity at ROR 7.97 and Rash at ROR 7.05. Aspirin (Anaemia) was
identified at ROR 3.80, which may be consistent with known gastrointestinal
bleeding risk. Atorvastatin — Fall at ROR 2.27 could be consistent with
statin associated muscle weakness in elderly patients.

### Opioid Combination Products — Paracetamol
The Paracetamol dataset may have captured opioid combination products
containing acetaminophen in addition to plain paracetamol. This could be
evidenced by the dominance of Drug dependence, Drug withdrawal syndrome and
Overdose in the reaction profile and the ROR analysis. FDA drug name searches
by active ingredient may capture the full range of combination products and
not exclusively single ingredient formulations.

### Demographics — Age
The 85 and over age group recorded the highest serious event rates across
both sexes — Female 93.75% and Male 87.32%. The 65 to 84 age group was the
largest known age group at 1,534 records, which could be consistent with
the chronic disease profile of the drugs analysed. Serious event rates
appeared to increase with age across both sexes, which may reflect the
increased vulnerability of elderly patients to serious drug reactions.

### Demographics — Sex
Female patients accounted for 51.88% of reports and male patients 48.12%.
Female patients dominated the 18 to 44 age group with 410 reports compared
to 169 male reports, which could be consistent with known patterns of higher
adverse event reporting among women of reproductive age. Male patients
recorded higher serious event rates than females in the Under 18 and 45 to
64 age groups, though the clinical significance of this pattern may require
further investigation with a larger dataset.

### Geography
The United States accounted for 54.79% of all reports, consistent with
FAERS being a US FDA database. The United Kingdom ranked third globally with
376 reports representing 6.29% of the dataset. Canada ranked second with
539 reports at 9.01%.

### Data Quality
39.73% of records had no patient age recorded and 7.87% had no sex recorded.
The January 2022 batch submission of 5,017 records represents 83.6% of all
2022 records, which may have created significant imbalance in the yearly
distribution and could have limited the reliability of temporal trend analysis.

## Python Analysis
| Step | Description |
|---|---|
| 1 | Import libraries and configure API connection |
| 2 | Pull adverse event data from openFDA API for five drugs |
| 3 | Parse nested JSON into structured DataFrame |
| 4 | Data quality assessment — missing values and distributions |
| 5 | Data cleaning — date conversion, label mapping and age group assignment |
| 6 | Analysis 1 — Serious vs non-serious event distribution |
| 7 | Analysis 2 — Death reports by drug |
| 8 | Analysis 3 — Hospitalisation reports and rates by drug |
| 9 | Analysis 4 — Patient sex distribution by drug |
| 10 | Analysis 5 — Age group distribution by drug |
| 11 | Analysis 6 — Top 20 most reported adverse reactions |
| 12 | Analysis 7 — Serious event and death rate trends 2022 to 2025 |
| 13 | Analysis 8 — Top 15 reporting countries |
| 14 | Analysis 9 — Serious event rate comparison by drug |
| 15 | Analysis 10 — Disabling and life threatening event rates by drug |
| 16 | Analysis 11 — Drug specific reaction profiles |
| 17 | Analysis 12 — Reporting Odds Ratio signal detection |
| 18 | Analysis 13 — Age and sex interaction serious event rates |
| 19 | Analysis 14 — Drug comparison heatmap |
| 20 | Analysis 15 — Summary scorecard |

## SQL Queries
| Query | Description |
|---|---|
| 1 | Total records and drug distribution |
| 2 | Serious event distribution |
| 3 | Death reports by drug |
| 4 | Hospitalisation rate by drug |
| 5 | Sex distribution |
| 6 | Age group distribution |
| 7 | Serious event rate by drug |
| 8 | Yearly trend analysis |
| 9 | Top 15 reporting countries |
| 10 | Disabling event rate by drug |
| 11 | Life threatening event rate by drug |
| 12 | Serious event rate by age group and sex |
| 13 | Month on month change using LAG window function |
| 14 | Comprehensive drug safety summary |
| 15 | Yearly death rate trend using LAG window function |

## Evidence

### Analysis 1 — Serious vs Non-Serious Events
[![analysis1](figures/analysis1_serious_events.png)](figures/analysis1_serious_events.png)

### Analysis 2 — Death Reports by Drug
[![analysis2](figures/analysis2_death_reports.png)](figures/analysis2_death_reports.png)

### Analysis 3 — Hospitalisation Reports by Drug
[![analysis3](figures/analysis3_hospitalisation.png)](figures/analysis3_hospitalisation.png)

### Analysis 4 — Patient Sex Distribution
[![analysis4](figures/analysis4_sex_distribution.png)](figures/analysis4_sex_distribution.png)

### Analysis 5 — Age Group Distribution
[![analysis5](figures/analysis5_age_distribution.png)](figures/analysis5_age_distribution.png)

### Analysis 6 — Top 20 Most Reported Reactions
[![analysis6](figures/analysis6_top_reactions.png)](figures/analysis6_top_reactions.png)

### Analysis 7 — Serious Event and Death Rate Trends
[![analysis7](figures/analysis7_yearly_trend.png)](figures/analysis7_yearly_trend.png)

### Analysis 8 — Top 15 Reporting Countries
[![analysis8](figures/analysis8_country_distribution.png)](figures/analysis8_country_distribution.png)

### Analysis 9 — Serious Event Rate by Drug
[![analysis9](figures/analysis9_serious_rate_by_drug.png)](figures/analysis9_serious_rate_by_drug.png)

### Analysis 10 — Disabling and Life Threatening Rates
[![analysis10](figures/analysis10_disabling_lifethreat.png)](figures/analysis10_disabling_lifethreat.png)

### Analysis 11 — Drug Specific Reaction Profiles
[![analysis11](figures/analysis11_reactions_by_drug.png)](figures/analysis11_reactions_by_drug.png)

### Analysis 12 — ROR Signal Detection
[![analysis12](figures/analysis12_ror_signals.png)](figures/analysis12_ror_signals.png)

### Analysis 13 — Age and Sex Interaction
[![analysis13](figures/analysis13_age_sex_interaction.png)](figures/analysis13_age_sex_interaction.png)

### Analysis 14 — Drug Comparison Heatmap
[![analysis14](figures/analysis14_drug_heatmap.png)](figures/analysis14_drug_heatmap.png)

### Analysis 15 — Summary Scorecard
[![analysis15](figures/analysis15_summary_scorecard.png)](figures/analysis15_summary_scorecard.png)

## How to Run

### Prerequisites
- Python 3.8 or higher
- PostgreSQL 14 or higher
- Power BI Desktop — powerbi.microsoft.com/desktop
- Jupyter Lab

### 1. Clone the Repository
```bash
git clone git@github.com:Kingsley-Eboh/fda-adverse-events-analysis.git
cd fda-adverse-events-analysis
```

### 2. Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn scipy requests sqlalchemy psycopg2-binary jupyter
```

### 3. Get an openFDA API Key
Register for a free API key at open.fda.gov/apis/authentication and replace
YOUR_API_KEY_HERE in the notebook with your key before running.

### 4. Set Up PostgreSQL
Create a local PostgreSQL database and user. Update the connection string in
the Section 6 data load cell with your credentials before running.

### 5. Run the Notebook
Launch Jupyter Lab and open fda_adverse_events_analysis.ipynb:
```bash
jupyter lab
```
Select Kernel → Restart and Run All Cells to execute all cells in sequence.

### 6. Run the SQL Queries
Once the database is populated execute the analytical queries:
```bash
psql -U your_user -d portfolio -h localhost -f sql/fda_adverse_events_queries.sql
```

### 7. Open the Power BI Dashboard
Open powerbi/fda_dashboard.pbix in Power BI Desktop and reconnect to your
local PostgreSQL instance using your configured credentials when prompted.

## Project Structure

```
fda-adverse-events-analysis/
├── fda_adverse_events_analysis.ipynb    # Main analysis notebook
├── figures/
│   ├── analysis1_serious_events.png
│   ├── analysis2_death_reports.png
│   ├── analysis3_hospitalisation.png
│   ├── analysis4_sex_distribution.png
│   ├── analysis5_age_distribution.png
│   ├── analysis6_top_reactions.png
│   ├── analysis7_yearly_trend.png
│   ├── analysis8_country_distribution.png
│   ├── analysis9_serious_rate_by_drug.png
│   ├── analysis10_disabling_lifethreat.png
│   ├── analysis11_reactions_by_drug.png
│   ├── analysis12_ror_signals.png
│   ├── analysis13_age_sex_interaction.png
│   ├── analysis14_drug_heatmap.png
│   └── analysis15_summary_scorecard.png
├── sql/
│   └── fda_adverse_events_queries.sql   # All 15 SQL queries
├── powerbi/
│   └── fda_dashboard.pbix               # Power BI dashboard
├── .gitignore
└── README.md
```
## Author
**Kingsley Eboh**
[GitHub](https://github.com/Kingsley-Eboh)

*Data sourced from the FDA Adverse Event Reporting System via the openFDA API.
This project is intended for portfolio and educational purposes. All analysis
was conducted in an isolated Ubuntu VM environment.*
