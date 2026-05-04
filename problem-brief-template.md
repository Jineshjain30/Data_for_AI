# Problem Brief — [Your Project Name]

> Copy this file into your team's repo as `docs/problem-brief.md`.
> Fill in every section. One page total. Plain English. Today.
>
> This is your project's **purpose document.** Every other deliverable
> in the seminar references this. Get it right and the rest gets easier.

---

## The Environmental Question

*One or two sentences. What environmental or ecosystem-related question
are you answering with data?*

> Example: *How fast is Barceloneta beach eroding, and which seafront
> buildings will be most exposed to wave action and storm surge by 2031?*

**Your question:**

How is land surface temperature (as a proxy for urban heat island intensity) changing across Manhattan, and which neighbourhood-scale zones are projected to experience critical outdoor thermal discomfort during peak summer conditions?

---

## The Design Decision This Supports

*A real decision someone will make, more confidently because of your
project. Not "raise awareness." A specific, near-term action.*

> Example: *The Barcelona Urban Resilience Office is preparing the 2026–2030
> capital plan. They need to decide which seafront buildings get priority
> funding for adaptation works.*

**Your decision:**

Urban planners and municipal agencies (e.g., NYC Department of City Planning or Department of Parks & Recreation) need to decide which neighbourhood zones in Manhattan should be prioritised for heat mitigation interventions such as tree planting, shading structures, or surface material changes.

This tool supports early-stage planning and resource allocation decisions by identifying high-risk thermal discomfort zones during peak summer conditions, enabling targeted and evidence-based interventions rather than uniform city-wide strategies.

---

## The Intended User

*Who is the person reading your output? What's their role? What do they
already know? What do they not know?*

> Example: *Capital planning analyst at the Barcelona Urban Resilience
> Office. Familiar with GIS and municipal data. Not a coastal engineer.
> Needs an output they can defend in front of district councilors.*

**Your user:**

A capital planning or climate resilience analyst within a New York City municipal agency (e.g., Department of City Planning or Mayor’s Office of Climate & Environmental Justice).

- Works with GIS-based spatial data and policy frameworks
- Responsible for recommending where limited urban intervention budgets should be allocated
- Needs outputs that are interpretable, spatially explicit, and uncertainty-aware
- Must justify decisions to non-technical stakeholders such as policymakers and community boards
---

## Measurable Success Criteria

*3–5 things that, if true at the end, mean the project worked. Each one
must be checkable. "Useful" is not checkable; "<10 buildings on the
shortlist" is.*

> Example:
> 1. Reproducible from the repo by a non-author in <10 minutes
> 2. 2031 coastline projection within ±2 m of an external validation
> 3. Tier 1 shortlist of <10 buildings, includes the 3 already flagged by engineers
> 4. Model card and failure gallery clear enough that a councilor can
>    state what the system can and cannot do

**Your criteria:**

1. The full pipeline (data loading → processing → output) runs from the repository on a new machine in under 10 minutes using documented steps
2. Land Surface Temperature (LST) maps are generated for Manhattan with spatial resolution ≤ 100m and at least 3 different time points (historical comparison)
3. The system identifies and outputs a shortlist of 5–10 high-risk neighbourhood zones based on peak summer thermal discomfort thresholds
4. At least one validation comparison is performed using an external dataset or known heat-vulnerable areas (e.g., NYC heat vulnerability index or similar proxy)
5. The final output (map/dashboard) clearly distinguishes:
-high-risk vs low-risk zones
-includes a stated limitation and uncertainty explanation.
6. The model or rule-based method used to classify thermal discomfort is documented and explained such that a non-technical user can understand its logic and limitations

---

## Risks and Open Questions

*What could make this project fail? What do you not know yet that you
need to learn?*

**Risks:**

- Spatial resolution limitations:
Satellite-derived Land Surface Temperature (LST) data (e.g., Landsat) has moderate resolution (~30–100m), which may not capture fine-grained urban variations, leading to oversimplified neighbourhood-level results
- Proxy mismatch (LST vs thermal comfort):
LST represents surface heat, not actual human thermal comfort. Important factors such as humidity, wind, and shading are not fully captured, which may lead to misleading interpretations
- Data integration inconsistency:
Combining satellite data with NYC datasets (e.g., Heat Vulnerability Index) may introduce inconsistencies in spatial scale, time period, and measurement methodology
- Temporal gaps and seasonality:
Satellite data availability depends on acquisition dates and cloud cover, potentially limiting consistent comparison across time and affecting trend analysis
- Projection uncertainty:
The use of simple trend-based projections (instead of robust predictive models) may oversimplify future conditions and produce unreliable estimates for 2030
- Validation constraints:
Limited access to ground-truth or high-resolution validation data for confirming identified high-risk zones

**Open questions for next session:**

- [ ... ]
- [ ... ]

---

## Out of Scope

*What are you NOT doing? Be explicit. This protects you from scope creep.*

- Building-level or indoor thermal comfort analysis
The project does not evaluate indoor conditions or individual building performance, as the data used (satellite LST) is not suitable for that scale
- High-resolution physical simulation of urban climate
The project does not include CFD simulations or detailed microclimate modelling (e.g., airflow, radiation balance)
- Advanced predictive modelling
The project does not implement complex machine learning or long-term climate forecasting; projections are limited to simple trend-based estimations
- Real-time or live data integration
The system does not process real-time sensor data or continuously update environmental conditions
- Complete representation of human thermal comfort
The analysis does not fully account for factors such as humidity, wind speed, or urban geometry, and relies primarily on temperature-based proxies
- Geographic scope beyond Manhattan
The analysis is limited to Manhattan and does not extend to other boroughs or cities

---

## Team

| Name | Role on this project |
|---|---|
| Dhruvil_Mahendra_Bhanushali | [ data lead] |
| Jinesh_Narendra_Jain | [ visualization lead] |
| Rudra_Mhatre | [documentation lead] |
| Sumit_Sudhir_Shingne | [ domain research lead] |

> Roles are loose — they help you divide work, not lock you in. Everyone
> reads everyone's code. Everyone defends every line.
