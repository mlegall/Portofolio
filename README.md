<meta charset="utf-8">
<head>
	<style>
	</style>
	
Bienvenu !

Vous trouverez ici la présentation de différents projets que j'ai pu réaliser durant mes études ou bien lors d'expériences professionnelles.
</head>

<body>
<script src="//d3js.org/d3.v3.min.js"></script>
<script src="./myVoronoi.js"></script>
  
<script src="https://unpkg.com/leaflet@1.0.3/dist/leaflet.css"></script>
<script src="https://unpkg.com/leaflet@1.0.3/dist/leaflet-src.js"></script>
 <!-- Make sure you put this AFTER Leaflet's CSS -->
<script src="https://unpkg.com/leaflet@1.3.1/dist/leaflet.js"
   integrity="sha512-/Nsx9X4HebavoBvEBuyp3I7od5tA0UzAxs+j83KgC8PU0kgB4XiK4Lfe4y4cgBtaRJQEIFCW+oC506aPT2L1zw=="
   crossorigin=""></script>

<h1>Parcours</h1>
<div id="map" style="width:300px; height:120px; overflow:auto; border:solid 1px black;"></div>
<script>//EDUCATION
var Cursus = L.layerGroup();

L.circleMarker([48.117232,-1.6734248], {
    color: '#3399ff',
    fillColor: '#3399ff',
   fillOpacity: 0.5,
    radius: 5,
    stroke: false
}).bindPopup("2008-2011, Baccalauréat S, Lycée Jean Macé").addTo(Cursus);

L.circleMarker([51.442749,-0.2208968], {
    color: '#3399ff',
    fillColor: '#3399ff',
   fillOpacity: 0.5,
    radius: 5,
    stroke: false
}).bindPopup("2012, ESOL program, South Tames College").addTo(Cursus),

L.circleMarker([48.1176084,-1.6661783], {
    color: '#3399ff',
    fillColor: '#3399ff',
   fillOpacity: 0.5,
    radius: 5,
    stroke: false
    }).bindPopup("2012-2014, Licence 2 Maths-Eco, Université de Rennes 1").addTo(Cursus),
    
L.circleMarker([48.5790692,7.7642658], {
    color: '#3399ff',
    fillColor: '#3399ff',
   fillOpacity: 0.5,
    radius: 5,
    stroke: false
    }).bindPopup("2014-2017, Master Démographie, Université de Strasbourg").addTo(Cursus),
    
L.circleMarker([48.0506619,-1.7440317],{
    color: '#3399ff',
    fillColor: '#3399ff',
   fillOpacity: 0.5,
    radius: 5,
    stroke: false
    }).bindPopup("2017-2018, MSc Statistics for Smart Data, Ecole Nationale de la Statistique et de l'Analyse de l'Information").addTo(Cursus);

//STAGES
var Stages = L.layerGroup();
L.circleMarker([45.5368285,-73.600919], {
    color: 'orange',
    fillColor: 'orange',
   fillOpacity: 0.5,
    radius: 5,
    stroke: false
}).bindPopup("2016(2mois), Stagiaire recherche, Département Urbanisation culture et Société, Institut Nationale de la Recherche Scientifique").addTo(Stages);

L.circleMarker([48.0925856,-1.6782827], {
    color: 'orange',
    fillColor: 'orange',
   fillOpacity: 0.5,
    radius: 5,
    stroke: false
}).bindPopup("2017(6mois), Stagiaire Démographe, Agence D' Urbanisme et de Développement Intercommunal de l'Agglomération Rennaise").addTo(Stages);

L.circleMarker([48.7154456,2.1916126], {
    color: 'orange',
    fillColor: 'orange',
   fillOpacity: 0.5,
    radius: 5,
    stroke: false
    }).bindPopup("2018(6mois), \\ Stagiaire chargée d'études quantitatives, Groupe de Recherche en Energie Technologie et Société, Département Innovation Commerciale Analyse du Marché et de son Envrionnement").addTo(Stages);
    
//EXPERIENCES PROFESSIONNELLES
//EDUCATION
var Experiences = L.layerGroup();

L.circleMarker([45.0686083,-1.1514688], {
    color: '#00cc66',
    fillColor: '#00cc66',
    fillOpacity: 0.5,
    radius: 5,
    stroke: false
}).bindPopup("Serveuse Plongeuse").addTo(Experiences);

L.circleMarker([51.5287718,-0.2416817], {
    color: '#00cc66',
    fillColor: '#00cc66',
    fillOpacity: 0.5,
    radius: 5,
    stroke: false
}).bindPopup("Jeune fille Au-pair").addTo(Experiences);

L.circleMarker([41.6510923,8.8549785], {
    color: '#00cc66',
    fillColor: '#00cc66',
    fillOpacity: 0.5,
    radius: 5,
    stroke: false
}).bindPopup("Vendeuse de Glaces").addTo(Experiences);

L.circleMarker([48.8500824,-3.017588], {
    color: '#00cc66',
    fillColor: '#00cc66',
    fillOpacity: 0.5,
    radius: 5,
    stroke: false
}).bindPopup("Serveuse").addTo(Experiences);

L.circleMarker([48.5692059,7.6920542], {
    color: '#00cc66',
    fillColor: '#00cc66',
    fillOpacity: 0.5,
    radius: 5,
    stroke: false
}).bindPopup("Agent Recenseur").addTo(Experiences);

L.circleMarker([48.5807445,7.7465913], {
    color: '#00cc66',
    fillColor: '#00cc66',
    fillOpacity: 0.5,
    radius: 5,
    stroke: false
}).bindPopup("Serveuse").addTo(Experiences);
    
//CREATION CARTO
var map = L.map("map", {
		layers: [Cursus, Stages, Experiences],
    center: [46.8013913,-31.0235914]
    });
    
var overlays = {
    "Cursus": Cursus,
    "Stages": Stages,
    "Experiences": Experiences
};

L.control.layers(null,overlays, {collapsed: false}).addTo(map);

L.tileLayer('https://cartodb-basemaps-{s}.global.ssl.fastly.net/light_nolabels/{z}/{x}/{y}{r}.png', {
	subdomains: 'abcd'
}).addTo(map);
</script>

</body>
