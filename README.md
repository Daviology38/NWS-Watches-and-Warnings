# NWS Watches and Warnings
 Python program to grab and plot current NWS watches and warnings for regions of the U.S. and the continental U.S.

This program uses the NWS API service to grab the current active watches, warnings, and advisories for the continental United States. These advisories are then plotted either using the geometry provided within the alert from the NWS API or using geometry created from the NWS county/watch are shapefile (which is provided here and can be found on the NWS website). 

This program uses the existing awips-python package to import the awips colors for each watches/warnings/advisory type to make these maps as close as possible to the NWS ones.

The continental U.S. map only shows colors as the legend would be difficult with so many entries. Each regionalized map contains the legend for each area. 

# Example Images

![ContinentalUSExample](/example_images/continentalus.png)

![RegionalNEExample](/example_images/ne.png)

# Extending the program with Bokeh and Geoviews/Holoviews

There is also a notebook available that coincides with the python script. The script itself just create the plain images with the keys for each region and the overall continental U.S. map.

The notebook shows this process as well, but also extends the program using geoviews, holoviews, and bokeh to make the main continental U.S. graphic interactive. This will allow the user to hover over a shaded region on the map to see the specific heading, warning/watch issue times, and a description of the warning/watch that was issued. This graphic can be saved to a file and embedded in a personal web page, more information on that can be found in the geoviews/holoviews documentation.

This method can also be extended for each of the regional areas, however that is not shown in the notebook. The process would be similar, but the DataFrame containing all the information would need to be grouped by region rather than removing the regional take outright. Then you can perform the rest of the script for each group.
