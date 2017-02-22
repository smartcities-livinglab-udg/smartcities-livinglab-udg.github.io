---
layout: post
title:  "SmartCheckIn"
date:   2017-02-22 14:27:16 -0600
categories: Livinglab Web Checkin
---
* this line won't be rendered
{:toc}

# Smart Check In

Proyecto para Smart Check In del CICI en CUCEA

## Instalación
Es necesario contar con Python2.7, pip, npm y bower instalado.<br>
Las bases de datos necesarias son PostgreSQL y MongoDB, para conectar a Python con PostgreSQL (`$ sudo apt-get update & sudo apt-get install -y postgresql postgresql-contrib`) es necesario tener instalado `python-psycopg2`, además del motor de geometría `postgis`.<br>
Además se puede usar `virtualenv`

{% highlight bash %}
$ sudo apt-get install python-psycopg2 libpq-dev postgis
{% endhighlight %}

Ahora es necesario crear un usuario y una base de datos:
> El nombre de la base de datos y el usuario tienen que estar en minúsculas, ejemplo db: `prueba_flask` usuario: `mi_usuario`, y de igual manera en el archivo de configuración.

{% highlight bash %}
$ sudo -u postgres psql postgres
{% endhighlight %}

{% highlight psql %}
postgres=# CREATE DATABASE tu_base_de_datos;
postgres=# CREATE ROLE nombre_usuario LOGIN PASSWORD 'tu_password';
postgres=# GRANT ALL PRIVILEGES ON DATABASE tu_base_de_datos TO nombre_usuario;
postgres=# \q
{% endhighlight %}

{% highlight bash %}
$ sudo -u postgres psql tu_base_de_datos
{% endhighlight %}

{% highlight psql %}
tu_base_de_datos=# CREATE EXTENSION postgis;
tu_base_de_datos=# \q
{% endhighlight %}

Ahora se tiene que editar el archivo ```app/config_sample.py```, y cambiar los datos de la base de datos que nosotros creamos, y lo guardamos como ```app/config.py```.


Después es necesario instalar las dependencias:

{% highlight bash %}
$ npm install
$ virtualenv env
$ source env/bin/activate
(env) $ pip install -r requirements.txt
{% endhighlight %}

Por último se corre la aplicación, se pueden ver las opciones de ejecución con el siguiente comando:

{% highlight bash %}
$ python run.py -h
usage: run.py [-h] [--debug DEBUG] [--host HOST] [--port PORT] [--threaded THREADED]

optional arguments:
  -h, --help            show this help message and exit
  --debug DEBUG, -d DEBUG
                        True if you want to debug your app
  --host HOST, -H HOST  The host where you want to run your app
  --port PORT, -p PORT  The port where you want to serve your app
  --threaded THREADED, -t THREADED
                        Only in developer mode
{% endhighlight %}
