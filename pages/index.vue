<template>
<div id='map'></div>
</template>
<script>
  export default {
    mounted () {
      mapboxgl.accessToken = process.env.MAPBOX_TOKEN;
      //mapboxgl.accessToken = MAPBOX_TOKEN;
      this.map = new mapboxgl.Map({
        container: 'map',
        style: process.env.MAPBOX_STYLE,
        center: [139.767125,35.681236],
        zoom: 10
      })
    }
  }
</script>
<style>
body { margin:0; padding:0; }
#map { position:absolute; top:0; bottom:0; width:100%; }
</style>