# Michigan Wind Speed & Precipitation Interpolation

This project was completed for an undergraduate course as an exercise in spatial statistics and geostatistical interpolation. The core question I aimed to answer was: is there a correlation between wind speed and precipitation across Michigan, and does that relationship vary by season or proximity to the Great Lakes?

Using observations from NOAA weather stations, surfaces for wind speed and precipitation were generated with ordinary krigin*, allowing values to be estimated at unmeasured locations across the state based on the spatial autocorrelation of nearby station readings.

## Data and Methodology

- **Source:** NOAA weather station observations
- **Year:** 2021
- **Region:** Michigan 
- **Variables:**
  - Mean precipitation (January, July)
  - Mean wind speed (January, July)
- **Station locations** are plotted as points on each map

Winter (January) and summer (July) were both analyzed to check whether any wind–precipitation relationship was consistent across seasons or was season-dependent.

Ordinary kriging was used as the primary interpolation method for all surfaces. For each variable/season combination, two outputs were generated:

Prediction standard error surface was used to measure interpolation uncertainty - generally lowest near clusters of stations and highest in areas with sparse station coverage (e.g., northern Lake Michigan shoreline, far northern Lower Peninsula)

### January Precipitation
![Interpolated January Mean Precipitation](January_Precipitation.png)

### January Wind Speed
![Interpolated January Mean Wind Speed](January_Wind.png)

### January Wind Speed — Prediction Standard Error
![Prediction Standard Error - January Wind Speed](January_Standard_Error.png)

### July Precipitation
![Interpolated July Mean Precipitation](images/July_Precipitation.png)

### July Wind Speed
![Interpolated July Mean Wind Speed](images/July_Wind.png)

### July Wind Speed — Prediction Standard Error
![Prediction Standard Error - July Wind Speed](July_Standard_Error.png)

## Key Findings

- A slightly positive relationship between wind speed and precipitation is visible in areas near the Great Lakes shorelines, most notably along the western/lakeshore side of the Lower Peninsula.
- This pattern is consistent with*lake-effect dynamics: onshore winds picking up moisture off the relatively warmer lake and depositing it as precipitation over nearby land. 
- The relationship is not strong or uniform statewide. 
- Prediction standard error was consistently higher in areas with fewer nearby stations, showing reduced confidence in the interpolated estimates there.

