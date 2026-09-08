# Analyzing Crime in Los Angeles

Exploratory analysis of LAPD crime reports to find when crimes peak, where night crimes are most common, and which victim age groups are affected most. The goal is to help the LAPD allocate patrols and outreach more effectively.

The data is a modified version of the public [Los Angeles Open Data](https://data.lacity.org/) crime dataset.

## Project files

| File | Description |
|------|-------------|
| `notebook.ipynb` | Analysis notebook with markdown, comments, and results |
| `crimes.csv` | Crime reports used in the notebook |

## Questions

1. **Peak crime hour** — Which hour of the day has the most crimes? Stored in `peak_crime_hour`.
2. **Night crime location** — Which patrol area has the most crimes between 10:00 p.m. and 3:59 a.m.? Stored in `peak_night_crime_location`.
3. **Victim ages** — How many crimes fall in each victim age group (`0-17` through `65+`)? Stored in `victim_ages`.

## Findings

- **Peak hour:** noon (`12`) has the highest number of reported crimes.
- **Night crime hotspot:** Central has the most crimes between 10:00 p.m. and 3:59 a.m.
- **Victim ages:** adults aged 26–34 are the largest victim group, followed by 35–44. Victims aged 0–17 are the smallest group.

## How to run

1. Open `notebook.ipynb` in Jupyter, VS Code, or Cursor.
2. Run all cells from the top so later steps can use the `HOUR` column created in the first analysis cell.

Required packages:

```text
pandas
numpy
matplotlib
seaborn
```

Install them with:

```bash
pip install pandas numpy matplotlib seaborn
```

## Data dictionary (`crimes.csv`)

| Column | Description |
|--------|-------------|
| `DR_NO` | Division of Records Number (year, area ID, and file number) |
| `Date Rptd` | Date the crime was reported |
| `DATE OCC` | Date the crime occurred |
| `TIME OCC` | Time of occurrence in 24-hour military time |
| `AREA NAME` | LAPD geographic area / patrol division |
| `Crm Cd Desc` | Description of the crime |
| `Vict Age` | Victim's age in years |
| `Vict Sex` | Victim's sex (`F`, `M`, `X` = unknown) |
| `Vict Descent` | Victim's descent code (see the notebook for the full key) |
| `Weapon Desc` | Weapon used, if applicable |
| `Status Desc` | Crime status |
| `LOCATION` | Street address of the crime |
