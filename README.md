# Plantilla de base PUG con SCSS (SASS), Bootstrap y Font Awesome con proceso de Purgecss incluido para mockups
Esta plantilla está preconfigurada para ser usada en mockups, usando Bootstrap con Font Awesome, configurando con SASS y como pre procesador de html está usando pug, además dentro de los comandos se optimiza el css de estilos con purgecss.
## Cambios Bootstrap
Se inicia con Bootstrap, no se toca, se configurará con SASS
## Cambios con SASS
Se relaciona un custom para importar las herramientas de Bootstrap, ejemplos de modificación de fuentes base, componentes creados y colores mapeados junto con un estilo simple de ejemplo y un estilo sobre escribiendo la salida de bootstrap de un componente.
## Plantilla de bootstrap demo
Básicamente es una hoja que permite ver de manera global cómo ha sido afectado bootstrap con SASS - NO es documentación u hoja de estilos documentado.
## Integración a pug
Se ha generado la integración con pug con mixins y partials creado de ejemplo, con un html base simple que sirva como guía.
## Demo de pug
Se generó una página demopug que muestra el uso de mixins y las áreas de contenido
## Uso de awesome font
Debido a que en muchos casos purgecss no optimizará el uso de awesome font ya que este posee javascript que lo menciona y que si se optimiza posteriormente no se podrían usar íconos que no existan previamente, la mejor opción es incluir el paquete completo, al momento de este documento es la 6-4-0 free, decidí no usar el paquete para que se pueda reemplazar si se desea fácilmente.
## A futuro
Usar un empaquetador tipo Parcel y minificar tambien el JS
## Tenga en cuenta
El comando para usar purge minifica y comprime además de limpiar el css, así que una vez listo, se debe volver a generar todas las páginas pug para que tome el arhcivo correcto que está en la carpeta assets/css-optimizado
## Comandos 
En el archivo package.json existen por ahora estos comandos.
### Vigila-Pug
Este comando toma pug como comando cli , le dice que vigile la carpeta src y lo envía a la carpeta dist, en formato "bonito" con -P  y se queda vigilando con -w watch.
### Vigila-Sass
También usa un comando cli o puede ser parte del proceso - junto con pug - y analiza los scss del directorio src y los lleva a estilos css, se queda vigilando con -w watch.
### LimpiaCss
Toma purge como cli y como dependencia, se va a la carpeta dist/css/estilos.css (archivo que previamente entrega sass), vigila el contenido que está tipo html en la carpeta dist y de salida entrega un css optimizado en la carpeta dist/assets/css-optimizado - no lo he puesto en modalidad watch, prefiero que se ejecute manualmente antes de empaquetar, se debería cambiar la url del css en la hoja de Pug para posteriormente enlazar el archivo compactado.