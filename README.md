# Plantilla de base PUG con SCSS (SASS), Bootstrap y Font Awesome incluido para mockups
Esta plantilla está preconfigurada para ser usada en mockups, usando Bootstrap con Font Awesome, configurando con SASS y como pre procesador de html está usando pug.
## Cambios Bootstrap
Se inicia con Bootstrap, no se toca, se configurará con SASS
## Cambios con SASS
Se relaciona un custom para importar las herramientas de Bootstrap, ejemplos de modificación de fuentes base, componentes creados y colores mapeados junto con un estilo simple de ejemplo y un estilo sobre escribiendo la salida de bootstrap de un componente.
## Integración a pug
Se ha generado la integración con pug de manera básica, pero se estima que tendrá mixins y partials creado de ejemplo, con un html base simple que sirva como guía.
## A futuro
Espero poder integrar con un nano css o similar para minificar el css usado resultado de SASS - Actualizado desde Vs Code
## Comandos 
En el archivo package.json existen por ahora estos comandos.
### Vigila-Pug
Este comando toma pug como comando cli , le dice que vigile la carpeta src y lo envía a la carpeta dist, en formato "bonito" con -P  y se queda vigilando con -w watch.
### Vigila-Sass
También usa un comando cli o puede ser parte del proceso - junto con pug - y analiza los scss del directorio src y los lleva a estilos css, se queda vigilando con -w watch.
### LimpiaCss
Toma purge como cli y como dependencia, se va a la carpeta dist/css/estilos.css (archivo que previamente entrega sass), vigila el contenido que está tipo html en la carpeta dist y de salid entrega un css optimizado en la carpeta dist/css/optimizado - no lo he puesto en modalidad watch, prefiero que se ejecute manualmente antes de empaquetar.