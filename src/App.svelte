<script>
  import maplibregl from "maplibre-gl";
  import "maplibre-gl/dist/maplibre-gl.css";
  import { onMount } from "svelte";

  onMount(() => {
    const map = new maplibregl.Map({
      container: "map",
      style: "https://demotiles.maplibre.org/globe.json",
      center: [0, 0],
      zoom: 2,
    });

    return () => map.remove();
  });
</script>

<section id="center">
  <div>
    <h1>Kamloops Rooftop Solar Resources</h1>
    <p>This tool is to let you explore and check out what we got!</p>
  </div>
</section>

<section id="next-steps">
  <div id="map"></div>
</section>
