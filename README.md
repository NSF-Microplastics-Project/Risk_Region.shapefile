# IETC NSF Microplastics Study Risk Region Shapefile

<br>

This repository houses the IETC NSF Microplastics study risk regions and its associated documentation. This zipped shapefile will always be the most up to date data available. The risk regions are projected in:

- NAD 1983 (2011) StatePlane California III FIPS 0403 (Meters)
- WKID: 6419

## Usage

This shapefile should be accessed directly from GitHub to ensure the latest version is used in analyses. This method requires the [sf](https://r-spatial.github.io/sf/) and IETC package. Follow these steps to use this shapefile in RStudio:

1. Install/Load IETC Library
2. Obtain Raw File Address (See Below) and Store as a Variable in RStudio
3. Use Raw Address as Input to unzipShape() Function; Store as Variable

#### Example

1. Load IETC package for `unzipShape Function`:
```R
devtools::install_github("WWU-IETC-R-Collab/IETC")
library(IETC)
```
2. Raw Address:
```R
RiskRegions.z <- "https://github.com/NSF-Microplastics-Project/Risk_Region.shapefile/raw/main/Data/SFB_RiskRegions_20210304_SP.zip"
```
3. Load Shapefile Using `unzipShape` and Raw Address:
```R
RiskRegions <- unzipShape(RiskRegions.z)
```

<br>

## File Locations

File | Location
------------ | -------------
NSF Microplastics Risk Regions Shapefile | [Data Folder](https://github.com/NSF-Microplastics-Project/Risk_Region.shapefile/tree/main/Data)
IETC Package and unzipShape Function | [WWU R Collab](https://github.com/WWU-IETC-R-Collab/IETC)

<br>

## Issues/Problems?

Please create an [issue](https://github.com/NSF-Microplastics-Project/Risk_Region.shapefile/issues).

<br>

# Current Shapefile Creation Method

The risk regions contained within this repository are based off of HUC08 watershed and HUC12 boundaries from USGS WBD as provided on 2021-03-04.

* HUC08 #18050001 (Suisun Bay)
* HUC08 #18050002 (San Pablo Bay)
* HUC08 #18050003 (Coyote Bay)
* HUC08 #18050004 (San Francisco Bay)

A small modification was made to HUC08 Coyote Bay to include portions of HUC12 boundaries south of the I-84 bridge (Newark to East Palo Alto) within the southern end of the San Francisco Bay HUC08 boundary.

* Portion of HUC12 #180500041001 (San Francisco Bay Estuaries)
* Portion of HUC12 #180500041002 (Oakland Inner Harbor-San Francisco Bay)
