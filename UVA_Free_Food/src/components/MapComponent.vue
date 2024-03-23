<template>
    <div id="map" style="height: 400px;"></div>
  </template>
  
  <script>
  import L from 'leaflet';
  
  export default {
    name: 'MapComponent',
    mounted() {
      this.initMap();
    },
    methods: {
      initMap() {
        const map = L.map('map').setView([51.505, -0.09], 13);
  
        L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
          attribution: '© OpenStreetMap contributors'
        }).addTo(map);
      }
    }
  };
  </script>
  