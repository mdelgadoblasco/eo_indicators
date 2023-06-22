
# Finished Goods Inventory indicator: 
This indicator uses the time series of Sentinel-1 Normalized Radar Backscatter information averaged over the user-defined area of interest (AOI) to provide a time overview of the backscatter variations which will be linked to the direct occupancy of the monitored areas.

The input parameters needed are:
- observation period from / to in YYYY-MM-DD format
- AOI in Well-Known Text format (WKT)

The implemented algorithm will retrieve, using the SentinelHub Statistical API, the average orthorectify and terrain-flattened gamma0 over the defined area (AOI) aggregated per day. Using gamma0 instead of the typical sigma0 allows us to aggregate the values from different orbits as it is geometry independent and corrected to remove its dependency on the incident angle.

More information about the **GAMMA0_TERRAIN** processing option available from Sentinelhub is available [here]([https://forum.sentinel-hub.com/t/sentinel-1-radiometric-terrain-correction-now-available/3194](https://docs.sentinel-hub.com/api/latest/data/sentinel-1-grd/#processing-options))

An example of a possible plot of such variation could be: 
<p><center> <img src="images/E8_ts_sample.png" width="700"/> </p></center>
