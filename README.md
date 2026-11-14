# Zomato Restaurants - Exploratory Data Analysis

Exploratory data analysis of the Zomato restaurants dataset using **Python, pandas, Matplotlib and Seaborn**. The notebook looks at where Zomato restaurants are located, how they are rated, which cuisines are popular, and how delivery, table booking and pricing vary across countries and cities.

## Dataset

| Item | Detail |
|---|---|
| Records | 9,551 restaurants |
| Columns | 21 (22 after merging country names) |
| Countries | 15 |
| Files | `zomato.csv`, `Country-Code.xlsx` (see [`data/README.md`](data/README.md)) |

Key columns: `Restaurant Name`, `City`, `Cuisines`, `Average Cost for two`, `Has Table booking`, `Has Online delivery`, `Aggregate rating`, `Rating color`, `Rating text`, `Votes`.

## What the analysis covers

1. Data loading, inspection (`info`, `describe`) and missing-value check
2. Handling the 9 missing `Cuisines` values
3. Merging restaurant data with country codes
4. Country and city distribution (pie, donut and count plots)
5. Rating distribution and rating categories
6. Online delivery and table booking availability by country
7. Most popular cuisines, top-rated and costliest cuisines
8. Top-rated restaurants (rating >= 4.5 and more than 250 votes)
9. Votes vs. average cost for two

## Key findings

- **India dominates the data**: 8,652 of 9,551 records (about 90.6%), followed by the United States (434) and the United Kingdom (80).
- **Delhi NCR is the core**: New Delhi (5,473), Gurgaon (1,118) and Noida (1,080) have the most restaurants.
- **Many restaurants are unrated**: 2,148 have a rating of 0 ("Not rated"), and 2,139 of those are in India. Among rated restaurants, most ratings fall roughly between 2.7 and 4.4.
- **Online delivery is limited to two countries**: India (2,423 restaurants) and the UAE (28).
- **Table booking** is offered mostly in India (1,111), then the UAE (18), the Philippines (14) and the UK (12).
- **Popular cuisines**: North Indian is the most common, followed by North Indian + Chinese, Chinese and Fast Food.
- **Top-rated and popular restaurants** include Toit (Bangalore, 4.8, 10,934 votes), Truffles (Bangalore, 4.7) and Barbeque Nation (Kolkata, 4.9).
- `Is delivering now` is "Yes" for only 34 restaurants, and `Switch to order menu` is "No" for all, so these columns add little information.

## Selected charts

| | |
|---|---|
| ![Top countries](images/02_top4_countries_pie.png) | ![Ratings](images/06_rating_count_by_color.png) |
| ![Online delivery](images/08_online_delivery_by_country.png) | ![Popular cuisines](images/10_popular_cuisines.png) |
| ![Top cities](images/11_top_cities_by_restaurants.png) | ![Votes vs cost](images/12_votes_vs_cost_for_two.png) |

All charts are in the [`images/`](images/) folder.

## Project structure

```
zomato-eda/
├── notebooks/
│   └── Zomato_EDA.ipynb
├── data/
│   └── README.md          # where to get zomato.csv and Country-Code.xlsx
├── images/                # charts used in this README
├── requirements.txt
├── .gitignore
└── README.md
```

## How to run

```bash
git clone https://github.com/<your-username>/zomato-eda.git
cd zomato-eda
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
# add zomato.csv and Country-Code.xlsx to the data/ folder
jupyter notebook notebooks/Zomato_EDA.ipynb
```

## Tech stack

Python, pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

## Author

**<LakshmiPrasanna>** - [GitHub](https://github.com/petluriLakshmiPrasanna) | [LinkedIn](<linkedin.com/in/lakshmiprasanna-petluri-22baa5424>)
