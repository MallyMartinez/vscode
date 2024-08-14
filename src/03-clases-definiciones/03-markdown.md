# Consejos
```
command + P : Abrir la vista previa de Markdown
command + P : Abrir la vista previa de Markdown al lado

Ctrl + P : Abrir la vista previa de Markdown
Ctrl + P : Abrir la vista previa de Markdown al lado
```


# Dillinger

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Estado de la compilación](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Dillinger es un editor de Markdown HTML5, preparado para la nube, compatible con dispositivos móviles, con almacenamiento sin conexión, y potenciado por AngularJS.

  - Escribe algo en Markdown en la izquierda
  - Ve HTML en la derecha
  - Magia

# ¡Nuevas Funciones!

  - Importa un archivo HTML y observa cómo se convierte mágicamente en Markdown
  - Arrastra y suelta imágenes (requiere que tu cuenta de Dropbox esté vinculada)

También puedes:
  - Importar y guardar archivos desde GitHub, Dropbox, Google Drive y One Drive
  - Arrastrar y soltar archivos Markdown y HTML en Dillinger
  - Exportar documentos como Markdown, HTML y PDF

Markdown es un lenguaje de marcado ligero basado en las convenciones de formato que las personas usan naturalmente en el correo electrónico. Como [John Gruber] escribe en el [sitio de Markdown][df1]:

> El objetivo de diseño principal para la sintaxis de formato de Markdown
> es hacerlo lo más legible posible. La idea es que un documento
> en formato Markdown debería ser publicable tal cual, como texto plano,
> sin que parezca que ha sido marcado con etiquetas o instrucciones de formato.

¡Este texto que ves aquí está *realmente* escrito en Markdown! Para familiarizarte con la sintaxis de Markdown, escribe algo de texto en la ventana de la izquierda y observa los resultados en la derecha.

### Tecnología

Dillinger utiliza varios proyectos de código abierto para funcionar correctamente:

* [AngularJS] - ¡HTML mejorado para aplicaciones web!
* [Ace Editor] - impresionante editor de texto basado en la web
* [markdown-it] - Analizador de Markdown hecho bien. Rápido y fácil de extender.
* [Twitter Bootstrap] - excelente plantilla de interfaz de usuario para aplicaciones web modernas
* [node.js] - I/O basado en eventos para el backend
* [Express] - rápido framework para aplicaciones de red en node.js [@tjholowaychuk]
* [Gulp] - el sistema de construcción por streaming
* [Breakdance](http://breakdance.io) - Convertidor de HTML a Markdown
* [jQuery] - duh

Y, por supuesto, Dillinger en sí es de código abierto con un [repositorio público][dill] en GitHub.

### Instalación

Dillinger requiere [Node.js](https://nodejs.org/) v4+ para ejecutarse.

Instala las dependencias y las dependencias de desarrollo y luego inicia el servidor.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

Para entornos de producción...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

# Plugins
Dillinger se extiende actualmente con los siguientes plugins. Las instrucciones sobre cómo usarlos en tu propia aplicación están enlazadas a continuación.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| Github | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |


### Desarrollo

¿Quieres contribuir? ¡Genial!

Dillinger utiliza Gulp + Webpack para un desarrollo rápido.
Haz un cambio en tu archivo y ve instantáneamente tus actualizaciones.

Abre tu Terminal favorita y ejecuta estos comandos.

Primera pestaña:
```sh
$ node app
```

Segunda pestaña
```sh
$ gulp watch
```

(opcional) Tercera pestaña:
```sh
$ karma test
```
#### Construyendo desde la fuente
Para lanzamiento en producción:
```sh
$ gulp build --prod
```
Generando archivos zip preconstruidos para distribución:
```sh
$ gulp build dist --prod
```
### Docker
Dillinger es muy fácil de instalar y desplegar en un contenedor Docker.

Por defecto, Docker expondrá el puerto 8080, así que cambia esto en el Dockerfile si es necesario. Cuando estés listo, simplemente usa el Dockerfile para construir la imagen.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```
Esto creará la imagen de Dillinger y descargará las dependencias necesarias. Asegúrate de reemplazar ${package.json.version} con la versión actual de Dillinger.

Una vez hecho, ejecuta la imagen Docker y mapea el puerto al que desees en tu host. En este ejemplo, simplemente mapeamos el puerto 8000 del host al puerto 8080 del Docker (o el puerto que esté expuesto en el Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Verifica la implementación navegando a la dirección de tu servidor en tu navegador preferido.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

Consulta [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)


### Tareas pendientes
- Escribir MÁS pruebas
- Agregar modo nocturno

Licencia
----

MIT


**Software libre**

