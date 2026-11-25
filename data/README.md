# Dataset

**Smart Healthcare-DailyLife Dataset Wearable device**

- **Source:** <https://www.kaggle.com/datasets/mdimammahdi/smart-healthcare-dailylife-dataset-wearable-device>
- **File:** `smart_healthcare_dailylife_wearable.csv`
- **Size:** 700 rows (100 participants × 7 days) × 15 columns
- **License:** as published on Kaggle by the dataset author.

## Columns

| Column | Description |
|---|---|
| `ID` | Participant identifier (1–100) |
| `Day` | Observation day (1–7) |
| `Gender` | `M`/`F` or `Male`/`Female` (mixed coding in the raw file) |
| `Age (years)` | Participant age |
| `Height (meter)` | Height in metres |
| `Weight (kg)` | Weight in kilograms |
| `BMI` | Body-mass index |
| `Step Count` | Steps taken that day |
| `Distance Travel (Km)` | Distance travelled that day |
| `Blood Pressure` | Systolic/diastolic as text, e.g. `120/82` |
| `Heart Rate (BPM)` | Resting heart rate |
| `Blood Oxygen Level` | SpO₂ percentage |
| `Sleep Duration (minutes)` | Sleep that night |
| `Screen Time (minute)` | Screen time that day |
| `Earphone Time (minute)` | Earphone use that day |

## Notes

- The CSV is bundled here so the notebook runs with **no setup**.
- If you remove this file, the notebook will automatically download the dataset with
  `kagglehub.dataset_download("mdimammahdi/smart-healthcare-dailylife-dataset-wearable-device")`
  (no API key required for this public dataset).
- The raw file uses two gender codings (`M`/`F` for participants 1–28, `Male`/`Female`
  for 29–100); the notebook standardises these before analysis.
