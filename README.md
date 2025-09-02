# Greater Sydney "Bustling Index"

## Overview  
This project was developed as part of **DATA2x01: Data Science, Big Data & Data Variety** at the University of Sydney.  
The task was to create a **“Bustling Index”** that quantifies how busy different Statistical Area Level 2 (SA2) regions in Greater Sydney are, based on integrated demographic, business, transport, and social datasets.  

This was a **group project (3 members)**.  
- **My contribution:**  
  - **Task 1:** Imported and cleaned multiple datasets into PostgreSQL/PostGIS with a consistent schema.  
  - **Task 2:** Designed and implemented the core **Bustling Index formula** (z-scores + sigmoid), combining businesses, public transport stops, polling places, and school catchments.  

---

## Objectives  
1. **Data Integration**  
   - Load spatial & tabular datasets (ABS, Transport for NSW, AEC, NSW DoE).  
   - Clean and transform into a unified PostgreSQL schema with PostGIS.  

2. **Bustling Index Calculation**  
   - Standardize indicators using z-scores.  
   - Apply sigmoid function to combine metrics.  
   - Ensure per-capita adjustments for fairness across SA2 regions.  

3. **Extensions (Group work)**  
   - Each member contributed an additional dataset to enrich the index.  
   - Final index correlated with **median income** to test economic alignment.  
   - Results visualized using maps and summary tables.  

---

## Tech Stack  
- **Languages:** Python, SQL  
- **Database:** PostgreSQL with PostGIS  
- **Libraries:** `pandas`, `geopandas`, `psycopg2`, `matplotlib`  
- **Data Sources:**  
  - [ABS SA2 Digital Boundaries](https://www.abs.gov.au/statistics/standards/australian-statistical-geography-standard-asgs-edition-3/jul2021-jun2026/access-and-downloads/digital-boundary-files/SA2_2021_AUST_SHP_GDA2020.zip)  
  - [ABS Business Counts](https://www.abs.gov.au/statistics/economy/business-indicators/counts-australian-businesses-including-entries-and-exits/latest-release#data-downloads)  
  - [Transport for NSW GTFS data](https://opendata.transport.nsw.gov.au/dataset/timetables-complete-gtfs)  
  - [AEC Polling Places 2019](https://data.aurin.org.au/dataset/au-govt-aec-aec-federal-election-polling-places-2019-na)  
  - [NSW School Catchments](https://data.cese.nsw.gov.au/data/dataset/school-intake-zones-catchment-areas-for-nsw-government-schools)  

---

## Repository Structure  
- [Lab-16_Group1.html](https://github.com/yun-522/Greater-Sydney-Analysis-Assignment-DATA2001/blob/2e556d5193f23998814c292bd87e27c066d3fc04/code.pdf)   # Code + analysis (Jupyter Notebook HTML export)  
- README.md   # Project description  

---

## Key Results  
- Successfully integrated **350+ SA2 regions** into PostgreSQL/PostGIS.  
- Computed **Bustling Index scores** for all Greater Sydney SA2s.  
- Found **positive correlation with median income**: more bustling regions tended to be higher income.  
- Visualization maps highlighted hotspots around **CBD, Parramatta, and major transport corridors**.  

---

## Insights  
- **Public transport stops** were the strongest driver of “bustling” scores.  
- **Businesses per capita** balanced high-density vs suburban regions.  
- **School catchments and polling places** ensured a social/community dimension.  
- Demonstrated how **data integration + spatial analytics** can produce interpretable urban metrics for policy and planning.  
