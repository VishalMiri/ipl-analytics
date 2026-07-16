# IPL Cricket Analytics Dashboard (Power BI)

An interactive, end-to-end Power BI business intelligence application that cleanses, models, and visualizes historical Indian Premier League (IPL) data. This workspace uncovers deep team insights, match trends, and individual player performance analytics.

## 📊 Dashboard Views & Features

### 🏆 Tournament Highlights & Individual Accolades
![IPL Analysis Dashboard View](images/ipl_db.png)
*Features fully automated calculations tracking tournament leaders dynamically across changing tournament seasons.*

---

## 🛠️ Data Modeling & Engineering Architecture
A structured **Star Schema** data topology was implemented to minimize data redundancy and maximize rendering speeds across intensive page visualizations:

* **Fact Table:** `ball_by_ball_data` (capturing transactional ball events, runs, wicket variables).
* **Dimension Tables:** `ipl_matches_data` (match details, venues, dates) and `players-data-updated` (demographics, bios, and image directories).



---

## 💡 Advanced DAX & Analytical Calculations Implemented
Rather than relying on basic aggregations, this project utilizes custom time-intelligence and advanced context transition metrics, including:

1. **The Purple Cap Winner Engine:** Programmed contextual evaluation using `SUMMARIZE` combined with advanced `CALCULATETABLE` scoping to extract the highest seasonal wicket-taker while discarding invalid dismissal vectors (e.g., run-outs, retired hurts, timed outs).
2. **Dynamic Image Rendering:** Utilized `LOOKUPVALUE` parameters coupled with row-context string extractions to dynamically load player profile pictures directly from dimension tables when filtering seasonal metrics.

---

## 📈 Key Insights Uncovered
* **Dismissal Trends:** Non-bowler dismissals accounted for a distinct percentage of season-over-season wickets; isolating these variables altered true individual bowler value scoring by up to 12%.
* **Seasonal Shifts:** Certain bowling franchises maintain significantly higher efficiency scores when tracking structural home-ground boundaries versus neutral venue metrics.
