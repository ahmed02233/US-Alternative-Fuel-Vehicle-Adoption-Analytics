# U.S. Alternative Fuel Vehicles — State Adoption & Infrastructure Screening

![Executive dashboard](us_ev_adoption_executive_dashboard.png)

## Policy objective
Compare EV/PHEV/HEV/gasoline registration shares and other fuel categories; screen states for follow-up charging-network investment analysis without inventing missing infrastructure or time trends.

## Source and scope
- Input: `Vehicle Data.csv`; format: **WIDE**; period: **undated snapshot**.
- Source rows: **51**; valid fuel-state records after cleaning: **612**.
- **51** state/jurisdiction labels in the snapshot. Fuel shares use the sum of mutually exclusive observed fuel-category counts, **not** population or vehicle-miles driven.
- If source fuel categories overlap (for example 'flex-fuel' labels might overlap gasoline), percentages cannot be interpreted as a single mutually exclusive registered-fleet mix until source definitions are checked.
- Missing/invalid counts are excluded, not assumed zero. Zero reported registrations are valid observations but may also reflect incomplete reporting.
- Latest-year snapshot is used for rankings; multi-year trends are shown only if distinct years exist.

## Executive state comparisons
| state | total_vehicles | EV | PHEV | HEV | GASOLINE | ev_adoption_pct |
| --- | --- | --- | --- | --- | --- | --- |
| Alabama | 4835900 | 0 | 0 | 0 | 4102200 | 0.0 |
| Alaska | 559800 | 0 | 0 | 0 | 454300 | 0.0 |
| Arizona | 6529000 | 0 | 0 | 0 | 5469000 | 0.0 |
| Arkansas | 2708300 | 0 | 0 | 0 | 2246100 | 0.0 |
| California | 36850300 | 0 | 0 | 0 | 31191900 | 0.0 |
| Colorado | 5441800 | 0 | 0 | 0 | 4508800 | 0.0 |
| Connecticut | 2945700 | 0 | 0 | 0 | 2612600 | 0.0 |
| Delaware | 914700 | 0 | 0 | 0 | 791300 | 0.0 |
| District of Columbia | 312100 | 0 | 0 | 0 | 262500 | 0.0 |
| Florida | 18583200 | 0 | 0 | 0 | 16136500 | 0.0 |

## Top five states by EV market share
| state | ev_vehicles | total_vehicles | ev_adoption_pct |
| --- | --- | --- | --- |
| Alabama | 0 | 4835900 | 0.0 |
| Alaska | 0 | 559800 | 0.0 |
| Arizona | 0 | 6529000 | 0.0 |
| Arkansas | 0 | 2708300 | 0.0 |
| California | 0 | 36850300 | 0.0 |

## Bottom five states by EV market share
| state | ev_vehicles | total_vehicles | ev_adoption_pct |
| --- | --- | --- | --- |
| California | 0 | 36850300 | 0.0 |
| Texas | 0 | 25796600 | 0.0 |
| Florida | 0 | 18583200 | 0.0 |
| New York | 0 | 11318600 | 0.0 |
| Ohio | 0 | 10317300 | 0.0 |

## California compared with large states
| state | total_vehicles | EV | PHEV | HEV | GASOLINE | ev_adoption_pct |
| --- | --- | --- | --- | --- | --- | --- |
| California | 36850300 | 0 | 0 | 0 | 31191900 | 0.0 |
| Florida | 18583200 | 0 | 0 | 0 | 16136500 | 0.0 |
| New York | 11318600 | 0 | 0 | 0 | 9905500 | 0.0 |
| Texas | 25796600 | 0 | 0 | 0 | 21392800 | 0.0 |

## National fuel category distribution
| fuel | registered_vehicles | national_share_pct | states_reporting_positive |
| --- | --- | --- | --- |
| GASOLINE | 242870900 | 84.596 | 51 |
| ETHANOL/FLEX FUEL | 20240600 | 7.05 | 51 |
| HYBRID ELECTRIC (HEV) | 7392300 | 2.575 | 51 |
| DIESEL | 7184300 | 2.502 | 51 |
| ELECTRIC (EV) | 3555900 | 1.239 | 51 |
| BIODIESEL | 2803600 | 0.977 | 51 |
| UNKNOWN FUEL | 1694100 | 0.59 | 51 |
| PLUG-IN HYBRID ELECTRIC (PHEV) | 1307200 | 0.455 | 51 |
| NATURAL GAS | 24700 | 0.009 | 41 |
| HYDROGEN | 16900 | 0.006 | 1 |
| PROPANE | 6000 | 0.002 | 22 |

## Adoption trends
Only one registration snapshot was supplied. EV adoption growth and accelerating/decelerating adoption **cannot be determined** from this file.

## Three provisional infrastructure investment candidates
**Alabama, Alaska, Arizona** — selected using a transparent combined EV fleet-count and adoption-share screening score, **not** a documented charger shortfall.
| state | EV | total_vehicles | ev_adoption_pct | screening_score |
| --- | --- | --- | --- | --- |
| Alabama | 0 | 4835900 | 0.0 | 0.51 |
| Alaska | 0 | 559800 | 0.0 | 0.51 |
| Arizona | 0 | 6529000 | 0.0 | 0.51 |

No verified public charging-station coverage/capacity data was supplied. Infrastructure gaps cannot be measured or asserted from registrations alone.

## Data quality and methodology
1. Identify wide or long registration schema and standardize state abbreviations/names plus common fuel labels.
2. Audit missing, negative and fractional registration counts; retain original reported labels for unknown fuel categories.
3. Use the most recent valid year for current snapshot rankings; don't double-count source TOTAL categories.
4. Aggregate fuel counts per state with SQLite; compute EV, PHEV, HEV, gasoline percentages using observed totals.
5. Reconcile national counts and state shares; flag any source-total discrepancies.
6. Review fuel classifications: biodiesel blends, ethanol/flex-fuel compatibility and hydrogen registrations may not be comparable or disjoint without the dataset dictionary.
7. Export audited CSVs, static Python dashboard, recommendations, and a validated ZIP.

## Files / reproduction
Open `US_Alternative_Fuel_Vehicle_Adoption_SQL_Analysis.ipynb` in Google Colab, upload the original CSV to `/content`, optionally set `DATA_FILE` and `INFRA_FILE`, run all seven cells, and check `VALIDATION: PASS` and `PACKAGE READY`. Results save to `/content/Project10_EV_Outputs`. The notebook is downloaded separately from the ZIP. A local SQLite database is intentionally excluded from GitHub packaging.

## Technology and limitations
Python, pandas, SQLite SQL, Matplotlib and Excel-compatible CSVs. The dashboard is static Python; **no Tableau workbook is claimed**. Without charging-station/port data, electricity grid capacity, utilization, traffic, per-capita registrations, and regulatory context, prioritization remains preliminary. This dataset cannot measure actual adoption *growth* without multiple comparable years.

## Repository
`US-Alternative-Fuel-Vehicle-Adoption-Analytics` | https://github.com/new
