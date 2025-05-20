# 📘 data_retrival.ipynb

## Overview

This Jupyter Notebook provides code to retrieve and process hydrometeorological datasets essential for flood risk assessment and culvert performance modeling. It is part of a broader project analyzing the spatio-temporal dynamics of flooding and infrastructure vulnerability in New York State.

The notebook currently focuses on accessing and handling two main datasets:
- NOAA's **AORC (Analysis of Record for Calibration)** dataset
- NASA's **NEX-GDDP-CMIP6** downscaled climate projections via the Microsoft Planetary Computer

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
- **Use Case**: Historical rainfall inputs for hydrologic modeling and infrastructure performance evaluation

### 2. NEX-GDDP-CMIP6 – NASA Earth Exchange Downscaled Climate Projections
- **Source**: NASA / Microsoft Planetary Computer
- **Access Method**: STAC API with `pystac-client`, `xarray`, and `planetary_computer`
- **Format**: NetCDF / Zarr
- **Temporal Resolution**: Daily
- **Spatial Resolution**: ~25 km (0.25°)
- **Time Period**: Historical (1970–2014), Projections (2015–2100)
- **Variables**:
  - Daily precipitation (pr)
- **Use Case**: Future rainfall projections under different climate scenarios for hydrologic simulation and risk assessment

---
