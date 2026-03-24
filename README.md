# Lightning Strike Analysis (2018): NOAA Data Exploration

## Project Overview
This project analyzes more than 3.4 million NOAA lightning records from 2018 to identify daily and seasonal strike patterns.  
The workflow demonstrates practical data cleaning, feature engineering, aggregation, and visualization in Python.  
Results show clear summer concentration, with August as the peak month.

## Project Background
NOAA monitors atmospheric activity, including lightning, using satellite-based systems such as the Geostationary Lightning Mapper (GLM).  
This project focuses on understanding how lightning activity changed over time across 2018.

## Project Goal
Use Python in a Jupyter Notebook to:
- prepare and validate NOAA lightning data,
- calculate total lightning strikes by day and month,
- visualize month-level trends.

## Dataset
- **Source file:** `lightning_strikes_1.csv`
- **Size:** 3,401,012 rows, 3 columns
- **Columns:**
- `date` (string, converted to datetime)
- `number_of_strikes` (integer)
- `center_point_geom` (geospatial point text)

## Tools and Libraries
- Python
- Jupyter Notebook
- pandas
- numpy
- datetime
- matplotlib

## Method
1. Load and inspect dataset with `head()`, `shape`, and `info()`.
2. Convert `date` to datetime format.
3. Create a `month` feature from `date`.
4. Aggregate total strikes by day and rank highest-activity days.
5. Aggregate total strikes by month.
6. Build a monthly bar chart (`month_txt` vs `number_of_strikes`).

## Key Findings
- Lightning activity peaks strongly in summer months.
- **August** had the highest monthly total with **15,525,255** strikes.
- Top daily strike counts were concentrated in August (for example, August 29 had 1,070,457 strikes).

## Monthly Totals (2018)

| Month | Total Strikes |
|---|---:|
| Jan | 860,045 |
| Feb | 2,071,315 |
| Mar | 854,168 |
| Apr | 1,524,339 |
| May | 4,166,726 |
| Jun | 6,445,083 |
| Jul | 8,320,400 |
| Aug | 15,525,255 |
| Sep | 3,018,336 |
| Oct | 1,093,962 |
| Nov | 409,263 |
| Dec | 312,097 |

## Visualization Summary
The monthly bar chart shows a gradual rise from spring into summer, a sharp peak in August, and then a steady decline through fall and winter.  
This pattern indicates strong seasonality in 2018 lightning behavior.

## How to Run
1. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib jupyter
   ```
2. Place `lightning_strikes_1.csv` in your project/notebook directory.
3. Open the notebook and run cells in sequence.
4. Review output tables and the monthly strike visualization.

## Notes
- If the full dataset is not included in the repo due to size, use a truncated sample for demonstration and document the limitation.

## Source
- Project reference: https://shadyeggs.github.io/2018-NOAA-Lightning-Strike-Data/
- Data origin: NOAA lightning observations (2018)
