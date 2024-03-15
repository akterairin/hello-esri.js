# hello-esri.js

<html>
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="initial-scale=1, maximum-scale=1, user-scalable=no" />
    <title>ArcGIS Maps SDK for JavaScript Tutorials: Display a map</title>

    <style>
      html,
      body,
      #viewDiv {
        padding: 0;
        margin: 0;
        height: 100%;
        width: 100%;
      }
    </style>

    <link rel="stylesheet" href="https://js.arcgis.com/4.29/esri/themes/light/main.css">
    <script src="https://js.arcgis.com/4.29/"></script>

    <script>
      require(["esri/config", "esri/Map", "esri/views/MapView"], function(esriConfig, Map, MapView) {

        esriConfig.apiKey = "AAPKacbc03aeb64248229c85810ce9f22ce7RC4SiHjeE1hD_QTL2MVmvDjYBkU3xDiPD-mG3iL_EtnPjbpwIMT86F2d2LLQZDue";

        const map = new Map({
          basemap: "arcgis/topographic" // basemap styles service
        });

        const view = new MapView({
          map: map,
          center: [-118.805, 34.027], // Longitude, latitude
          zoom: 13, // Zoom level
          container: "viewDiv" // Div element
        });

      });
    </script>

  </head>
  <body>
    <div id="viewDiv"></div>
  </body>
</html>
