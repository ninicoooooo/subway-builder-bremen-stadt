# Bremen Stadt – LoD2

By **NINICOO** · version **1.1.5** · Subway Builder **1.7.2 or later**.

A custom map of Bremen and its surroundings, with the Weser, harbour districts, roads and native building foundations. Approximately 965,000 people live within the map area according to the Zensus 2022 grid. Playable commuter demand represents 403,307 people; this is distinct from the overall population.

For the detailed landmark buildings and the preserved road styling, also install **Bremen Stadt – LoD2 Wahrzeichen** (`ninicoo-bremen-landmarks`). It adds 79 landmark entries from Bremen's official LoD2 models. Foundations are hidden by default with the companion mod and can be enabled manually.

## Installation

Install the map through Railyard, install and enable the companion mod, and launch Subway Builder using Railyard. 

City code: `BREM`. Registry map ID: `ninicoo-bremen-stadt-lod2`.

This is a separate map from the existing Railyard Bremen listing (`HB`). Older locally created Bremen saves may reference a different mod ID; save migration has not been verified.

## Demand detail

Residential locations derive from 100 × 100 metre Zensus 2022 grid cells. Official 2024 municipality commuting (Regionaldatenbank 19321-Z-22) and 2022 employment data inform 44,954 synthetic origin–destination groups across 21,234 points, representing 403,307 commuters. Each group has car travel-time and distance values. Point-level flows and job allocations are model outputs, not measured individual journeys or per-building employee counts. No additional airport-passenger, student or leisure demand is included.

## Data and credits

See ATTRIBUTION.md and DATA-PROVENANCE.md. Demand is a synthetic allocation based on census, employment and regional commuter statistics. The original end-to-end scripts are not included; reproducibility and travel-time validation limits are documented.

## Release assets

Upload the map ZIP and the standalone `manifest.json` to the same GitHub release. Use a dedicated map repository; the companion mod uses its own release repository to avoid downloading the wrong ZIP.
