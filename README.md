<<<<<<< HEAD
# Welcome to SOfish Diversity! 🎣

This application allows you to explore the diversity of fish species in the Southern Ocean.
The app can be consulted here: https://sofish.naturalsciences.be

***

### Key Features
* **Interactive Map:** Visualize species occurrences on a live map. You can zoom in, pan, and draw a polygon to filter data in a specific area.
* **Flexible Filters:** Use the **`Filters`** tab to narrow down your search by taxonomy, traits, IUCN status, and more.
* **Diversity Analysis:** The app calculates and displays diversity metrics for your filtered data, both spatially (by MEASO region) and temporally (as a moving average over time).
* **Temporal Trends:** The **`Temporal Diversity`** tab shows how diversity metrics like the Shannon Index and Species Richness change over time, alongside a measure of sampling effort.
* **H3 Diversity Grid:** The **`Spatial H3 Polygons`** tab flexibly visualizes different diversity estimators.

***

### How to Use
1.  Navigate to the **`Filters`** tab to set your desired criteria.
2.  Use the map on the **`Display`** tab to visualize the results.
3.  Draw a polygon on the map to define a custom area of interest.
4.  Check the different tabs to see the calculated metrics and maps based on your filters.

***

### Data Source
All occurrence data is sourced from the GBIF and OBIS. Traits are sourced from Fishbase.<br>
GBIF Occurrence Download https://www.gbif.org/occurrence/download/0019157-250802193616735 Accessed from R via rgbif (https://github.com/ropensci/rgbif) on 2025-08-06
=======
# SOfish Diversity

An interactive R Shiny application for exploring, filtering, and analyzing fish species occurrence data from the Southern Ocean. Species taxonomy is sourced from [WoRMS](https://www.marinespecies.org/) and biological traits from [FishBase](https://www.fishbase.se/).

---

## Features

- **Interactive map** — occurrence points coloured and sized by user-selected traits (family, genus, IUCN status, vulnerability, length)
- **Flexible filtering** — filter by taxonomy, body measurements, depth range, ecology, conservation status, commercial importance, basis of record, and RAMS species membership
- **Spatial polygon filter** — draw a polygon on the map or paste a WKT string to spatially subset records
- **Diversity metrics** — overall and MEASO-region-level indicators (Shannon, Simpson, ES50, Hill numbers) via [`obisindicators`](https://github.com/iobis/obisindicators)
- **Temporal diversity** — moving-average diversity trends over time, per MEASO region or drawn polygon
- **H3 hexagonal grid** — spatial diversity visualised on Uber's H3 grid at any resolution
- **CSV downloads** — all filtered tables and diversity outputs are exportable

---

## Database

The app reads from a single **Parquet file** (`Actinopterygii_database.parquet`) loaded at startup into an in-memory [DuckDB](https://duckdb.org/) instance. This file must be placed in the same directory as `app.R`.

### Building the database

The Parquet file is assembled from two sources:

1. **Occurrence records** — download Southern Ocean *Actinopterygii* occurrences from [OBIS](https://obis.org/) or [GBIF](https://www.gbif.org/), filtered to the Southern Ocean boundary polygon included in the app.
2. **Taxonomy** — resolved against [WoRMS](https://www.marinespecies.org/) using the [`worrms`](https://cran.r-project.org/package=worrms) R package to add valid `AphiaID`, accepted names, and higher taxonomy.
3. **Traits** — merged from FishBase via the [`rfishbase`](https://cran.r-project.org/package=rfishbase) R package (length, weight, depth range, vulnerability, IUCN status, commercial importance, catching method, etc.).
4. **RAMS flag** — a boolean column `RAMS_species` indicating membership in the [RAMS checklist](https://www.marinespecies.org/rams/).

Once assembled, write the combined data frame to Parquet:

```r
arrow::write_parquet(df, "Actinopterygii_database.parquet")
```

Place the resulting file in the project root alongside `app.R`.

---

## Running with Docker

### Requirements

- [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://docs.docker.com/compose/) installed
- `Actinopterygii_database.parquet` present in the project root

### Project structure

```
.
├── app.R
├── Actinopterygii_database.parquet
├── Dockerfile
├── docker-compose.yaml
├── renv.lock
├── about.md
├── cite_us.md
└── report_bug.md
```

### Build and start

```bash
docker compose up --build
```

The app will be available at **http://localhost:8081**.

To run in the background:

```bash
docker compose up --build -d
```

### Stop

```bash
docker compose down
```

### Notes

- The container is built on [`rocker/geospatial:4.4.1`](https://rocker-project.org/) and R packages are restored from `renv.lock` at build time.
- Memory is capped at **6 GB** in `docker-compose.yaml`. Adjust the `limits.memory` value if your dataset is larger.
- The environment variables `OPENBLAS_CORETYPE=GENERIC` and `MKL_DEBUG_CPU_TYPE=5` prevent illegal-instruction errors on non-AVX hosts (e.g. older servers or ARM machines).
- To rebuild after code changes without reinstalling R packages, Docker's layer cache means only the `COPY . /srv/shiny-server/` layer is re-run — keeping rebuilds fast.

---

## Citation

If you use this app or the underlying data in your work, please cite it via the **Help → Cite Us** tab inside the app.

---

## Author

Pablo Deschepper
>>>>>>> personal/main
