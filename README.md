# FloodRelief-Planner
This project provides a lightweight decision-support tool for planning relief supplies during floods in Bangladesh. It forecasts the number of people affected (per upazila &amp; district) and translates those into daily relief needs.
## Overview
This project provides a lightweight decision-support tool for planning relief supplies during floods in Bangladesh.
It forecasts the number of people affected (per upazila & district) and translates those into daily relief needs:

Safe water (liters per day)

Food ration-days (per day)

Emergency shelter kits

The approach is deliberately transparent and simple, so responders and judges can understand the assumptions.
## Files
upazilas.csv – pilot upazilas with population and flood risk tags

rain_forecast.csv – daily rainfall forecasts (24h, or let script compute 3- & 7-day sums)

river_level.csv – optional template for river gauge inputs (not used in MVP)

FloodReliefMVP.ipynb – Kaggle-ready notebook (can also run as .py script)

Outputs:
planner_upazila_level.csv → daily estimates by upazila

district_totals_next_N_days.csv → totals per district for the next 3 days

## How It Works
Inputs:

Population & vulnerability tags (flood-prone, river proximity)

Rainfall forecast (24h / 3-day / 7-day totals)

Risk Score:

Adds points if 3-day or 7-day rain exceeds thresholds

Adds points for flood-prone areas or river-nearby upazilas

Affected People Estimate:

Maps risk → % of population affected (with uncertainty bands P50 / P90)

Conversion to Relief Quantities:

Water: 15 L per person per day

Food: 1 ration-day per person per day

Shelter: 1 kit per 4 people

Outputs:

Clear CSVs + plots for decision makers

Optional bar/line charts for presentations

planner_upazila_level.csv → daily estimates by upazila

district_totals_next_N_days.csv → totals per district for the next 3 days
