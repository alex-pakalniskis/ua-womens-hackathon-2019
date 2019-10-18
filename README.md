# Workshop Materials for [UA Women's Hackathon 2019](https://womenshackathon.arizona.edu/)

This interactive workshop will introduce participants to the use of Google Colaboratory for analysis and visualization of spatial data. Using this free Google Drive extension, participants will access a cloud-based Jupyter Notebook Python programming environment for a hands-on experience with software libraries such as geopandas, matplotlib, and folium. Participants will learn how to programmatically interact with Google Drive files and create interactive web maps.

Track: Compute

ILC 117

<!DOCTYPE html>
<html>
  <head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <meta name="viewport" content="initial-scale=1, maximum-scale=1, user-scalable=no">
    <title>UA Enterprise GIS</title>
    <link rel="stylesheet" href="https://js.arcgis.com/3.18/esri/css/esri.css">
    <style>
      html, body, #map {height: 100%; width: 100%; margin: 0; padding: 0;}
    </style>
    <script src="https://js.arcgis.com/3.18/"></script>
    <script>
      var map;
      require(["esri/map", "esri/layers/ArcGISTiledMapServiceLayer", "esri/layers/ArcGISDynamicMapServiceLayer", "dojo/domReady!"],
        function(Map, ArcGISTiledMapServiceLayer, ArcGISDynamicMapServiceLayer) {
            map = new Map("map", {  
                center: [-110.953, 32.232], // long, lat of UA Old main
                zoom: 20, 
                logo: false,
            });  
            var campusBaseMap = new ArcGISTiledMapServiceLayer("https://services.maps.arizona.edu/pdc/rest/services/enterprise/MapServer/");
            var interior = new ArcGISDynamicMapServiceLayer("https://services.maps.arizona.edu/pdc/rest/services/InteriorDept/MapServer")
            map.addLayer(campusBaseMap);
            map.addLayer(interior)
        });
    </script>
  </head>
<body>
    <div id="map"></div>
</body>
</html>


[Alex Pakalniskis](https://alexpakalniskis.com)
