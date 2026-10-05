# Data provenance

## Verified local facts

- Coverage: west 8.45, south 52.93, east 9.10, north 53.30.
- OSM base, roads and aeroways: the original Bremen MapGen configuration uses the regional OpenStreetMap PBF.
- LoD1 buildings: the same configuration uses Overture buildings; extraction script selects release 2026-06-17.0.
- LoD2 landmarks: GeoInformation Bremen CityGML; 79 catalog entries, 141 building parts, 19,888 surfaces and 60,188 triangles.
- Population label: validated Zensus 2022 100 m grid sum 965,312; reference date 15 May 2022; cell-midpoint clipping.
- Playable demand: 21,234 points, 44,954 commuter groups, 403,307 residents/jobs/represented commuters; every group has drivingSeconds.

## Demand methodology and verification

The published demand is a synthetic commuter model, not individual travel records. All 44,954 (origin, destination, commuter count) groups match the locally generated 2024 point-pair table exactly, including the total 403,307. Residential origins use the Zensus grid; job destinations and municipality employment weights are generated model inputs. The processing inputs include the Bundesagentur für Arbeit municipality employment statistics (2022) and the regional commuter calculation.

The saved Regionaldatenbank response explicitly identifies table 19321-Z-22, Einpendelverflechtungen nach Geschlecht, reference date 30 June 2024, for Bremen and surrounding municipalities. It includes its own attribution and dl-de/by-2-0 notice. Small or missing flows are suppressed in the source; point-level allocation is a modelling choice and should not be interpreted as measured precision.

Final point records exactly match the repaired demand point set. Final commuter records exactly match the saved routed demand output. All groups have positive drivingSeconds; individual repaired travel times have not been independently recalculated. The original end-to-end generation scripts are not included, so complete reproducibility is limited. The published demand file is supplied unchanged from the earlier local map release.

Sources: Statistische Ämter des Bundes und der Länder, Regionaldatenbank Deutschland, table 19321-Z-22 (2024), https://www.regionalstatistik.de/ ; Zensus 2022, https://www.destatis.de/DE/Themen/Gesellschaft-Umwelt/Bevoelkerung/Zensus2022/_inhalt.html ; Statistik der Bundesagentur für Arbeit, municipality employment data (2022), https://statistik.arbeitsagentur.de/ . Modelling, clipping, point allocation and road travel-time processing modify these inputs.

No special-demand tags are selected: visual presence of an airport or stadium alone does not demonstrate passenger or leisure demand.
