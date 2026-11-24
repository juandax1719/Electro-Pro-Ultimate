# Electro Pro — PWA v3.5

Aplicación web progresiva (PWA) preparada para publicarse en GitHub Pages. Incluye proyectos BT/MT en pestañas independientes y una interfaz adaptable a móviles.

## Novedades v3.5
- Selector de tipo de proyecto al crear: BT o MT.
- Pestañas para alternar entre proyectos abiertos; los proyectos permanecen agrupados en pestañas y se puede alternar entre ellos sin cerrar el trabajo anterior.
- En proyectos MT solo se habilitan Resumen, Datos del proyecto, Media tensión y SPT (puesta a tierra y diseño de malla).
- Interfaz móvil mejorada: pestañas desplazables, formularios táctiles y tablas con desplazamiento horizontal.

## Archivos
- `index.html`: aplicación Electro Pro.
- `manifest.webmanifest`: nombre, iconos y configuración de instalación.
- `sw.js`: service worker y caché para uso sin conexión (caché v3.5).
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`: iconos de la aplicación.

## Publicar en GitHub Pages
1. Crea un repositorio en GitHub (por ejemplo, `electro-pro`).
2. Sube **todos los archivos de esta carpeta** a la raíz del repositorio.
3. En GitHub abre **Settings → Pages**.
4. En **Build and deployment**, selecciona **Deploy from a branch**.
5. Selecciona la rama `main` y la carpeta `/ (root)`, luego guarda.
6. Espera a que GitHub Pages publique el sitio. La dirección será similar a:
   `https://TU-USUARIO.github.io/electro-pro/`
7. Abre esa dirección en Chrome. En Android usa el menú ⋮ → **Instalar aplicación** o **Agregar a pantalla principal**.

## Importante
- La instalación PWA requiere HTTPS. GitHub Pages entrega HTTPS automáticamente.
- No cambies los nombres ni las rutas relativas de `manifest.webmanifest`, `sw.js` y los iconos.
- La primera visita necesita conexión para descargar la aplicación. Después, el service worker conserva los archivos principales para abrirla sin conexión.
- Los proyectos se guardan en el almacenamiento local del navegador/dispositivo. Para moverlos entre dispositivos, usa Exportar/Importar proyecto.
- Esta versión corrige defectos estructurales y de robustez detectados en una revisión estática. No constituye una certificación de los cálculos eléctricos ni reemplaza pruebas funcionales y contraste normativo en terreno.

## Actualizar la aplicación
Cuando publiques una versión nueva, cambia el valor de `CACHE_NAME` en `sw.js` para forzar la renovación de caché.


## Pruebas adicionales de v3.5
- Se corrigió la persistencia de pestañas abiertas.
- Se agregó cierre de pestaña sin borrar el proyecto guardado.
- Se aisló por proyecto el ingreso rápido de Wenner y electrodo vertical.
- Se incorporó el formateador numérico usado por los módulos de cálculo.


Actualización v3.6: se renovó el icono de Electro Pro, se añadieron iconos maskable independientes para Android y se actualizó la caché del service worker para forzar la carga de los nuevos recursos.


Versión 3.7 corregida: se conserva íntegra la lógica funcional de v3.6. Se actualizan iconos, colores del manifiesto y pantalla de inicio. La pantalla de inicio se inserta al final del documento y no modifica funciones ni cadenas de exportación.
