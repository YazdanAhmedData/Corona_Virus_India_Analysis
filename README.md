# 🦠 COVID-19 India Analysis | Tableau Public-Health Dashboard

<img width="100%" alt="COVID-19 India dashboard screenshot" src="https://github.com/user-attachments/assets/26069883-0592-4fdd-8749-eb78b21cd80d" />

**Portfolio case study · Public-health data · Geographic analytics · Tableau**

## Executive Summary
This project combines Indian COVID-19 case records with testing, vaccination, demographic and state-boundary data to explore how reported public-health indicators varied over time and geography. Tableau is used to bring multiple datasets into a visual analysis workflow.

## Business Problem
Public-health datasets are spread across sources and often use different date ranges, definitions and geographic labels. A dashboard can make those differences easier to inspect and help a viewer explore reported case trends, testing activity and vaccination coverage without treating raw counts as the whole story.

This is a historical descriptive analysis, not medical advice or a causal study.

## Data Sources
| File | Role |
|---|---|
| `covid_19_india.csv` | Case, recovery and death reporting by date/state |
| `covid_vaccine_statewise.csv` | State-wise vaccination information |
| `ICMRTestingLabs.csv` | Testing-related information |
| `AgeGroupDetails.csv` | Age-group breakdown |
| `IndividualDetails.csv` | Individual-level records in the source collection |
| `India_State_Boundary.*` | Geographic boundaries for maps |
| `Corona Dashboard.twb` | Tableau workbook |
| `Corona-dashboard_glimpse.pdf` | Dashboard preview |

## Business / Public-Health Questions
- How did reported cases, recoveries and deaths change over the available timeline?
- How did testing and vaccination measures vary across states?
- Which geographic patterns appear in the mapped data?
- What context do age-group breakdowns add to aggregate totals?
- Which comparisons require population denominators or more consistent date coverage?

## KPI Framework
| KPI | Definition | Interpretation caution |
|---|---|---|
| Confirmed cases | Reported cumulative or daily cases, depending on source field | Distinguish cumulative counts from new cases |
| Recoveries | Reported recovered cases | Confirm whether source values are cumulative |
| Deaths | Reported deaths | Reporting definitions and dates may vary |
| Recovery / case ratio | Recoveries ÷ confirmed cases, for a consistent date and definition | Not a clinical recovery probability |
| Death / case ratio | Deaths ÷ confirmed cases, with matched reporting date | Not a causal or individual risk estimate |
| Testing activity | Reported tests or testing indicators | Confirm units and coverage |
| Vaccination coverage | Vaccination count or coverage rate as defined by source | State whether doses or people are counted |
| State comparison | Comparable rate with appropriate population denominator where available | Raw totals favour larger populations |

## Insights & Decision Use
- **Trend interpretation:** use date-aligned measures to distinguish changes in reported cumulative totals from changes in daily activity.
- **Geographic comparisons:** prefer rates and clearly defined denominators over raw counts when comparing states of different sizes.
- **Vaccination and testing context:** interpret changes alongside the source's reporting period and coverage; do not infer that one measure caused another.
- **Data integration:** investigate unmatched state names, date gaps, and differences in source definitions before presenting cross-source conclusions.

These are responsible interpretation principles for the displayed analysis. Add specific numerical findings only after verifying the selected date, source field and denominator.

## Technical Workflow
1. Review each source's grain, date range, field definitions and missing values.
2. Standardise date and state/UT fields where needed.
3. Connect the datasets and geographic boundary files in Tableau.
4. Build time-series, state comparison, demographic and map views.
5. Validate filters, joins and geographic mappings against the source records.

## Tools & Skills
Tableau · CSV data preparation · Geographic visualisation · Multi-source analysis · KPI interpretation · Public-health reporting · Data-quality awareness

## Reproduce / Review
1. Open `Corona Dashboard.twb` in Tableau Desktop.
2. Update local source paths for CSV and shapefile components if needed.
3. Review `Corona-dashboard_glimpse.pdf` and the screenshot above.
4. Validate joins, date filters, cumulative/daily fields and state mapping before using the results.

## Ethics & Limitations
- Individual-level public-health data should be handled carefully; do not republish identifying information.
- COVID reporting definitions, completeness and time coverage vary by source.
- Correlation and geographic co-occurrence do not prove causation.
- State-level raw counts should not be compared as risk without appropriate population denominators.
- This is a historical data-analysis project, not current epidemiological guidance.

## Next Steps
- Add a data dictionary and source dates.
- Report three to five verified findings with exact date range and denominators.
- Add a refresh/cleaning process and tests for duplicate state-date records.
- Include a methodology note describing any joins and calculated fields.

## Author
**Yazdan Ahmed** · [GitHub Portfolio](https://github.com/YazdanAhmedData)
