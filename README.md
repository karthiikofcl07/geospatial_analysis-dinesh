# 🌍 Geospatial Analysis of Restaurant Distribution
### Data Analysis Internship Project

---

## 📌 Project Overview

This project performs a comprehensive **geospatial analysis** of restaurant data collected across **15 countries** and **141 cities** worldwide. The analysis encompasses three primary objectives:

1. **Visualization** — Mapping restaurant locations using latitude and longitude coordinates via interactive and static plots.
2. **Distribution Analysis** — Examining how restaurants are distributed across countries and cities.
3. **Correlation Study** — Investigating whether a restaurant's geographic location correlates with its aggregate rating.

---

## 📁 Project Structure

```
geospatial_analysis/
│
├── Geospatial_Analysis.ipynb        ← Main Jupyter Notebook (full analysis)
├── Dataset_.csv                     ← Source dataset (9,551 restaurant records)
│
├── outputs/
│   ├── interactive_map.html         ← Interactive Folium map with cluster markers
│   ├── heatmap.html                 ← Restaurant density heatmap (dark theme)
│   ├── fig1_distribution_country_city.png   ← Country & city distribution bar charts
│   ├── fig2_ratings_by_country.png          ← Boxplot & mean rating by country
│   ├── fig3_correlation_location_rating.png ← Scatter plots: lat/lon vs rating
│   ├── fig4_geo_rating_map.png              ← Global map colored by rating
│   ├── fig5_top_cities_rating.png           ← Top 20 cities by average rating
│   ├── fig6_rating_overview.png             ← Rating histogram & category pie chart
│   └── summary_statistics.csv              ← Key metrics summary table
│
├── README.md                        ← This file
└── Project_Explanation.txt          ← Detailed plain-text task explanation
```

---

## 📊 Dataset Description

| Column | Description |
|--------|-------------|
| `Restaurant ID` | Unique identifier for each restaurant |
| `Restaurant Name` | Name of the restaurant |
| `Country Code` | Numeric country identifier |
| `City` | City where the restaurant is located |
| `Latitude / Longitude` | Geographic coordinates |
| `Cuisines` | Type(s) of cuisine served |
| `Average Cost for two` | Average dining cost for two people |
| `Aggregate rating` | Overall rating (0.0 – 5.0 scale) |
| `Rating text` | Categorical label (Poor, Average, Good, Very Good, Excellent) |
| `Votes` | Total number of user votes |

---

## 🔧 Technologies Used

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading, cleaning, and manipulation |
| `numpy` | Numerical computations |
| `matplotlib` | Static charts and plots |
| `seaborn` | Statistical visualizations |
| `folium` | Interactive geospatial maps |
| `scipy` | Pearson correlation and statistical testing |

---

## ▶️ How to Run

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn folium scipy
```

### Execute Notebook
```bash
jupyter notebook Geospatial_Analysis.ipynb
```

Or run all cells from top-to-bottom. All output files will be automatically saved to the `outputs/` directory.

---

## 📈 Key Findings

| Finding | Detail |
|---------|--------|
| **Dominant Country** | India accounts for over 90% of all restaurant records |
| **Top City** | New Delhi with 5,473 restaurants |
| **Best-Rated Country** | Indonesia and Philippines rank highest in mean ratings |
| **Latitude–Rating Correlation** | r ≈ −0.07 (weak, statistically significant) |
| **Longitude–Rating Correlation** | r ≈ −0.04 (very weak, statistically significant) |
| **Interpretation** | Geographic coordinates alone are weak predictors of rating; cultural and regional standards play a larger role |

---

## 📝 Notes

- Restaurants with a rating of `0.0` are excluded from all correlation and rating-based analyses as they represent unrated entries.
- The interactive HTML maps open in any modern web browser — no additional software required.
- The Folium cluster map samples up to 2,000 points for performance; the heatmap uses the full valid dataset.

---

*Analysis conducted as part of a Data Analytics Internship. All findings are based solely on the provided dataset.*
