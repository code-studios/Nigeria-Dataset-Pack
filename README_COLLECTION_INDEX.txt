====================================================================
  NIGERIA DATASET COLLECTION
  README & COLLECTION INDEX
  Compiled by : Eni Solomon Laughter — Chang'an University
  Research lab: TRAMSYS LAB
  Date        : 2026-03-18  13:12:02
====================================================================

ABOUT THIS COLLECTION
  This folder contains all datasets assembled and produced
  for a K-means based research study on transport planning
  and railway station optimization in Nigeria. The datasets
  span socioeconomic indicators, demographic data, geographic
  coordinates, transport infrastructure metrics, and full
  optimization results and visualizations.

  The collection is organized into 9 top-level folders.
  Each folder contains the dataset file(s) and a companion
  description .txt file explaining the dataset content,
  schema, source, generation method, and intended use.

  For any dataset where the source is unconfirmed or values
  are estimated/synthetic, see PROVENANCE_NOTES.txt in this
  same directory.

--------------------------------------------------------------------
  FOLDER STRUCTURE & CONTENTS
--------------------------------------------------------------------

  01  Nigeria State Unemployment Rate
  ··················································
  File : nigeria_state_unemployment_rate.json
  What : State-level unemployment rate (%) for all 36
         Nigerian states + FCT.
  Use  : Socioeconomic feature for clustering and
         transport demand modelling.
  Rows : 37 state records

  02  Nigeria State Sociodemographic and Transport Indicators
  ··················································
  File : nigeria_state_sociodemographic_transport_indicators.json
  What : Four state-level indicators — rural residence %,
         disability prevalence %, ethnic diversity index,
         and road condition index — for all 37 units.
  Use  : Multi-dimensional socioeconomic clustering input.
  Rows : 37 state records

  03  Nigeria City Coordinates
  ··················································
  File : nigeria_city_coordinates.json
  What : Geographic centroid coordinates (WGS84 lat/lon)
         for 37 major Nigerian cities, one per state + FCT.
  Use  : Spatial reference layer for clustering maps,
         distance calculations, and GIS work.
  Rows : 37 city records

  04  Nigeria State Dependency Ratio
  ··················································
  File : nigeria_state_dependency_ratio.json
  What : State-level dependency ratio (dependants per
         working-age person) from NLSS 2018/2019.
  Use  : Labour market and welfare indicator for
         socioeconomic clustering.
  Rows : 37 state records

  05  Nigeria Cities Data
  ··················································
  Files: nigeria_cities_data.xlsx (36 sheets + Summary)
         state_json_files/ (35 individual state JSONs)
  What : Settlement-level inventory of cities, towns, and
         localities across 35 Nigerian states + FCT.
         Fields: name, type, region, country, lat, lon,
         elevation (ft), population estimate.
  Use  : Spatial base layer, population-weighted analysis,
         transport accessibility modelling.
  Rows : ~28,874 settlement records across 35 states

  06  Nigeria LGA Population and Socioeconomic Indicators
  ··················································
  File : nigeria_lga_population_socioeconomic_indicators.csv
  What : LGA-level panel dataset (2010–2024) for 5 states
         (Lagos, Rivers, Enugu, Kano, Kaduna) with 25
         demographic, economic, and social variables.
  Use  : Longitudinal LGA analysis, clustering, transport
         demand modelling.
  Rows : 200 LGA-year records

  07  Nigeria LGA Population by State
  ··················································
  Files: nigeria_lga_population_by_state.xlsx
         (sheets: All LGAs + State Summary)
         nigeria_lga_population_by_state_original_wide_format.xlsx
  What : LGA-level population figures for all 36 states
         + FCT (36 states, ~774 LGAs). Reshaped from
         original wide side-by-side Excel format.
  Use  : Population-weighted spatial analysis, LGA
         clustering, administrative reference.
  Note : Bauchi state data absent from source file.

  08  Nigeria Inter-City Travel and Traffic Data
  ··················································
  File : nigeria_intercity_travel_traffic_data.csv
  What : OD travel records between 9 Nigerian cities with
         road distance, speed, congestion level, travel
         time, weather, alternative routes, and suitability
         score. 896 records across 72 unique OD pairs.
  Use  : Inter-city route analysis, traffic pattern
         modelling, transport network assessment.
  Rows : 896 OD trip records

  09  Railway Station Optimization Results
  ··················································
  Sub-folders: 11 thematic groups (01–11)
  What : Complete dataset collection from the K-means
         railway station optimization study — all input
         features, distance/demand matrices, optimization
         results, service designs, and visualizations.
         See README_DATASET_INDEX.txt inside this folder
         for the full 11-group breakdown.
  Files: 49 datasets across 11 groups

--------------------------------------------------------------------
  QUICK REFERENCE: DATASET FORMATS
--------------------------------------------------------------------

  Format       Folders
  ········································
  JSON         01, 02, 03, 04, parts of 05, 09
  CSV          06, 08, parts of 05, 09
  XLSX         05 (consolidated), 07
  PNG          09 (Group 11 visualizations)

--------------------------------------------------------------------
  COORDINATE SYSTEM
--------------------------------------------------------------------
  All geographic coordinates use WGS84 decimal degrees.
  Longitude range: ~3°E – 15°E
  Latitude range : ~4°N – 14°N

--------------------------------------------------------------------
  COVERAGE NOTES
--------------------------------------------------------------------
  • All datasets target 36 Nigerian states + FCT (37 units)
    unless otherwise noted in the description file.
  • Datasets 05 and 07 are missing Kwara and/or Bauchi
    due to gaps in source data — see description files.
  • Dataset 06 covers only 5 states (not nationally
    representative) — see description file.
  • Dataset 08 covers only 9 cities — likely synthetic.

--------------------------------------------------------------------
  LICENCE & CONTACT
--------------------------------------------------------------------
  Licence    : TRAMSYS LAB
  Maintainer : Eni Solomon Laughter — Chang'an University

  For source attribution and data provenance details,
  see PROVENANCE_NOTES.txt in this directory.

====================================================================
  END OF README
====================================================================
