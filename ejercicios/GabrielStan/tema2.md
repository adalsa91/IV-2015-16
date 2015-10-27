# Tema 2

### Ejercicio 1

**Instalar alguno de los entornos virtuales de node.js (o de cualquier otro lenguaje con el que se esté familiarizado) y, con ellos, instalar la última versión existente, la versión minor más actual de la 4.x y lo mismo para la 0.11 o alguna impar (de desarrollo).**

Usando **virtualenv** he instalado **nodeenv** y dos otros entornos virtuales para node: **4.2.1** y **0.1.15**.

![virtualenv y nodeenv](https://www.dropbox.com/s/jm2ipw6u5hmy3k7/instalando%20nodejs%20venv.png?dl=1)

Ya que voy a usar Django (**python**) para crear la aplicación, voy a usar el entorno **virtualenv**.

![virtualenv y django](https://www.dropbox.com/s/rxjghtcmjhqhr0v/venv%2Bdjango.png?dl=1)

### Ejercicio 2

**Crear una aplicacion para calificar empresas**

He creado una aplicacion basica usando el framework Django. El codigo se puede ver en el siguiente repositorio de GitHub:

[Ejercicio 2 - Enlace a GitHub](https://github.com/gabriel-stan/tema2-IV)

### Ejercicio 3

**Ejecutar el programa en diferentes versiones del lenguaje. ¿Funciona en todas ellas?**

He creado dos entornos virtuales: no usando **python 2.7.6** y el otro usando **python 3.4.3**, instalando Django en cada uno de ellos. Como se puede ver en la imagen, la aplicacion se ejecuta tanto con python 2 como con python 3.

![ej3](https://www.dropbox.com/s/rg2ox6lyszs1wk5/ejercicio3.png?dl=1)

### Ejercicio 4

**Crear una descripción del módulo usando package.json. En caso de que se trate de otro lenguaje, usar el método correspondiente.**

Siguiendo el [tutorial de empaquetado de aplicaciones para Django](https://docs.djangoproject.com/en/1.8/intro/reusable-apps/#packaging-your-app) (muy parecido al de empaquetado de python), he empaquetado la aplicación de calificaciones (llamada "votos"). 

Primero he movido la aplicación del proyecto, tal y como se puede comprobar, el proyecto Django no funciona:

**$ ./manage.py runserver**

![no funciona](https://www.dropbox.com/s/w3v7cam31klv6ga/no-funciona.png?dl=1)

A continuación, he empaquetado la aplicación:

**$ python setup.py sdist**

![empaquetando](https://www.dropbox.com/s/6nlpf6q8bpxattg/packaging.png?dl=1)

... y he instalado el paquete Django:

**$ pip install django-votos/dist/django-votos-0.1.tar.gz**

![instalando](https://www.dropbox.com/s/bbt7ml60xfal3y3/install-django-votos.png?dl=1)

Como podemos observar, el paquete aparece en la lista de paquetes instalados.

![pip freeze](https://www.dropbox.com/s/shlh1hxix7c5abo/freeze-votos.png?dl=1)

Arrancamos el servidor, y voilà!

![funciona](https://www.dropbox.com/s/ol4eb9ka2bovgrp/funciona.png?dl=1)

El paquete también se puede instalar con todos los demás requisitos usando el comando **pip install -r requirements.txt**. El código se puede ver en github (ver ejercicio 2).

### Ejercicio 5

**Automatizar con grunt y docco (o algún otro sistema) la generación de documentación de la librería que se cree. Previamente, por supuesto, habrá que documentar tal librería.**











