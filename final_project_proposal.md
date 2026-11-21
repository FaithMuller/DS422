# DS 422 Geocomputation – Final Project Proposal

**Name: Faith Muller**

**Date: Noverember 19, 2026**

------------------------------------------------------------------------

Fill this out before you start on your analysis. Write your answers under each question. A few sentences is fine for most of them. Be specific, though: "I'll look at land use" is too vague, but "I'll compare sugar land change across Maui from 2001 to 2021" is better.

Download this file and add it to your DS422 Repository, then edit right in the github browser.

------------------------------------------------------------------------

## 1. My research question

What do you want to find out? Phrase it as a question. Mention the place and time period if they are relevant.

<!-- Write your answer below this line -->

How does tuna fishing effort in the Marshall Islands Exclusive Economic Zone (EEZ) change in location between El Niño years (2019,2023) and La Niña years (2021, 2022), and does purse seine and longline vessels respond differently (2017-2025)?

------------------------------------------------------------------------

## 2. The dataset(s) I will use to approach my research question

List each dataset and where it comes from (agency, website, link). Note the format (shapefile, raster, CSV with coordinates, etc.) and the spatial and temporal coverage if you know it.

<!-- Write your answer below this line -->

1.  Fishing efforts:
    - [Global Fishing Watch (GFW)](https://globalfishingwatch.org), a nonprofit

    - Access: in R with the oceandatr package (get_gfw()), using a free GFW API token.

    - Format: gridded raster data

    - Spatial coverage: global, cut to the Marshall Islands’ EEZ. Source resolution 0.1°, summarized to a 25 km grid.

    - available 2012–present. I will use 2017–2025, by year and gear type, since GFW coverage improved in 2017.
2.  EEZ boundary
    - [Flanders Marine Institute (VLIZ)](https://www.marineregions.org/downloads.php), Marine Regions

    - **Format:** shapefile (polygon)

    - **Spatial coverage:** global, filtered to the Marshall Islands

    - **Temporal coverage:** static boundary (World EEZ v12, 2023)
3.  **Oceanic Niño Index (ONI)**
    - **Agency:** [NOAA Climate Prediction Center](https://www.cpc.ncep.noaa.gov/products/analysis_monitoring/enso/oni/v6/)

    - **Format:** table of 3-month seasonal values (no coordinates)

    - **Spatial coverage:** Niño 3.4 region (5°N–5°S, 120°–170°W), a single index value

    - **Temporal coverage:** 1950–present. I will use 2017–2025 to identify El Niño and La Niña years.

------------------------------------------------------------------------

## 3. The specific geocomputation techniques I will use to answer my research question

What methods will you actually run? For example, image segmentation, spatial statistics, time series analysis etc.

<!-- Write your answer below this line -->

- Raster processing: download and clip fishing maps

- Change detection: compare El Niño and La Niña maps

- Zonal statistics: total fishing east vs. west

- Mean center: find middle of fishing yearly

- Time series: track changes from 2017–2025

- Correlation: link fishing shifts to El Niño

------------------------------------------------------------------------

## 4. 3-5 peer-reviewed publications or news articles surrounding my research question

Give the link below. Add a sentence or two on why each source is relevant to your project.

1.  <https://spccfpstore1.blob.core.windows.net/digitallibrary-docs/files/fc/fc9f6f2a8b3dcf08a6ca7bf9a7171aa8.pdf>.

This report illustrates how El Niño and La Niña affect tuna catches and purse seine and longline fishing in the Marshall Islands.

2.  <https://www.mdpi.com/2071-1050/14/3/1217>

This case-study shows that best tuna fishing areas moved east during El Niño, near the Marshall Islands.

3.  <https://repository.library.noaa.gov/view/noaa/71287/noaa_71287_DS1.pdf>

This study shows how El Niño changes where purse seine vessels choose to fish at.

4.  <https://mail.tunaresearch.org/reprints/Science_Kroodsma_et_al_2018.pdf>

It's a paper that explains how Global Fishing Watch tracks fishing vessels with satellite.

5.  <https://library.sprep.org/sites/default/files/2021-08/pathways-sustaining-tuna-oceania-climate-change.pdf>

Explains why changes in where tuna are found matters for Pacific Islands like the Marshall Islands.

------------------------------------------------------------------------
