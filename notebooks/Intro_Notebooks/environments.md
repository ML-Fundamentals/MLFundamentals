# Anaconda Navigator y envs

Desde la terminal de linux o el Anaconda Prompt en windows corremos:

``anaconda-navigator``
## Home
Aquí vemos un listado de las aplicaciones que están integradas en Anaconda. En este curso nos van interesar en particular:
*  Jupyter Notebook o Jupyter Lab
## Environments

### Intro
Un _environment_ es un "contexto" donde tenemos instalado librerías, paquetes y sus dependencias de lenguajes de programación. Estos solucionan un problema muy común en el día a día de usar librerías externas: ** la compatibilidad y dependencias entre paquetes**.

En cada proyecto que uno trabaje es recomendable asignarle **su** environment en donde se incluyan las librerias que se van a usar. Esto permite compartir qué requirimientos tiene nuesto código facilmente y poder reproducir los resultados entre diferentes usuarios.

### Base Environment
Desde Anaconda navigator vamos a la solapa "Environments".  Allí tendremos un listado de los environments creados en nuestra máquina. Si recién instalamos Anaconda sólo tendremos "base(root)".

REMEMBER: **base** es lo que nos aparece en la terminal de linux o el Anaconda prompt indicando que estamos trabajando en ese environment!

En base están todos los paquetes que vienen con Anaconda que son del orden de 400. A veces queremos tener más flexibilidad y trabajar con menos paquetes para que cuando compartimos código no tengamos que instalar librerías innecesarias

### Crear un envoronment

1. Simplemente clickemos el botón con el símbolo "+" que dice Create.
2. Le ponemos nombre Ej Nieve
3. Le decimos que versión de pytho (o/y R) queremos.

Listo
El número de paquetes ahora se redujo a 190. 
####  

 Desde terminal también podemos hacerlo corriendo

``conda create --name Nieve``

En caso de querer una versión en particular de python podemos aclararlo como:

`` conda create -n Nieve python=3.7``
### Activar un environment

Para trabajar en el environment "Nieve" que creamos vamos a la terminal y corremos
``conda activate Nieve``

Ahora vamos a ver que en lugar de "(base)" nuestra terminal muestra "(Nieve)".


### Instalar paquetes en un environment
Para instalar paquetes dentro de un environment simplemente escribimos

``conda install "nombre de paquete``

Anaconda se encargará de incorporarlo en la lista y resolver las dependenciasque tenga con otros paquetes.

### Exportar un environment

Desde navigator seleccionamos el environmente que queremos exportar y tocamos en el boton con la fecha hacia arriba que dice "Backup"



O bien desde terminal escribimos

``conda env export Nieve>Nieve.yml``

El archivo .yml simplemente es un listado con las dependencias y versiones de cada paquete

### Importar un environment (Crear desde .yml)
Desde navigaro tocamos en Import y seleccionamos el archivo .yml

Desde la terminal escribimos 
``conda env create -n Nieve --file Nieve.yml``