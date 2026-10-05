# Ethical concerns about AI in healthcare: survey analysis code

This repository holds the analysis code for the paper "Ethical concerns about artificial intelligence in healthcare among patients, healthcare professionals and AI developers".
## Aim of the survey

The study was a cross-sectional online survey of patients, healthcare professionals and AI developers. It aimed to describe and compare their views on key ethical issues in the use of AI in healthcare, and to use the results to inform proposed governance recommendations. It asked three questions:

1. What are participants' views on bias, privacy, explanations, informing patients, accountability, trust, autonomy, ethical guidelines, human oversight and disparities in access to care?
2. Do these views differ between the three groups?
3. Do any differences remain after taking account of age, gender, continent and familiarity with AI?

The survey ran on Microsoft Forms from 29 July to 31 August 2026 and was shared on LinkedIn. 253 people took part. The study was approved by the University of Hertfordshire Health, Science, Engineering and Technology Ethics Committee with Delegated Authority (protocol 2274 SFa HSET 2026).

The sample is a convenience sample. The results do not apply to any wider population.

## Data

`data/survey_clean.csv` holds the anonymised, cleaned answers of all 253 participants. `data/data_dictionary.csv` describes each column.

## Folders

| Folder | What it holds |
|---|---|
| `data/` | `data_dictionary.csv` (description of each column); `survey_clean.csv` (cleaned survey data, see Data above) |
| `notebooks/` | Six Jupyter notebooks, described below |
| `results/` | Result files written by the notebooks (CSV) |

## Notebooks

Notebooks 01 to 05 read only `data/survey_clean.csv`, and each can be run on its own. Notebook 06 reads the result files, so run it last.

| Notebook | What it does | In the paper |
|---|---|---|
| `01_descriptive` | Participant characteristics; all answers with 95% confidence intervals; accountability combinations | Table 1, Results |
| `02_group_comparisons` | Group comparisons for the 12 primary outcomes; Holm correction; effect sizes | Table 2 |
| `03_associations` | Exploratory: number of parties held accountable; Spearman correlations between views | Fig 3, Tables D and E |
| `04_regression` | Regression models adjusted for age group, gender, continent and familiarity with AI | Table 3, Table B |
| `05_sensitivity` | Other codings of Q7, Q9, Q14 and Q16 | Table C |
| `06_figures` | Figures 1 to 3 (run 01 and 03 first) | Figs 1-3 |


## How to run

You need Python 3.10 and `data/survey_clean.csv` in the `data/` folder.

1. Install the packages (fixed versions):

   ```
   pip install -r requirements.txt
   ```

2. Run the notebooks in order from inside the `notebooks/` folder:


3. The outputs are written to `results/`.
