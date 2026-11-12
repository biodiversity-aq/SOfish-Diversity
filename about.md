<<<<<<< HEAD
# Welcome to SOfish Diversity! 🎣

This application allows you to explore the diversity of fish species in the Southern Ocean.

***

### Key Features
* **Interactive Map:** Visualize species occurrences on a live map. You can zoom in, pan, and draw a polygon to filter data in a specific area.
* **Flexible Filters:** Use the **`Filters`** tab to narrow down your search by taxonomy, traits, IUCN status, and more.
* **Diversity Analysis:** The app calculates and displays diversity indicators for your filtered data, both spatially (by MEASO region) and temporally (as a moving average over time).
* **Temporal Trends:** The **`Temporal Diversity`** tab shows how diversity metrics like the Shannon Index and Species Richness change over time, alongside a measure of sampling effort.
* **H3 Diversity Grid:** The **`Spatial H3 Polygons`** tab flexibly visualizes different diversity estimators.

***

### How to Use
1.  Navigate to the **`Filters`** tab to set your desired criteria.
2.  Use the map on the **`Display`** tab to visualize the results.
3.  Draw a polygon on the map to define a custom area of interest.
4.  Check the different tabs to see the calculated diversity indicators and maps based on your filters.

***

### Data Sources
- **Occurrence data** is sourced from GBIF and OBIS. 
- **Traits** are sourced from Fishbase and WoRMS.<br>
<br>
<br>
<br>
<div style="background-color: #f0f0f0; border-radius: 10px; padding: 15px; margin: 10px 0; border: 1px solid #d3d3d3;">
<span style="font-size: 0.8em;">
  <strong>License and Citation</strong><br>
  This application is licensed under the <a href="https://opensource.org/licenses/MIT" target="_blank">MIT License</a>. If you use this tool or data in your research, please cite the relevant data sources (see 'Cite Us' tab) and this application.<br>
</span>
<span style="font-size: 0.8em;">
  <strong>Source Code and Issues</strong><br>
  <a href="https://github.com/thesnakeguy/SOfish-Diversity" target="_blank">https://github.com/thesnakeguy/SOfish-Diversity</a>
</span>
=======
# SOfish Diversity

**Explore the fish diversity of the Southern Ocean — filter, map, and analyse occurrence data enriched with taxonomy and biological traits.**

---

### What this app does

| Tab | Purpose |
|---|---|
| **Display** | Interactive occurrence map - colour and size points by family, IUCN status, vulnerability, and more |
| **Filters** | Narrow records by taxonomy, body size, depth, ecology, conservation status, commercial traits, and record metadata |
| **Active Filters** | Review what filters are currently applied and how many records and species remain |
| **Table** | Browse and download the filtered occurrence dataset as CSV |
| **Spatial Diversity** | Diversity indicators (Shannon, Simpson, ES50, Hill numbers) overall and broken down by MEASO region |
| **Temporal Diversity** | Moving-average diversity trends over time, with sampling effort overlay |
| **Spatial H3 Polygons** | Hexagonal grid map of spatial diversity at any H3 resolution |

---

### Quick start

1. Open the **Filters** tab and select a taxon (e.g. a family or order) to scope the dataset.
2. Switch to **Display** to see matching occurrences on the map. Optionally draw a polygon to restrict results to a custom area.
3. Explore the **Spatial Diversity** and **Temporal Diversity** tabs to analyse patterns in your filtered data.
4. Download any table as CSV using the buttons within each tab.

Note: the map is showing the first 4,000 points in view — zoom in further, or draw a boundary box, to see the rest.

---

### Data sources

- **Occurrences** — [GBIF](https://www.gbif.org/) and [OBIS](https://obis.org/)
- **Taxonomy** — [WoRMS](https://www.marinespecies.org/) (all scientific names and AphiaIDs are WoRMS-validated)
- **Biological traits** — [FishBase](https://www.fishbase.se/) (length, weight, depth range, vulnerability, commercial importance, etc.)
- **RAMS checklist** — [Register of Antarctic Marine Species](https://www.marinespecies.org/rams/)

---

<div style="background:#f0f6ff; border-radius:10px; padding:14px 18px; border:1px solid #c5d8ee; font-size:0.82em; line-height:1.7;">

**License** — Released under the [MIT License](https://opensource.org/licenses/MIT).

**Citation** — If you use this app or its data in your research, please cite the relevant data sources and this tool.  
GBIF occurrence download: <a href="https://doi.org/10.15468/dl.uf8fd2" target="_blank">doi:10.15468/dl.uf8fd2</a>

**Source code & issues** — <a href="https://github.com/thesnakeguy/SOfish-Diversity" target="_blank">github.com/thesnakeguy/SOfish-Diversity</a>

</div>

---

### Partners & Data Providers

<div align="center" style="display: flex; flex-wrap: wrap; align-items: center; justify-content: center; gap: 20px; margin-top: 20px;">
  <a href="https://www.naturalsciences.be/" target="_blank">
    <img src="https://eurogoos.eu/api/media/file/natural-sciences.png" alt="Museum of Natural Sciences (RBINS)" height="80" style="margin: 10px;">
  </a>
  <a href="https://www.biodiversity.aq/" target="_blank">
    <img src="https://avatars.githubusercontent.com/u/48433448?s=200&v=4" alt="biodiversity.aq" height="150" style="margin: 10px;">
  </a>
  <a href="https://obis.org/" target="_blank">
    <img src="https://www.biodiversity.be/5500/download" alt="OBIS" height="100" style="margin: 10px;">
  </a>
  <a href="https://www.gbif.org/" target="_blank">
    <img src="https://www.biodiversity.be/3005/download" alt="GBIF" height="100" style="margin: 10px;">
  </a>
  <a href="https://www.marinespecies.org/" target="_blank">
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSTHwDDcEKxw6lR1ukbQ28-QrQS1IF0MJ_IBLpakt5pZQ&s=10" alt="WoRMS" height="50" style="margin: 10px;">
  </a>
  <a href="https://www.fishbase.se/" target="_blank">
    <img src="https://www.fishbase.se/images/png/Fishbase-logo-CMYK.png" alt="FishBase" height="50" style="margin: 10px;">
  </a>
>>>>>>> personal/main
</div>