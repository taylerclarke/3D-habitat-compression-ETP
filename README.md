# 3D Habitat Compression – Min/Max Depth Estimates (Eastern Tropical Pacific)

This repository contains `.rds` files with monthly, species-specific estimates of minimum and maximum habitat depth** for pelagic fishes in the Eastern Tropical Pacific.

The depth limits were calculated following the workflow described in:

Clarke, T. M., Palacios-Abrantes, J., Villalobos-Rojas, F., Beita-Jimenez, A., Romero-Chaves, R., Sánchez, C., Bejarano, S., Zapata, F. A., Madeira, C., DeFalco, C., Tjiputra, J., Mooney, P., & Cheung, W. W. L. (2026). *Three-dimensional habitat compression of pelagic fishes in the Eastern Tropical Pacific under El Niño–Southern Oscillation (ENSO) and climate change* (manuscript submitted for publication).

## Data files

Each `.rds` file corresponds to one species. The species scientific name is included at the beginning of the filename.

### Historical period (2004–2022)
Files with the pattern:

`<species>_lenfest_3D_AGIv2_gobaio2_minmaxdepth_2004-2022_erm.rds`

contain estimates for 2004–2022.

### Future high-emissions scenario (SSP5-8.5, 2031–2050)
Files with the pattern:

`<species>_lenfest_3D_AGIv2_deltassp585_gobaio_minmaxdepth_2031-2050_erm.rds`

contain estimates for 2031–2050 under the SSP5-8.5 scenario.

## Contents of each `.rds` file

Each `.rds` file is an R object (typically a data frame/tibble) with the following columns:

| Column name            | Description |
|------------------------|-------------|
| `lat`                  | Latitude (decimal degrees) |
| `lon`                  | Longitude (decimal degrees) |
| `year`                 | Year of the estimate |
| `month`                | Month of the estimate (1–12) |
| `depthmax_presfin`     | Final estimated maximum depth limit (meters) |
| `depthmin`             | Estimated minimum depth limit (meters) |

Interpretation: For each species, the dataset provides the estimated minimum and maximum depth bounds each month and year across the specified period (2004–2022 or 2031–2050), gridded by `lat`/`lon`.


