# Proyecto de Mapa Sisdai con Nuxt

Este es un proyecto de demostración que integra la librería de componentes geoespaciales de `@centrogeomx/sisdai-mapas` en una aplicación web moderna construida con Nuxt.js (versión 3+).

El objetivo principal es mostrar un mapa interactivo con una capa base y una capa WMS superpuesta, configurado para funcionar correctamente en un entorno de renderizado del lado del servidor (SSR) como Nuxt.

## Características Implementadas

- **Mapa Base**: Se utiliza un mapa base de teselas XYZ por defecto.
- **Capa WMS**: Se superpone una capa de un servicio WMS (Web Map Service) que muestra datos de "tiraderos clandestinos".
- **Renderizado en Cliente**: El mapa se renderiza exclusivamente en el navegador (`client-side`) utilizando la funcionalidad `<client-only>` de Nuxt para asegurar la compatibilidad con librerías que manipulan el DOM como OpenLayers.

## Tecnologías Utilizadas

- **Nuxt.js**: Framework de Vue para aplicaciones web universales.
- **Vue.js**: Framework progresivo de JavaScript.
- **`@centrogeomx/sisdai-mapas`**: Librería de componentes de Vue para la creación de mapas interactivos.
  - **`<SisdaiMapa>`**: Componente contenedor principal del mapa.
  - **`<SisdaiCapaXyz>`**: Componente para la capa base de teselas.
  - **`<SisdaiCapaWms>`**: Componente para la capa de datos WMS.
- **`@centrogeomx/sisdai-css`**: Paquete de estilos para los componentes Sisdai.
- **OpenLayers**: El motor de mapas subyacente que utiliza `sisdai-mapas`.

## Puesta en Marcha

### Prerrequisitos

- [Node.js](https://nodejs.org/) (versión 18 o superior recomendada)
- [npm](https://www.npmjs.com/) (o un gestor de paquetes equivalente)

### Instalación

1. Clona el repositorio (si aún no lo has hecho).
2. Navega al directorio del proyecto.
3. Instala las dependencias:
   ```bash
   npm install
   ```

### Servidor de Desarrollo

Inicia el servidor de desarrollo local. La aplicación estará disponible en `http://localhost:3000`.

```bash
npm run dev
```

### Producción

Para construir la aplicación para un entorno de producción:

```bash
npm run build
```

Para previsualizar la build de producción localmente:

```bash
npm run preview
```