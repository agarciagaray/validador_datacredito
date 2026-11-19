# Validador de Archivos Planos DataCrédito

Herramienta web para validar archivos planos de reporte de información a DataCrédito/Experian Colombia, según el Manual de Entrega de Información Cartera LHD v2.2 (2023-06-03).

## ¿Qué hace?

Recibe un archivo plano `.txt` con formato `SSSSSS.AAAAMMDD.T` y valida que cumpla con la estructura, longitudes, catálogos y reglas de negocio definidas en el manual. Devuelve un informe técnico de auditoría con los hallazgos clasificados por tipo de error.

## Instalación

No requiere instalación. Es un archivo HTML autocontenido con CSS y JavaScript. Funciona 100% en el navegador, sin servidor, sin dependencias, sin Node.js.

### Requisitos

- Navegador moderno (Chrome 80+, Firefox 75+, Edge 80+, Safari 13+)
- JavaScript habilitado

## Cómo usarlo

### Opción 1: Abrir directamente

1. Descarga el archivo `validador-datacredito.html`
2. Haz doble clic para abrirlo en tu navegador
3. Arrastra tu archivo `.txt` a la zona de carga o haz clic para seleccionarlo
4. Espera a que termine el procesamiento (verás la barra de progreso)
5. Revisa los resultados en las pestañas de resumen y detalle
6. Descarga el informe en el formato que necesites (Markdown, CSV o HTML)

### Opción 2: Servir desde un servidor local

Si prefieres no abrir el archivo directamente (algunos navegadores bloquean ciertas funciones al abrir archivos locales), puedes servirlo con cualquier servidor estático:

```bash
# Con Python 3
python -m http.server 8000

# Con Node.js (requiere http-server global)
npx http-server -p 8000

# Con PHP
php -S localhost:8000