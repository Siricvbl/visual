### Aim 
The visualization aims to intuitively present the differences in average annual hours worked per
worker among countries from 2005 to 2020, in spatial and temporal scales.

### Data 
Three datasets are used for the visualization.
• The annual work hour CSV data is obtained from The Conference Board, which provides
comprehensive economic data for 131 countries within 8 regions in the world.
• Additional dataset of countries' coordinates sourced from GitHub gives each country a
coordinate based on the country's average longitude and latitude coordinates since the
work hour data do not contain any geographical information. The collated data is
transformed to GeoJson.
• Global administrative boundaries Shapefile is downloaded from Opendatasoft, joined
with work hour data, and uploaded to Mapbox as a tileset for customizing the base map.

### Visualization 
The visualization is built on Html and javascript to develop an interactive map.
• A customized Mapbox base map is firstly added to the Html file. The country boundaries
tileset are colored according to each country's "region " property in work hour data. For
those countries with no data, grey color is used. For visualizing purposes to emphasize
the country, I adjust the transparency of ocean labels and use a very light color for the
ocean.
• Then is to add the work hour layer on the map. The initial page is a cluster map, which
shows how many countries with data are in the cluster: the cluster size and color changes
at different levels of the number of counts. The clusters can click to zoom in to that area
a little bit.
• After zooming in, I use circles to represent the annual average work hours per worker.
Circle size and color vary from different levels of work hours. Larger circles and deeper
colors represent the countries with longer average work hours. (Note: I choose a set of
gradient blue colors for these circles, the color difference may not be conspicuous but
hopes to achieve a subtle visual effect). Considering some circles are overlapped, I lower
the circle opacity.
• Continuing zoom in, the specific work hour for each country will appear on the circles.
• A slider is set to allow the audience to change the year. The circle size and value will also
change to the selected year when dragging the slider to a specific year.
• A stacked line chart created by Echart for average work hours in each region tries to give
the audience a macroscopical comparison across time and regions.
