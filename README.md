# <ins>Annual Cumulative Precipitation and Average Temperature Correlation Analysis in Nairobi County</ins>

This project analyzes the correlation between annual cumulative precipitation and average temperature in **Nairobi County, Kenya, from 2010 to 2019**. It utilizes Earth Engine to access the TerraClimate dataset, which provides monthly climate data. The analysis is performed using the _xarray_ and _xee_ Python libraries, enabling the handling and analysis of multi-dimensional geospatial data.

The study first defines Nairobi County as the region of interest using the _FAO GAUL Level 2 administrative boundaries dataset_. It then loads the _TerraClimate_ dataset, filters it for the specified time period, and selects _precipitation (pr), minimum temperature (tmmn), and maximum temperature (tmmx)_ bands. This Earth Engine data is converted into an xarray dataset for easier manipulation.

**Annual cumulative precipitation** is calculated by summing the monthly precipitation data for each year. **Annual average temperature** is derived by averaging the monthly minimum and maximum temperatures for each year, applying a scale factor of _0.1_ as per the TerraClimate dataset documentation. The resulting annual precipitation and temperature data are visualized using maps generated with the _matplotlib_ library.

Finally, the project computes the _Pearson correlation coefficient_ between the annual cumulative precipitation and average temperature across the _time_ dimension for each spatial location within Nairobi County using the _xr.corr()_ function. The resulting correlation map is also visualized.
