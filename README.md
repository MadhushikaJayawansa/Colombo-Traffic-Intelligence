# Colombo-Traffic-Intelligence

## Measuring traffic delays, congestion patterns, , fuel impact, and estimated economic cost  from 2013 to 2019


## Project Overview

Sri Lanka’s transport authorities are reviewing how to allocate limited resources to tackle traffic congestion in Colombo. They need to identify which road corridors experience the most severe congestion and where commuters may be losing the most time.

As a data analyst, my role in this project is to analyse historical traffic data, compare congestion and speed loss across corridors, and estimate the time cost of a 10 km vehicle trip. The findings aim to help decision-makers identify priority areas for further investigation and more informed traffic management planning.

## Key Findings

Union Place / Ibbanwala Link: Recorded an average congestion index of 4.83, speed loss of 69.05%, and estimated time cost of approximately LKR 690 per 10 km vehicle trip. This corridor is a candidate for further congestion investigation.

T.B. Jayah Mawatha / Darley Road: Recorded an average congestion index of 5.00, speed loss of 60%, and estimated time cost of approximately LKR 600 per 10 km vehicle trip. Its high recorded congestion and estimated time cost make it another priority for investigation.

Morning vs evening congestion: Havelock/Pamankada recorded an evening-minus-morning congestion difference of approximately +1 index point. This suggests that commute-period differences should be considered when investigating traffic management needs.

## Tableau Dashboards

The project includes three interactive dashboards:

Colombo Traffic Overview — Compares corridor congestion, peak and off-peak speeds, speed loss, morning/evening congestion, and estimated time cost.

Congestion Cost & Priority — Highlights estimated time costs and corridors with high congestion and speed loss.

Commute Patterns & Context — Explores morning/evening congestion and directional asymmetry.

Dashboard access: Open dashboard/The_Price_of_Congestion_Colombo.twbx to explore the packaged Tableau workbook.

Screenshots:

[Colombo Traffic Overview](C:\Users\Nanny\Desktop\archive (3)\traffic\Colombo Traffic Intelligence\Colombo-Traffic-Intelligence\dashboard\screenshots\Colombo Traffic Overview 1.PNG)

<a href="dashboard\screenshots\Colombo Traffic Overview 1.PNG">
  <img src="Colombo Traffic Overview 1.PNG" alt="Colombo Traffic Overview">
</a>



[Congestion Cost & Priority](C:\Users\Nanny\Desktop\archive (3)\traffic\Colombo Traffic Intelligence\Colombo-Traffic-Intelligence\dashboard\screenshots\Congestion Cost & Priority 1.PNG)


[Commute Patterns & Context](C:\Users\Nanny\Desktop\archive (3)\traffic\Colombo Traffic Intelligence\Colombo-Traffic-Intelligence\dashboard\screenshots\WHERE CONGESTION COSTS THE MOST.PNG)


## Data & Tools

Data Sources

Traffic observations: Historical corridor-level observations from September 2014 to December 2019, with gaps in recorded periods.

Fuel-price data: Historical fuel prices used as context for the cost model.

## Tools Used

Python: Data cleaning and preparation.

Power Query: Data integration and transformation.

PostgreSQL: Data storage and analytical views.

SQL: Metric calculations and corridor comparisons.

Tableau Desktop: Interactive dashboard development.

GitHub: Project documentation and version control.

## Metrics & Methodology


|      Metric         |          Definition                                |            Important caveat          |
|-------------------------|----------------------------------------------------|--------------------------------------|
| Congestion index        | Average recorded congestion index by corridor                  | Reflects available historical observations from September 2014 to December 2019, with gaps in the data. |
| Speed loss (%)          | Reduction in peak speed relative to off-peak speed             | Requires valid peak and off-peak speeds; corridors with identical speeds are excluded from speed-loss comparisons. |
| Estimated time cost     | Additional travel time multiplied by the assumed value of time | Illustrative estimate per 10 km vehicle trip, not measured financial loss. |
| Corridor priority score | 60% congestion percentile + 40% speed-loss percentile          | Relative project-specific score, not an official government ranking. |

## Estimated Cost Assumptions

Trip distance: 10 km

Value of time: LKR 500 per hour

Fuel economy: 12 km per litre

Assumed additional fuel consumption: 15%

Fuel-price benchmark: Petrol 92

Estimated delay (hours) = (10 / peak speed) − (10 / off-peak speed)

Estimated time cost (LKR) = Estimated delay × LKR 500 per hour


##  Recommendations

Investigate priority corridors: Conduct updated traffic surveys on Union Place / Ibbanwala Link and T.B. Jayah Mawatha / Darley Road to validate congestion and speed-loss patterns.

Improve traffic monitoring: Collect consistent peak and off-peak speed observations across corridors to support more reliable comparisons over time.

Strengthen future analysis: Match traffic and weather records by date and location, and use more detailed road-level incident data where available, before drawing stronger conclusions about causes or safety outcomes.

