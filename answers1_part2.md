2. GDAL/OGR
2.1 Retrieving information about the DEM files

$gdalinfo <Dateiname>

N45E014.hgt:
1) EPSG: 4326
2) File Format: .hgt
3) Resolution: 3601x3601 pixel x pixel

n45_e013_1arc_v3.tif:
1) EPSG: 4326
2) File Format: TIF-Datei
3) Resolution: 3601x3601 pixel x pixel

2.2 Creating a raster mosaic

Mithilfe von $gdal_merge -o dem_merge.tif n45_e013_1arc_v3.tif N45E014.hgt und  $gdalbuildvrt dem_buildvrt.vrt n45_e013_1arc_v3.tif N45E014.hgt kann man die genannten 
Dateien zusammenfügen (mergen). Allerdings muss man bei gdalbuildvrt aufpassen, da gdalbuildvrt heterogene Farbenbänder-Interpretation nicht unterstützt und nur graue Bänder akzeptiert.
Der Raster-Layer, der mit gdal_merge erzeugt worden ist, ist schärfer bzw. detaillierter und umfasst eine größere Fläche als der Raster-Layer mit gdalbuilvrt.


