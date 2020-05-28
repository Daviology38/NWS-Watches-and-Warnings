# NWS Watches and Warnings
 Python program to grab and plot current NWS watches and warnings for regions of the U.S. and the continental U.S.

This program uses the NWS API service to grab the current active watches, warnings, and advisories for the continental United States. These advisories are then plotted either using the geometry provided within the alert from the NWS API or using geometry created from the NWS county/watch are shapefile (which is provided here and can be found on the NWS website). 

This program uses the existing awips-python package to import the awips colors for each watches/warnings/advisory type to make these maps as close as possible to the NWS ones.

The continental U.S. map only shows colors as the legend would be difficult with so many entries. Each regionalized map contains the legend for each area. 
