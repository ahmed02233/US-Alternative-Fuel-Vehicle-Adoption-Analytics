# U.S. Alternative Fuel Vehicles — Transportation Policy Recommendations

## Interpretation standard
Vehicle registrations measure recorded fleet stock—not new purchases, charging access, infrastructure shortage, charging utilization, or causal policy outcomes.

## 1. Screen three states for infrastructure feasibility (HIGH)
**Candidates:** California, Washington, New Jersey. **Evidence:** latest EV market-share and absolute EV-stock screening in `us_ev_three_priority_state_candidates.csv`. **Action:** collect and validate charger locations, number of ports, uptime, utilization, housing types, corridor traffic and underserved community access before siting new investments. **KPI:** operational public ports per 1,000 EVs, wait time and access within a travel-time threshold. **Caveat:** no charger gap is established from registrations alone.

## 2. Prioritize verified underserved charging areas (CRITICAL)
**Action:** overlay geocoded charger locations, household income, apartment occupancy and trips with EV registration concentration. **KPI:** geographic coverage and reliable fast-charge availability. Avoid assuming state-level registration share reveals local access gaps.

## 3. Plan separately for EVs and PHEVs (HIGH)
**Action:** distinguish battery-electric fast-charging needs from plug-in hybrid mixed-fuel behavior. **KPI:** charger demand per plug-in vehicle by connection type, measured utilization.

## 4. Benchmark lagging states with comparable denominators (MEDIUM)
**Evidence:** five lowest shares appear in `us_ev_bottom5_ev_states.csv`. **Action:** check data completeness, income, travel needs and vehicle mix before considering policy incentives. **KPI:** annual change in EV share after matching comparable registration periods.

## 5. Evaluate hybrid and gasoline transition pathways (HIGH)
**Action:** use `us_ev_state_fuel_market_shares.csv` to identify high conventional-fleet states and develop grid-capacity and dealer-readiness scenarios. **KPI:** EV registrations as a share of replacements and grid upgrades completed.

## 6. Classify non-electric alternative fuels correctly (MEDIUM)
**Action:** separately track biodiesel blends, ethanol flex-fuel capability and hydrogen fuel-cell registrations using source definitions. **KPI:** verified distinct registrations, fueling availability, and fleet use cases; avoid treating overlapping fuel labels as disjoint.

## 7. Publish a multi-year data and infrastructure scorecard (CRITICAL)
**Action:** collect comparable years, source denominators, public charging stations/ports, and data refresh dates. **KPI:** missingness, reconciliation error, adoption share by year and charger uptime; publish assumptions and exclusions.

## Decision
Treat the three selected states as **follow-up study candidates**, not evidence of a verified charger shortage. Confirm with charging infrastructure and traffic data before authorizing capital expenditures.
