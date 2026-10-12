


# Colombo-Traffic-Intelligence

## Traffic Congestion, Speed Loss & Commuter Impact  from 2013 to 2019

A data analytics project investigating traffic congestion across selected road corridors in Colombo, Sri Lanka.



## 01. Project Overview

Sri Lanka’s transport authorities are reviewing how to allocate limited resources to tackle traffic congestion in Colombo. They need to identify which road corridors experience the most severe congestion and where commuters may be losing the most time.

As a data analyst, my role in this project is to analyse historical traffic data, compare congestion and speed loss across corridors, and estimate the time cost of a 10 km vehicle trip. The findings aim to help decision-makers identify priority areas for further investigation and more informed traffic management planning.

## 02. Executive Summary

The analysis focuses on three questions:

Which selected corridors have the highest recorded congestion?

Where is the estimated additional travel-time cost greatest?

How do recorded morning and evening congestion levels differ?

## 03. Key Findings

Union Place / Ibbanwala Link: Recorded an average congestion index of 4.83, speed loss of 69.05%, and estimated time cost of approximately LKR 690 per 10 km vehicle trip. This corridor is a candidate for further congestion investigation.

T.B. Jayah Mawatha / Darley Road: Recorded an average congestion index of 5.00, speed loss of 60%, and estimated time cost of approximately LKR 600 per 10 km vehicle trip. Its high recorded congestion and estimated time cost make it another priority for investigation.

Morning vs evening congestion: Havelock/Pamankada recorded an evening-minus-morning congestion difference of approximately +1 index point. This suggests that commute-period differences should be considered when investigating traffic management needs.


These findings describe the available observations and modelled costs, not the entire Colombo road network.

## 3.1 Visual Insights

### 3.1.1 Corridor Cost Comparison

#### Business question: Which road corridors have the greatest estimated time cost for a 10 km vehicle trip?

<div align="center">
  <img width="1000px" src="images\Corridor Cost Comparison.PNG" />
</div>
<br>
The horizontal bar chart compares the estimated additional travel-time cost across selected corridors. The estimates are calculated from the difference between observed peak and off-peak travel times, multiplied by an assumed value of time of LKR 500 per hour.

#### What the analysis reveals

Union Place / Ibbanwala Link has an estimated average time cost of approximately LKR 690 per 10 km vehicle trip.

T.B. Jayah Mawatha / Darley Road follows at approximately LKR 600 per 10 km vehicle trip.

These results identify corridors where the difference between peak and off-peak travel times translates into a comparatively high modelled cost.

#### Why it matters

A corridor with a higher estimated time cost may warrant closer investigation because peak-period delays can impose a greater time burden on road users under the assumptions used in this model. Transport planners could validate these findings using updated travel-time surveys before deciding where to prioritise interventions.

#### How to interpret it

These values are illustrative estimates, not observed financial losses. They represent a 10 km vehicle trip under the project's assumptions and should not be multiplied into a citywide economic-loss estimate without reliable traffic volumes and additional supporting data.

### 3.1.2 Congestion and Speed Loss

Business question: Do corridors with higher congestion also tend to experience greater peak-period speed loss?

<div align="center">
  <img width="1000px" src="images\Congestion and Speed Loss 1.PNG" />
</div>
<br>

This visual compares the average recorded congestion index with the percentage reduction in peak speed relative to off-peak speed. It provides a complementary perspective to the cost chart by examining traffic conditions rather than their modelled monetary impact.

#### What the analysis reveals

Union Place / Ibbanwala Link combines a high average congestion index of 4.83 with a speed loss of approximately 69.05%.

T.B. Jayah Mawatha / Darley Road records an average congestion index of 5.00 and a speed loss of 60%.

Comparing both measures helps distinguish corridors that experience high recorded congestion and substantial speed reduction from corridors where the two indicators may tell a different story.

#### Why it matters

A congestion index alone does not fully describe how much slower traffic moves during peak periods. Reviewing it alongside speed loss provides additional evidence for screening corridors for further investigation.

#### How to interpret it

The visual describes an association between recorded measures; it does not establish that congestion causes a particular amount of speed loss. The historical dataset contains gaps and limited variation over time, so the results should not be presented as proof of a long-term relationship. Cotta Road / Rajagiriya is excluded from speed-loss comparisons because its recorded peak and off-peak speeds are identical.


### 3.1.3 Morning vs. Evening Congestion

**Business question:** Does recorded congestion differ between morning and evening commute periods across selected Colombo corridors?

<div align="center">
  <img width="1000px" src="images\Morning vs Evening Congestion.PNG" />
</div>
<br>

This chart compares the recorded business-hour morning and evening congestion indices for each corridor. Comparing the two periods helps identify where congestion levels are similar and where a larger difference may warrant further investigation.

**What the analysis reveals**

- **T.B. Jayah Mawatha (Darley Road)** records a congestion index of 5.00 in both the morning and evening periods, indicating similarly high recorded congestion.
- **Union Place / Ibbanwala Link** also records high congestion in both periods, with a morning index of 4.50 and an evening index of 5.00.
- **Havelock Road / Pamankada** records a morning index of 3.75 and an evening index of 4.75, a difference of one index point.
- Other corridors show different levels of congestion across the two periods, suggesting that commute patterns are not uniform across the selected road network.

**Why it matters**

Comparing commute periods provides more context than an overall corridor average alone. Corridors with consistently high congestion may require further investigation across both periods, while larger morning–evening differences can help guide more targeted traffic monitoring.

**How to interpret it**

The chart reflects the available historical observations and should not be treated as a universal pattern for every weekday or season. Differences do not establish their causes. Updated, consistently collected traffic data would be needed to validate these patterns before specific traffic-management changes are recommended.

### Overall Insight

Taken together, the visuals provide three complementary perspectives:

Estimated time cost helps compare the modelled commuter time burden across corridors.

Congestion and speed loss helps examine whether high recorded congestion coincides with substantial peak-period speed reduction.

Morning and evening differences helps identify corridors where the balance of congestion varies by commute period.

These findings provide a starting point for prioritising further investigation. They are not a substitute for current traffic surveys, verified road-segment coverage or a comprehensive economic assessment of congestion in Colombo.


[Download The Price of Congestion: Colombo ](dashboard\tableau dashboard\The_Price_of_Congestion_Colombo.twbx)

Screenshots:

<a href="dashboard\screenshots\Colombo Traffic Overview 1.PNG">
  <img src="Colombo Traffic Overview 1.PNG" alt="Colombo Traffic Overview">
</a>
<br>
<a href="dashboard\screenshots\Congestion Cost & Priority 1.PNG">
  <img src="Congestion Cost & Priority 1.PNG" alt="Congestion Cost & Priority">
</a>
<br>
<a href="dashboard\screenshots\WHERE CONGESTION COSTS THE MOST.PNG">
  <img src="WHERE CONGESTION COSTS THE MOST.PNG" alt="Commute Patterns & Context">
</a>


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

