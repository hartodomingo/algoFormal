<template>
  <div>
    <h1>Mapa WMS con Sisdai y Nuxt</h1>
    <p>Mostrando la capa "geonode:tiraderos_clandestinos".</p>

    <!-- Envolvemos el mapa en <client-only> para evitar problemas con SSR -->
    <client-only>
      <div style="height: 60vh; width: 100%; border: 1px solid #ccc;">
        <SisdaiMapa>
          <SisdaiCapaXyz />
          <SisdaiCapaWms
            fuente="https://geonode.dev.geoint.mx/gs/geonode/tiraderos_clandestinos/ows"
            capa="geonode:tiraderos_clandestinos"
            :opacidad="0.7"
          />
        </SisdaiMapa>
      </div>
      <p><em>El mapa puede tardar unos segundos en cargar. Si no aparece, verifica la consola del navegador por posibles errores.</em></p>
    </client-only>
  </div>
</template>

<script setup>
// Importamos los componentes directamente para este ejemplo simple.
// Nuxt los resolverá desde node_modules.
import { SisdaiMapa, SisdaiCapaWms, SisdaiCapaXyz } from '@centrogeomx/sisdai-mapas';
</script>

<style>
/* Estilos globales para la página */
body {
  font-family: sans-serif;
  padding: 1rem;
  background-color: #f4f4f4;
  color: #333;
}

h1 {
  color: #00558c; /* Un color institucional de ejemplo */
}
</style>
