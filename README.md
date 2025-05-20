# 🌧️ Climate Data Retrieval Scripts

## Overview

This Jupyter Notebook provides code to retrieve and process hydrometeorological datasets essential for flood risk assessment and culvert performance modeling. It is part of a broader project analyzing the spatio-temporal dynamics of flooding and infrastructure vulnerability in New York State.

The notebook currently focuses on accessing and handling two main datasets:
- NOAA's **AORC (Analysis of Record for Calibration)** dataset
- NASA's **NEX-GDDP-CMIP6** downscaled climate projections via the Microsoft Planetary Computer

---
## 📁 Repository Structure

```
data_retrival/
├── AORC/                  # Scripts and utilities to access AORC historical climate data
├── NEX_GDDP_CMIP6/        # Scripts to retrieve CMIP6 future climate projections
├── LICENSE                # MIT License
└── README.md              # This file
```

---

## 📦 Datasets Included
### 1. AORC – Analysis of Record for Calibration
- **Source**: NOAA National Water Model archive
- **Access Method**: Public AWS S3 via `fsspec` and `xarray`
- **Format**: Zarr / NetCDF
- **Temporal Resolution**: Hourly
- **Spatial Resolution**: ~1 km
- **Time Period**: 1979–Present
- **Variables**: 
  - Precipitation (APCP_surface)

### 2. NEX-GDDP-CMIP6 – NASA Earth Exchange Downscaled Climate Projections
- **Source**: NASA / Microsoft Planetary Computer
- **Access Method**: STAC API with `pystac-client`, `xarray`, and `planetary_computer`
- **Format**: NetCDF / Zarr
- **Temporal Resolution**: Daily
- **Spatial Resolution**: ~25 km (0.25°)
- **Time Period**: Historical (1970–2014), Projections (2015–2100)
- **Variables**:
  - `pr`: Precipitation
  - `tas`: Near-surface air temperature
  - `tasmax`: Maximum daily temperature
  - `tasmin`: Minimum daily temperature
  - `hurs`: Relative humidity
  - `huss`: Specific humidity
  - `rlds`: Downward longwave radiation
  - `rsds`: Downward shortwave radiation
  - `sfcWind`: Near-surface wind speed
---

## 🪪 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.
