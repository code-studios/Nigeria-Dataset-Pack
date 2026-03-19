======================================================================
  DATASET COLLECTION INDEX
  Nigeria HSR Station Optimization — Full Release
  Paper : K-Means-Based Railway Station Location Optimization
          in Nigeria
  Author: Eni Solomon Laughter - Chang'an University
          TRAMSYS LAB
  Date  : 2026-03-18  12:51:16
======================================================================

COLLECTION OVERVIEW
  This collection contains all input, intermediate, and output
  datasets produced in a two-stage analysis to optimize the
  placement of high-speed railway (HSR) stations across
  Nigeria's 37 state capitals using a modified K-means
  clustering algorithm with a geographic penalty term.

  Total datasets : 49 files across 11 thematic groups
  Total folders  : 11

RECOMMENDED VIEWING SEQUENCE
  Follow folder order (01 → 11). Each group builds on the
  previous. The tree below shows the logical progression:

  ┌──────────────────────────────────────────────────────────┐
  │  STAGE 1 — DATA PREPARATION                             │
  ├──────────────────────────────────────────────────────────┤
  │  01  Master Dataset                                      │
  │      The unified feature table — start here.            │
  │                                                          │
  │  02  Spatial and Distance Matrices                       │
  │      How far apart are the capitals?                     │
  │                                                          │
  │  03  Demand Analysis                                     │
  │      Where is travel demand highest?                     │
  │                                                          │
  │  04  Network Adjacency and Redundancy                    │
  │      Which capitals are neighbours or redundant?         │
  │                                                          │
  │  05  Optimization Constraints and Parameters             │
  │      What rules govern the optimization?                 │
  │                                                          │
  │  09  Stage 1 Support and Configuration Files  ◄ NEW     │
  │      Decision trail, sharing rules, audit outputs.      │
  ├──────────────────────────────────────────────────────────┤
  │  STAGE 2 — OPTIMIZATION RESULTS                         │
  ├──────────────────────────────────────────────────────────┤
  │  06  Scenario 1 Results — Complete Coverage              │
  │      Full 37-station MST baseline network.               │
  │                                                          │
  │  07  Scenario 2 Results — Optimized Network              │
  │      Optimized 15-station network results.               │
  │      ★ Use corrected_metrics.json for all figures.      │
  ├──────────────────────────────────────────────────────────┤
  │  SERVICE DESIGN                                          │
  ├──────────────────────────────────────────────────────────┤
  │  08  Train Service Design                                │
  │      Final 3-train OD-locked service corridors.         │
  │                                                          │
  │  10  Service Design and Corridor Planning  ◄ NEW        │
  │      S1 service patterns, corridor plan,                 │
  │      preliminary S2 routes, station utilization.        │
  ├──────────────────────────────────────────────────────────┤
  │  OUTPUTS                                                 │
  ├──────────────────────────────────────────────────────────┤
  │  11  Visualizations and Charts  ◄ NEW                   │
  │      9 maps and charts (300 DPI PNG).                    │
  │      ★ chart3 uses uncorrected values — see note.       │
  └──────────────────────────────────────────────────────────┘

SCRIPT EXECUTION ORDER (for full reproduction)
  Run scripts in this order to regenerate all outputs:
    1.  step0.py                 — raw data audit
    2.  step1_1_data_integration.py — master dataset
    3.  step1_2_distance_matrix.py  — distance & time matrices
    4.  step1_4_gravity_model.py    — demand matrices
    5.  step1_5_redundancy.py       — adjacency & redundancy
    6.  step1others.py              — constraints & parameters
    7.  step2_1_2.py                — S1 MST + S2 K-means
    8.  step2_3_5.py                — evaluation & comparison
    9.  step2_6_7.py                — sensitivity & charts
   10.  stage2_issue_audit.py       — corrected metrics
   11.  network_path.py             — S1 service patterns
   12.  network_path2.py            — S2 preliminary routes
   13.  network_path3.py            — S2 final OD-locked routes
   14.  route.py                    — corridor planning
   15.  bonus.py                    — geographic maps
   16.  OD.py                       — OD corridor map (Group 08)

IMPORTANT NOTES FOR USERS

  1. CORRECTED METRICS: corrected_metrics.json (Group 07)
     contains audited values superseding scenario1_results.json,
     all_evaluations.csv, comparison_table.csv, and
     chart3_scenario_comparison.png (Group 11). Always use
     corrected_metrics.json for publication figures.

  2. DEMAND DATA IS SYNTHETIC: Demand matrices (Group 03)
     are gravity model estimates — not observed counts.

  3. DISTANCES ARE GEODETIC: Most values are Haversine
     great-circle distances × 1.3 road correction factor.
     Check distance_type_matrix.csv for actual vs estimated.

  4. PRELIMINARY vs FINAL TRAIN DESIGN:
     s2_3train_routes_preliminary.json (Group 10) is an
     earlier zone-greedy TSP version. The authoritative
     final design is train_service_design.json (Group 08).

  5. CHART 3 NOTE: chart3_scenario_comparison.png (Group 11)
     plots pre-audit network length values. Regenerate with
     corrected values (S1: 5,106 km; S2: 3,617 km) before
     final manuscript submission.

LICENCE
  TRAMSYS LAB

CONTACT / MAINTAINER
  Eni Solomon Laughter - Chang'an University

======================================================================
  END OF INDEX
======================================================================
