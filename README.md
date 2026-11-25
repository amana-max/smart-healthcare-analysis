# Smart Healthcare – Daily Lifestyle Analysis

A data-analysis project that studies how everyday lifestyle behaviour relates to health
indicators recorded by **wearable devices**. It uses **700 daily records from 100
participants observed over 7 days** and covers data loading, cleaning, descriptive
statistics, group comparisons, correlation analysis and visualisation in Python.

The whole project lives in a single, self-contained Jupyter notebook that runs
end-to-end in **Google Colab** or a local Jupyter environment.

---

## Dataset

**Smart Healthcare-DailyLife Dataset Wearable device** — a public Kaggle dataset.

- Source: <https://www.kaggle.com/datasets/mdimammahdi/smart-healthcare-dailylife-dataset-wearable-device>
- 700 rows (100 participants × 7 days) × 15 columns
- A copy is bundled in [`data/`](data/) so the notebook runs with no setup.

**Columns:** `ID`, `Day`, `Gender`, `Age (years)`, `Height (meter)`, `Weight (kg)`,
`BMI`, `Step Count`, `Distance Travel (Km)`, `Blood Pressure`, `Heart Rate (BPM)`,
`Blood Oxygen Level`, `Sleep Duration (minutes)`, `Screen Time (minute)`,
`Earphone Time (minute)`.

---

## Workflow

1. **Data loading and inspection** — read the CSV, check shape, columns, dtypes, missing values and summary statistics.
2. **Data cleaning and feature preparation** — standardise gender labels, split blood pressure into systolic/diastolic, derive age groups, BMI categories, a short-sleep flag and ACC/AHA blood-pressure categories.
3. **Descriptive statistics** — headline averages for activity, sleep, screen time and vitals.
4. **Group comparison** — lifestyle measures across age group, BMI category and gender.
5. **Correlation analysis** — pairwise correlation matrix and heat-map of the numeric attributes.
6. **Visualisation and interpretation** — 13 charts (histograms, scatter plots, bar charts, a heat-map and a 7-day trend line) with a written discussion of findings, limitations and future work.

---

## How to run

### Google Colab (recommended)
1. Go to <https://colab.research.google.com>.
2. **File → Upload notebook** and choose `Smart_Healthcare_Analysis.ipynb`.
3. **Runtime → Run all**.

The notebook loads the bundled `data/` CSV if present; otherwise it downloads the
dataset automatically with `kagglehub` (no API key needed for this public dataset).

### Local Jupyter
```bash
pip install -r requirements.txt
jupyter notebook Smart_Healthcare_Analysis.ipynb
```
Then run all cells top to bottom.

---

## Repository structure

```
.
├── Smart_Healthcare_Analysis.ipynb   # the full analysis notebook (with saved outputs)
├── README.md                         # this file
├── requirements.txt                  # Python dependencies
└── data/
    ├── README.md                     # dataset source and notes
    └── smart_healthcare_dailylife_wearable.csv
```

---

## Key findings

- Mean ≈ **8,357 steps** and **5.89 km** per day; about 38% of days reached 10,000 steps.
- Mean sleep ≈ **420 minutes (7.0 h)**; about 49% of nights were shorter than 7 hours.
- Mean screen time ≈ **326 min** and earphone time ≈ **130 min** per day.
- Mean heart rate ≈ **73.8 BPM**, blood oxygen ≈ **97.5%**, blood pressure ≈ **120/77 mmHg**.
- Step count and distance are almost perfectly correlated (r ≈ 0.97); screen time has a weak negative association with steps and sleep (r ≈ −0.23).

> Correlations show **association, not causation**. The dataset covers only 7 days per
> participant, so long-term trends cannot be studied.

---

## References

- McKinney, W. *Python for Data Analysis*, 3rd ed., O'Reilly Media, 2022.
- VanderPlas, J. *Python Data Science Handbook*, 2nd ed., O'Reilly Media, 2022.
- Whelton, P. K., et al. *2017 ACC/AHA Guideline for High Blood Pressure in Adults*, Hypertension, 2018.
- Kaggle dataset — <https://www.kaggle.com/datasets/mdimammahdi/smart-healthcare-dailylife-dataset-wearable-device>
