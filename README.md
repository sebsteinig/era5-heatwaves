# era5-heatwaves

https://github.com/sebsteinig/era5-heatwaves/assets/80361118/a9d32081-6e6f-4741-99f6-553462957f84

Analysis and visualisation of ERA5 hourly 2m air temperature for July 2023. This was the warmest month on record and was characterised
by multiple, simultaneous heatwaves across the Northern Hemisphere (and winter warm spells in the Southern Hemisphere).

The analysis was done with Python and is documented in the Jupyter Notebook "era5_july-2023_heatwaves.ipynb". Processed temperature data
and calculated heatwave metrics are exported to bitmap (PNG) for visualisation with the [ClimateArchive engine](climatearchive.org). 
The final visualisation is shown at the top.

Input data is too large for GitHub, but can be freely obtained from the sources below:

## input data
### ERA5 reanalysis
Input data includes:
1. era5_2t_hourly_202307.nc: Hourly data for July 2023.
2. era5_2t_daymean_clim1991-2020_lowpass_07.nc: Daily mean 2m temperature climatology for July based on the 1991-2020 reference period.
3. era5_2t_daymax_clim1991-2020_lowpass_07.nc: Daily maximum 2m temperature climatology for July based on the 1991-2020 reference period.
4. era5_2t_daymin_clim1991-2020_lowpass_07.nc: Daily minimum 2m temperature climatology for July based on the 1991-2020 reference period.

Data can be downloaded from the [Copernicus Climate Data Store](https://cds.climate.copernicus.eu/cdsapp#!/home) and is published under a 
[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). 

### Gridded Population of the World (GPW), v4
Not essential, only used for a summary metric of the global population affected by the July heatwaves. Data has been used at 15 arc-minute resolution
and can be downloaded from [SEDAC](https://sedac.ciesin.columbia.edu/data/collection/gpw-v4). The GPW data collection is licensed under the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0).

## running the notebook
Easiest way to run the notebook locally is to first download the repo with

```
git clone https://github.com/sebsteinig/era5-heatwaves
```
and then install conda (if not installed already). Then create an environment env_name with

```
conda env create --name env_name --file=environment.yml
```
using the environment.yml file from this repository to install all necessary python packages. The notebooks can then be run interactively by typing

```
jupyter lab
```
