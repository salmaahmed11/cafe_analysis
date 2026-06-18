# # Coffee Shop Sales — Exploratory Data Analysis

Exploratory data analysis on a real coffee shop's transaction records spanning March 2024 to March 2025, covering 3,636 sales across 8 drink types.

---

## Dataset

| Property | Details |
|---|---|
| File | `index_1.csv` |
| Records | 3,636 transactions |
| Period | March 2024 — March 2025 |
| Unique customers | 1,316 anonymized cards |

| Column | Description |
|---|---|
| `datetime` | Timestamp of the transaction |
| `cash_type` | Payment method (card / cash) |
| `card` | Anonymized customer card ID |
| `money` | Amount paid |
| `coffee_name` | Drink ordered |

---

## Cleaning Steps

- Filled 89 missing `card` values with `"No Card"` (cash transactions)
- Dropped redundant `date` column (kept full `datetime`)
- Converted `datetime` column to proper datetime type
- Verified zero duplicates

---

## Feature Engineering

New columns extracted from `datetime`:

| Feature | Description |
|---|---|
| `hour` | Hour of purchase |
| `day` | Day of month |
| `month` | Month number |
| `year` | Year |
| `time_of_day` | Morning / Afternoon / Evening / Night |

---

## Key Findings

**Most popular drinks:**

| Rank | Drink | Orders |
|---|---|---|
| 1 | Americano with Milk | 824 |
| 2 | Latte | 782 |
| 3 | Americano | 578 |
| 4 | Cappuccino | 501 |
| 5 | Cortado | 292 |

**Payment methods:** 97.6% card, 2.4% cash

**Price range:** 18.12 — 40.00 (avg ~31.75)

---

## Visualizations

- Most ordered coffee types (bar chart)
- Sales by time of day
- Revenue distribution
- Monthly sales trends
- Payment method breakdown

---

## Tech Stack

- **Python**
- **Pandas** — data loading, cleaning, feature engineering
- **Matplotlib / Seaborn** — visualizations
- **NumPy** — numerical operations
- **Jupyter Notebook**

---

## Project Structure

```
├── Untitled9.ipynb       # Main analysis notebook
├── index_1.csv           # Raw dataset
└── README.md
```
