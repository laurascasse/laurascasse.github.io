<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>Display a map with a custom style</title>
<meta name="viewport" content="initial-scale=1,maximum-scale=1,user-scalable=no">
<link href="https://api.mapbox.com/mapbox-gl-js/v2.9.2/mapbox-gl.css" rel="stylesheet">
<script src="https://api.mapbox.com/mapbox-gl-js/v2.9.2/mapbox-gl.js"></script>
<style>
body { margin: 0; padding: 0; }
#map { position: absolute; top: 0; bottom: 0; width: 100%; }
.map-overlay {
  position: absolute;
  width : 200px;
  height: 80px;
  bottom: 0;
  right: 0;
  background: #fff;
  margin-right: 10px;
  font-family: Arial, sans-serif;
  #overflow: auto;
  border-radius: 5px solid black;
}

#features {
  top: 0;
  height: 80px;
  margin-top: 5px;
  width: 200px;
}

#legend {
  padding: 10px;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.1);
  line-height: 18px;
  height: 150px;
  margin-bottom: 40px;
  width: 100px;
}

.legend-key {
  display: inline-block;
  border-radius: 20%;
  width: 10px;
  height: 10px;
  margin-right: 5px;
}
</style>
</head>
<body>
<div id="map"></div>
<div class='map-overlay' id='features'><h4>Densité des annonces AirBNB dans les Alpes-Maritimes</h3>
<div id='pd'><p></p></div></div>
<div class='map-overlay' id='legend'></div>
<script>
	mapboxgl.accessToken = 'pk.eyJ1IjoibGF1cmFjb3N0YTIiLCJhIjoiY2thN3Ztanh3MDR2YTJwc2J3MTJmbnQ5YyJ9.77hloQ92nEIx0XgL-f7N7Q';
const map = new mapboxgl.Map({
container: 'map', // container ID
style: 'mapbox://styles/lauracosta2/cl6op0e7s003215mgoml32w05', // custom style url from https://studio.mapbox.com/
center: [7.02, 43.7], // starting position
zoom: 10,
pitch : 65 // starting zoom
});
</script>
 
</body>
</html>
