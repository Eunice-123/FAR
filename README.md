# Floor to area ratio calculation in qgis 
- Get DSM data
- Get DTM data
- Download OSM data for all buildings in selected parcel
- Using Quick OSM plugin , download building footprint data that fall under
- Houses
- Commercial
- Apartments
- Hotel( built
- levels underground)
- Retail
- Industrial
- Alternatively download layers for yes
- Reclassify downloaded buildings into
-	Residential
- Commercial
  
- Preprocessing and correction
- Building data retrieved from OSM is corrected in QGIS by
- 	Editing boundaries by cross referencing with different base maps: google, bing, Mapbox
- 	Editing attributes of scraped data
-	Adding buildings that were not captured in scraped data
- Calculate height using DSM-DTM
- Adding height to scraped footprint data
- Attach height data from clipped height results to building data Perform zonal statistics for building data by:Setting raster layer as results from the clipped height
  Setting buildings as vector layer containing zones
- Checking MIN, MAX and
 # MEAN as statistics to compute
- Get Normalized DSM by removing noise by removing height for vehicles and vegetation, i.e.,non-building data Vegetation is removed by NDVI Other noise like vehicle, pole etc. are 
  filtered - as well
- The height of building to be used, roof level inclusive or exclusive
- Average number of floors – area
  
# Consideration
-	When average number of floors is used, what happens to the surplus, is it rounded or ignored?
-	Should total FAR be based on all buildings combined or buildings separated into different classes i.e., Total FAR = FAR (residential) + FAR (commercial)?
-	Should a constant number be used as average number of floors for every (parcel) or different averages must be used used?
-	Height of building – roof level inclusive or exclusive
-	Getting data from a spatial planning authority from a country. Essentially, data should provide number of floors for every building or average number of floors for an area.

  
