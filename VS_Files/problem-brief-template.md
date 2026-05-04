# Problem Brief — Urban Heat Risk Mapping for Manhattan

---

## The Environmental Question

How has land surface temperature (LST) changed across Manhattan during peak summer periods over the past decade, and which neighbourhood-scale zones currently exhibit the highest heat exposure risk based on these patterns?

---

## The Design Decision This Supports

A climate resilience analyst at a New York City municipal agency (e.g., Department of City Planning or Mayor’s Office of Climate & Environmental Justice) must decide which 5–10 neighbourhood zones in Manhattan should be prioritised for near-term heat mitigation interventions such as tree planting, shading infrastructure, or surface material changes.

This project supports targeted allocation of limited public resources by identifying spatially explicit heat exposure hotspots, enabling prioritised and defensible intervention planning instead of uniform city-wide strategies.

---

## The Intended User

A capital planning or climate resilience analyst working within a New York City municipal agency.

* Works with GIS-based spatial datasets and urban policy frameworks
* Tasked with recommending where limited intervention budgets should be allocated
* Needs outputs that are spatially explicit, interpretable, and defensible
* Must communicate decisions to non-technical stakeholders such as policymakers and community boards

**Moment of use:**
Tuesday morning, preparing a shortlist of priority zones for inclusion in a seasonal or annual heat mitigation plan.

---

## Measurable Success Criteria

1. The full pipeline (data loading → processing → output) runs from the repository on a new machine in under 10 minutes using clearly documented steps

2. Land Surface Temperature (LST) maps are generated for Manhattan at ≤100m spatial resolution for at least three distinct summer time points (historical comparison)

3. The system produces a shortlist of 5–10 neighbourhood-scale zones with the highest relative heat exposure during peak summer conditions

4. At least one validation comparison is performed using an external dataset (e.g., NYC Heat Vulnerability Index or equivalent proxy), with agreement or discrepancy explicitly documented

5. The final output (map or dashboard) clearly distinguishes high-risk vs low-risk zones and includes a transparent explanation of limitations and uncertainty

6. The classification logic (rule-based or threshold-based) used to identify high-risk zones is documented in plain language and understandable to a non-technical stakeholder

---

## Risks and Open Questions

### Risks

* **Proxy limitation:**
  LST represents surface heat and not full human thermal comfort; factors such as humidity, wind, and shading are not directly captured

* **Spatial resolution limits:**
  Satellite-derived LST (~30–100m) may not capture fine-grained urban variations such as street-level shading or material differences

* **Temporal inconsistency:**
  Satellite data availability is affected by revisit cycles and cloud cover, potentially limiting consistent multi-year comparison

* **Data integration mismatch:**
  External datasets (e.g., heat vulnerability indices) may differ in spatial resolution, temporal coverage, or methodology

* **Projection uncertainty:**
  Any forward-looking assessment based on historical trends will be indicative, not predictive

* **Validation limitations:**
  Limited availability of high-resolution ground-truth data for confirming hotspot accuracy

---

### Open Questions

* What is the most appropriate spatial unit for defining “neighbourhood-scale zones” (grid, census tract, or custom aggregation)?
* What threshold or method should define “high-risk” heat exposure (absolute vs relative ranking)?
* Which additional variables (e.g., vegetation, land cover) are necessary to explain or contextualise observed heat patterns?

---

## Out of Scope

* Indoor or building-level thermal comfort analysis
* High-resolution microclimate or CFD-based simulations
* Real-time or live environmental monitoring systems
* Full human thermal comfort modelling (including humidity, wind, radiation balance)
* Long-term climate forecasting using advanced predictive models
* Geographic scope beyond Manhattan

---

## Team

| Name                        | Role on this project |
| --------------------------- | -------------------- |
| Dhruvil Mahendra Bhanushali | Data Lead            |
| Jinesh Narendra Jain        | Visualization Lead   |
| Rudra Mhatre                | Documentation Lead   |
| Sumit Sudhir Shingne        | Domain Research Lead |

---

**This document defines the purpose and scope of the project. All subsequent artifacts (data inventory, decision map, system design, and output) must align with this brief.**
