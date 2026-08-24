# Acme Armadillos Attendance Analysis

Take-home case study analyzing declining attendance for the Acme Armadillos, diagnosing the root causes, and sizing a recommendation to reverse the trend.

## Folder Structure

```
provided_materials/          Original case study materials (data + prompt) as provided
analysis/
  step_01_clean_data/        Raw data cleaning and validation
  step_02_analysis/          All diagnostic and sizing analysis (see below)
```

## provided_materials/

The original case data and prompt, unmodified.

## analysis/step_01_clean_data/

- **step_01_clean_data.ipynb** — Loads the raw case data, identifies and fixes data quality issues (creates one single dataset, fixes corrupted Day of Week values, and an outlier Group Tickets row), and outputs the cleaned dataset.
- **clean_data.csv** — The cleaned dataset used by every notebook in step_02_analysis. 3 seasons (2021-2023), 243 games.

## analysis/step_02_analysis/

Run in this order:

| Notebook | What it covers |
|---|---|
| **01_initial_look.ipynb** | First broad look at the data. YoY ticket/revenue trends, breakdown by segment (Full Season, Partial Season, Group, Single Game), cuts by day of week/month, and no-show rates. Identifies where the decline is concentrated and prioritizes what to dig into next. |
| **02_single_game_deep_dive.ipynb** | Deep dive into Single Game's decline on Monday/Tuesday/Wednesday/Sunday. Rules out price and scheduling artifacts, confirms the decline is broad and real, and concludes it's a behavior shift specific to casual, one-off buyers. |
| **03_full_season_price_relationship.ipynb** | Tests whether price is actually driving Full Season's decline (which it is and statistically confirmed). Explores the price/attendance relationship, models different pricing scenarios, and lands on a "hold price flat and test" recommendation. |
| **04_partial_season_success.ipynb** | Documents Partial Season's growth story, gaining share on the exact days Single Game is struggling, commanding a real price premium, with no sign of price sensitivity. Builds the case for a dedicated new package. |
| **05_recommendation_sizing.ipynb** | Final sizing of the recommendation. The 3-2-1 and 3-6-9 Partial Season plans, working backward from a 75% overall Partial Season growth goal to determine what each lever (organic growth, 3-2-1, 3-6-9) needs to deliver. |
| **deck_views.ipynb** | Standalone chart renderings used directly in the final presentation deck. Not part of the analytical narrative, just a reference notebook for reproducing deck visuals. |
