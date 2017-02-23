# Ejemplo

*Sitio de GitHub del Centro de Inovación en Ciudades Inteligentes.*


## Instalación

Para poder correr el sitio de manera local es neceario tener instalado Ruby y las gemas Bundle y Jekyll.

Lo primero que se tiene que hacer es ejecutar el comando:

```bash
$ sudo apt-get install ruby -y
```

Una vez que Ruby se encuentre instalado se tiene que ejecutar

```bash
$ sudo gem install bundle jekyll
```

## Uso

### Correr en local

Lo primero que se tiene que hacer es clonar el repositorio:

```bash
$ git clone https://github.com/smartcities-livinglab-udg/smartcities-livinglab-udg.github.io
$ cd smartcities-livinglab-udg.github.io
```

Una vez que nos encontremos dentro de la carpeta del sitio, ejecutamos:

```bash
$ bundle install
```

Después, para correr el sitio de manera local ejecutamos:

```bash
$ bundle exec jekyll serve --watch
```

### Estructura del proyecto
```
.
+-- _data
|   +-- members.yml
|   +-- projects.yml
+-- _drafts
|   +-- archivos.html
|   +-- archivos.tex
|   +-- archivos.md
+-- _includes
|   +-- footer.html
|   +-- header.html
+-- _layouts
|   +-- default.html
|   +-- post.html
|   +-- page.html
|   +-- home.html
+-- _posts
|   +-- 2017-02-22-SmartCities-CheckIn.markdown
|   +-- 2017-02-23-SmartCities-CheckIn.html
+-- _sass <- Aquí se guardará el tema que se esté utilizando, no es necesario editarlo
+-- _site <- Aquí se generará el sitio, no es necesario editar nada de esta carpeta
+-- assets
|   +-- main.scss
|   +-- projects.scss
+-- img
|   +-- projects
|   |   +-- AppSmartCheckIn
|   |   |   +-- portada.jpg
|   |   +-- OtroProyecto
|   |   |   +-- portada.jpg
|   +-- posts
|   |   +-- 2017-02-22-titulo.jpg
|   |   +-- 2017-02-22-otro-titulo.jpg
|   +-- pages
|   |   +-- Index
|   |   |   +-- portada.jpg
|   |   |   +-- 2017-02-22-otro-titulo.jpg
|   |   +-- About
|   |   |   +-- portada.jpg
|   |   |   +-- 2017-02-22-otro-titulo.jpg
+-- js
|   +-- archivos.js
+-- index.html <- Archivo que cargará la vista principal de la página
+-- about.md <- Se pueden generar páginas tanto en MarkDown como HTML
+-- otra_pagina.html <- Para acceder sería en la ruta /otra_pagina, ejemplo en local sería: localhost:4000/otra_pagina
+-- _config.yml <- Archivo de configuración principal
```

#### _data
Aquí se guardarán los archivos de datos, por ejemplo los miembros de equipos, los proyectos, etc. Más adelante se darán detalles de cómo utilizarse


#### _drafts
Aquí se guardarán los posts no publicados

#### _includes
Aquí se guardarán los archivos comunes para layouts

#### _layouts
Aquí se guardarán los layouts, en caso de que se quiera crear otro tipo de publicación o página, para que después se puedan importar en otros archivos.

#### _posts
Aquí irán los posts, posteriormente se darán detalles de su estructura

#### assets
Aquí se guararán los archivos scss que se vayan necesitando

#### img
Aquí se guardarán las imágenes del sitio. Posteriormente se indicará cómo guardarlas

## License

The theme is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
