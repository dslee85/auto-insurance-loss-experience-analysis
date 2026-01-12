# Auto Insurance Loss Experience Analysis

## Objective
Analyze auto insurance loss experience using policy- and claim-level data to evaluate
claim severity patterns across driver segments.

---

## Data Overview
- Policy and claim data derived from an observed-claims dataset
- Each record represents a reported auto insurance claim
- Annual premium is used as a proxy for earned premium due to data limitations

---

## Methodology
- Restructured flat claims data into relational policy and claims tables using SQL
- Joined datasets on policy number
- Segmented drivers into age bands for comparative analysis
- Calculated claim severity as average claim amount per reported claim

---

## Key Results

### Claim Severity by Driver Age Band
- Claim severity is highest among younger drivers (under age 25)
- Severity declines for drivers ages 25–34
- Severity increases modestly for drivers ages 35–64
- The 65+ age band exhibits lower observed severity; however, results are based on a very small claim count and are not considered credible


### Claim Severity by State
- Indiana (IN): Average severity ≈ $53,022
- Illinois (IL): Average severity ≈ $52,872
- Ohio (OH): Average severity ≈ $52,478
- Severity levels are broadly consistent across analyzed states, with relatively low variance

### Claim Severity by Incident Type
- Single-vehicle collisions exhibit higher average claim severity than multi-vehicle collisions
- Multi-vehicle incidents show lower average severity despite higher claim frequency
- Results suggest that claim severity is not solely driven by the number of vehicles involved

---

## Interpretation

### Driver Age Effects
- Higher severity among younger drivers may reflect riskier driving behavior and higher-impact loss events
- Lower severity among drivers ages 25–34 may reflect more stable driving patterns
- The apparent decrease in severity for drivers age 65+ is based on limited observations and should not be interpreted as a true underlying risk difference
- Claim count volume is an important consideration when evaluating the credibility of segment-level results
- Observed patterns represent correlation and were not tested for causality

### State-Level Effects
- Claim severity shows limited variation across states in the observed dataset
- Similar severity levels may reflect comparable coverage limits, repair costs, or claim handling practices across states
- Limited geographic differentiation may also be driven by dataset composition and the absence of exposure weighting
- Observed patterns represent correlation and were not tested for causality

### Incident Type Effects
- Higher severity for single-vehicle collisions may reflect higher-impact events such as loss-of-control accidents and collisions with fixed objects
- Multi-vehicle incidents may include a higher proportion of low-speed or minor collisions, reducing average severity
- In multi-vehicle incidents, losses may be distributed across multiple parties, lowering per-claim reported severity
- Observed results highlight the importance of understanding claim composition when interpreting severity metrics

---

## Future Enhancemennts
- Incorporate exposure-based frequency metrics
- Adjust severity for policy limits and vehicle value
- Expand geographic analysis using additional state-level variables


---
## Assumptions & Limitations
- Dataset includes only observed claims and excludes exposure-only policies
- Claim frequency metrics are conditional on reported claims
- Annual premium assumed to be fully earned
- Vehicle value and coverage limits were not directly modeled

---

## Tools Used
- SQL (SQLite) for data modeling and aggregation
- Excel for data validation and reconciliation
- R for exploratory data analysis and visualization
