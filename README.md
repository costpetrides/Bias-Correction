# Bias correction

Static view of the IDW bias-correction results for NO₂, O₃ and PM2.5.

Open `index.html` and choose a pollutant and a method. The page shows 2015, 2022, 2023 and 2024 together. The address keeps the selection, for example `#NO2/IDW_ADD`.

## How the files are split

```
results/{pollutant}/{method}/{year}/
```

Pollutants are `NO2`, `O3` and `PM25`. Methods are `IDW_ADD` (additive) and `IDW_MULT` (multiplicative). Years are `2015`, `2022`, `2023` and `2024`.

2015 is the NILU cross-validation year. The bias is fitted on stations with Active = 1 and scored on Active = 0. That folder also has the parameter-search heatmaps.

2022–2024 compare every station in that year's observation file with the raw EMEP scenario and the scenario after the 2015 bias correction.

Each year folder contains the maps, the station scatter, the country plot, `summary.csv`, `country.csv` and `stations.csv`. The 2015 folder also contains `best_params.csv` and `idw_search.csv`.

Model NetCDF files and the original observation files are not in this repository.
