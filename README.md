# Climate-Change
Repository for Data 3320 project 3.

# Project Description
This project will apply fourier transformation, spectral analysis, prophet model forecasting, and regression analysis to determine how various sea surface temperatures (SST) are changing in the North Atlantic and Indian oceans. This process will provide insight into which major trends govern SST changes and which of the two oceanic regions is more heavily affected by climate change.

# Data
Data used is sourced from the ERA5 Reanalysis project, which can be viewed here: https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-single-levels?tab=overview

The project is managed by the European Center for Medium-Range Weather Forecasting (ECMWF). The ECMWF is a global leader in numerical weather research and forecasting, and holds the largest meteorology database.

The data files imported can be viewed in the north_atlantic.csv and indian.csv files in this repository.

# Spectral Analysis
To perform analysis, the data was first transformed into a fourier series using numpy's fast fourier transform feature. The resulting series were used to generate spectromagrams, where spikes are identified which reveal the frequencies of major trend components. A bandpass filter is applied around the identified trends to reconstruct a fourier series with reduced noise.

# Forecasting and Regression
The above mentioned filtered series are passed through the prophet model to create a forecast of sea surface temperatures for each ocean. These forecasts are fitted with elastic net least squares regression to quantify the trend in SST, based on time.

# Authors
Joel Stockton Uy 

https://www.linkedin.com/in/joel-uy/

# License
This project is licensed under the terms of Open Software License 3.0

License Keyword: OSL-3.0
