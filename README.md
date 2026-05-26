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
| **Access** | openFDA API (open.fda.gov/apis/drug/event) |
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

### Mortality Finding — Ibuprofen
Ibuprofen recorded the highest death rate at 20.50%, more than double the
next highest drug Metformin at 13.10%. The proportion of ibuprofen adverse
events resulting in death appeared disproportionately high relative to its
overall serious event rate of 79.60%, which may suggest that ibuprofen
adverse events could be more likely to result in fatal outcomes than
equivalent events reported for other drugs in this dataset. This pattern
may warrant further investigation with a larger and more representative
dataset before firm conclusions can be drawn.

### Serious Adverse Events
Out of 6,000 adverse event reports analysed, 81.15% were classified as
serious by the reporting healthcare professional or patient. Paracetamol
had the highest proportion of serious events at 93.65% and Aspirin had the
lowest at 72.80%. The proportion of serious events across all five drugs
appeared to increase steadily from 80.42% in 2022 to 91.94% in 2025, an
upward trend of 11.52 percentage points over 3 years and 4 months. This
pattern could reflect a gradual change in the types of patients or clinical
situations being reported, though a larger dataset would be needed to
confirm this observation.

### Hospital Admissions
Atorvastatin had the highest rate of reports leading to hospital admission
at 40.80% and Paracetamol had the lowest at 25.60%. The relatively low
hospital admission rate for Paracetamol despite having the highest serious
event rate may indicate that serious Paracetamol adverse events could more
commonly result in other outcomes such as disability or life threatening
events rather than hospital admission. This interpretation should be treated
with caution given that the Paracetamol data may have captured opioid
combination products rather than plain paracetamol.

### Disabling Adverse Events
Paracetamol had the highest rate of adverse events resulting in disability
at 22.25%, substantially higher than Ibuprofen at 8.60% and Atorvastatin
at 4.40%. Aspirin had the lowest disabling event rate at 1.30%. The
elevated disabling rate for Paracetamol could be partially related to the
opioid combination products that may have been captured within the
Paracetamol search results.

### Life Threatening Adverse Events
The proportion of adverse events classified as life threatening was broadly
similar across all five drugs, ranging from 3.70% for Aspirin to 5.60% for
Paracetamol. This narrow range across very different drug types may suggest
that life threatening outcomes are distributed relatively evenly regardless
of which drug is involved, though the sample size of this analysis limits
the confidence with which this can be stated.

### Death Rate Over Time
The proportion of adverse event reports resulting in death appeared to
improve from 11.00% in 2022 to 8.40% in 2024 before rising sharply to
12.90% in 2025. The 2025 increase of 4.50 percentage points is the largest
single year on year change observed in the dataset. As the 2025 data
available at the time of this analysis covered only January to April, this
finding should be interpreted carefully until the full 2025 dataset becomes
available.

### Pharmacovigilance Signal Detection
A statistical method called the Reporting Odds Ratio (ROR) was used to
identify drug reaction combinations reported more frequently than would be
expected by chance. An ROR greater than 1 indicates a potential signal
worthy of further investigation.

The strongest signal identified was Paracetamol and Drug withdrawal syndrome
at ROR 777.39, supported by Drug dependence at ROR 176.88 and Emotional
distress at ROR 149.22. These signals may be consistent with opioid
combination products containing acetaminophen rather than plain paracetamol.
Metformin and Lactic acidosis was identified at ROR 49.34, a signal
consistent with established medical literature on lactic acidosis risk in
patients with renal impairment taking Metformin. Ibuprofen signals included
Joint swelling at ROR 8.25, Hypersensitivity at ROR 7.97 and Rash at ROR
7.05. Aspirin and Anaemia was identified at ROR 3.80, which may be
consistent with known gastrointestinal bleeding risk associated with long
term aspirin use. Atorvastatin and Fall was identified at ROR 2.27, which
could be consistent with muscle weakness in elderly patients taking statins,
though the relatively modest ROR value suggests this signal should be
interpreted with appropriate caution.

### Paracetamol and Opioid Combination Products
The Paracetamol data retrieved from the FDA database may have captured
opioid combination products such as those containing both acetaminophen and
codeine or oxycodone, in addition to plain paracetamol. This is suggested
by the high frequency of Drug dependence, Drug withdrawal syndrome and
Overdose in the reported reactions, which are not typical reactions
associated with plain paracetamol. The ROR analysis confirmed Drug
withdrawal syndrome as the strongest signal in the entire dataset at
ROR 777.39. This is an important consideration when interpreting Paracetamol
specific findings in this analysis, as the results may reflect the safety
profile of combination opioid products rather than paracetamol alone.

### Patient Age
Patients aged 85 and over had the highest rates of serious adverse events
across both male and female patients, at 93.75% and 87.32% respectively.
Patients aged 65 to 84 made up the largest age group with known age
information at 1,534 records, which could reflect the fact that all five
drugs are commonly prescribed for conditions that affect older adults.
Serious event rates appeared to increase with age in both male and female
patients, which may reflect the greater vulnerability of older patients to
serious adverse drug reactions. However 39.73% of records had no age
recorded, which means age related findings should be interpreted with
appropriate caution.

### Patient Sex
Female patients accounted for 51.88% of reports and male patients 48.12%.
Female patients made up a notably larger proportion of reports in the 18 to
44 age group with 410 reports compared to 169 for male patients, which
could be consistent with research suggesting women in this age group tend
to report adverse drug reactions more frequently. Male patients recorded
higher rates of serious events than female patients in the Under 18 and
45 to 64 age groups, though the clinical significance of this pattern may
require further investigation with a larger and more complete dataset.

### Reporting Countries
The United States accounted for 54.79% of all reports, consistent with
FAERS being a US FDA database. The United Kingdom ranked third globally
with 376 reports at 6.29% and Canada ranked second with 539 reports at
9.01%. The strong US dominance in reporting means findings may be more
representative of the US patient population than UK or global populations
and should be interpreted accordingly.

### Data Completeness
39.73% of records had no patient age recorded and 7.87% had no patient
sex recorded. A large batch of 5,017 records was submitted in January 2022,
representing 83.6% of all 2022 records. This concentration of records in a
single month may have affected the reliability of year on year trend
comparisons and should be considered when interpreting findings related to
reporting patterns over time.

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

*Data sourced from the FDA Adverse Event Reporting System via the openFDA API. This project is intended for portfolio and educational purposes.*
