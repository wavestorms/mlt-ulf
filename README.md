# mlt-ulf
A jupyter notebook for calculating a magentic local time dependent Pc5 ultra-low frequency wave index from [SuperMAG](https://supermag.jhuapl.edu/mag/) data. It uses the scale-averaged wavelet (equation 24 in Torrence and Compo).

## Requirements
This script requires: [numpy](https://numpy.org/), [netCDF4](https://unidata.github.io/netcdf4-python/), [pandas](https://pandas.pydata.org/).
The wavelet transform is done by using a module called PyCWT. Installation instructions can be found in https://pycwt.readthedocs.io/

## Setting up
Before running the following parameters need to be set up

The script reads yearly files in form: `all_stations_all{YYYY}.netcdf`. The year needs to be specified in the code:
```
# year
YYYY = 2023
```

Choose what magnetic latitude range you want to use
```
# latitude (60-70,70-80,etc.)
lat_set = (65,70)
```

From which magnetic field component 
```
# component (N,E or H)
component = 'N'
```

Calculate the narrowband index instead of the Pc5 index
```
# calculate narrowband index?
narrow = False
```

## References
Torrence, C. and Compo, G. P.. A Practical Guide to Wavelet Analysis. Bulletin of the American Meteorological Society, American Meteorological Society, 1998, 79, 61-78.
