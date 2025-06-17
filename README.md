# mlt-ulf
A jupyter notebook for calculating a magnetic local time dependent Pc5 ultra-low frequency wave index from [SuperMAG](https://supermag.jhuapl.edu/mag/) data. It uses wavelet transform to get the power and the scale-averaged wavelet (equation 24 in Torrence and Compo) to resolve power in the Pc5 band.

## Requirements
This script requires: [numpy](https://numpy.org/), [netCDF4](https://unidata.github.io/netcdf4-python/), [pandas](https://pandas.pydata.org/).
The wavelet transform is done by using a module called PyCWT. Installation instructions can be found at: https://pycwt.readthedocs.io/

## Setting up
Download SuperMAG yearly data. The script reads yearly files in the form: `all_stations_all{YYYY}.netcdf`. 

Before running the following parameters need to be set up

What year the data are from:
```
# year
YYYY = 2023
```

Choose the magnetic latitude range:
```
# latitude (60-70,70-80,etc.)
lat_set = (65,70)
```

Choose which magnetic field component:
```
# component (N,E or H)
component = 'N'
```

## Data
Index for years 1995–2023 in the latitude range 65–70 can be downloaded from [zenodo](https://doi.org/10.5281/zenodo.15372450)

## References
Torrence, C. and Compo, G. P.. A Practical Guide to Wavelet Analysis. Bulletin of the American Meteorological Society, American Meteorological Society, 1998, 79, 61-78.
