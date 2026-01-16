## API Assignment 
# Multimodal Data Reveal Climatic Connections to Stehekin, WA Debris Flows in December 2025

## Overview

In December 2025, a sequence of atmospheric river events delivered intense rainfall to the North Cascades of Washington State. These storms coincided with widespread debris flows in and around **Stehekin, Washington**, a community that has experienced extensive wildfire activity in recent years. Post-fire landscapes are especially vulnerable to debris flows because the loss of vegetation and root systems reduces soil cohesion and slope stability.

Debris flow initiation is strongly controlled by **soil moisture**, which is governed by two competing processes:

- **Flux into the system** (precipitation)
- **Flux out of the system** (hydrologic drainage)

While direct measurements of soil moisture are limited in steep alpine terrain, precipitation records and river discharge data together provide a physically consistent proxy for basin-scale soil saturation. When combined with seismic observations, these datasets form a coherent narrative explaining debris flow timing in Stehekin during December 2025.

---

## Multimodal Data Sources

This analysis integrates three independent datasets:

1. **Precipitation** from NOAA daily climate records
2. **Stream discharge and stage** from USGS stream gauges
3. **Seismic waveforms** from the UW PNSN network (IRIS)

All datasets are accessed programmatically via public APIs and visualized in the accompanying Jupyter Notebook.

---

## NOAA Precipitation Data

Daily precipitation data for the Stehekin region show multiple rainfall maxima during December 2025. Two sustained periods of elevated precipitation occur:

- **December 9–13**
- **December 16**

These rainfall events represent substantial **inputs to the soil moisture system**. However, precipitation alone does not determine debris flow triggering because it provides no information about how efficiently water is drained from the basin.

**Figure 1.**  
*Daily precipitation totals for Stehekin, WA during December 2025. Two precipitation maxima occur between December 9–13 and on December 16, indicating sustained atmospheric river influence.*

---

## USGS Stream Gauge Data

Hydrologic response is quantified using daily stream gauge data from the Stehekin River. This analysis explicitly uses the following uploaded datasets:

- **Discharge:**  
  `usgs_12451000_iv_discharge_2025-12-10_to_2025-12-16.csv`

- **Stage (river height):**  
  `usgs_12451000_iv_stage_2025-12-10_to_2025-12-16.csv`

The discharge record shows a clear monthly maximum on **December 11, 2025**, reaching approximately **14,000 cubic feet per second**. Stream discharge integrates both rainfall input and subsurface drainage, making it an effective proxy for **watershed-scale soil moisture conditions**.

The accompanying stage data show a concurrent rise in river height, confirming a basin-wide hydrologic response rather than localized runoff.

**Figure 2.**  
*USGS Stehekin River daily discharge (cubic feet per second) from December 10–16, 2025, derived from `usgs_12451000_iv_discharge_2025-12-10_to_2025-12-16.csv`. Peak discharge occurs on December 11, coincident with sustained antecedent rainfall.*

---

## PNSN Seismic Data

Seismic observations provide independent evidence of debris flow activity. Data from the UW.DREAM three-component seismometer station in Stehekin reveal long-period seismic signals characteristic of debris flows.

These signals initiate on **December 11**, coincident with the peak in stream discharge, and persist throughout the day with additional intermittent signals over the following days. Importantly, debris flows begin **after several consecutive days of heavy rainfall**, indicating a critically oversaturated soil column in a post-fire landscape.

**Figure 3.**  
*Three-component seismic waveform data from the UW.DREAM station in Stehekin, WA show long-period debris flow signals initiating on December 11, 2025, coincident with peak river discharge.*

---

## Synthesis and Interpretation

The combined datasets define a clear sequence of physical processes:

1. Prolonged atmospheric river rainfall increased basin-wide soil moisture.
2. River discharge peaked as soils reached full saturation and drainage capacity was exceeded.
3. Debris flows initiated at the time of maximum discharge in a destabilized post-fire landscape.

This multimodal agreement demonstrates that **antecedent hydrologic conditions**, not just instantaneous rainfall intensity, control debris flow hazards in mountainous terrain.

---

## Data Accessibility and Reproducibility

All datasets used in this analysis are freely available and accessed via public APIs:

- **NOAA:** Daily precipitation records for Stehekin, WA  
- **USGS:** Stehekin River discharge and stage data (Station 12451000)  
- **IRIS / PNSN:** Seismic waveform data from the UW.DREAM station  

The USGS hydrologic data used directly in this analysis are archived locally as:

- `usgs_12451000_iv_discharge_2025-12-10_to_2025-12-16.csv`
- `usgs_12451000_iv_stage_2025-12-10_to_2025-12-16.csv`

This workflow enables fully reproducible analysis and visualization within the accompanying Jupyter Notebook.
