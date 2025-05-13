### Examen Final Docker
## Autor: Juan Josè Arango Ocampo
## Descripción

Este trabajo se basa en el desarrollo de una aplicación web sencilla y fácilmente ampliable, construida utilizando Python y el framework Flask, y desplegada dentro de un contenedor Docker. Su propósito es mostrar de forma práctica los conocimientos adquiridos en la asignatura de Telemática, con especial énfasis en la utilización de tecnologías de contenedores para la implementación de servicios en la web.

## Herramientas y Tecnologías Empleadas

-Versión de Python: 3.10
-Framework de desarrollo web: Flask
-Virtualización de entornos: Docker
-Diseño del lado del cliente: HTML5 y CSS3 (hojas de estilo integradas en index.html)
-Plataforma del sistema operativo: Ubuntu 22.04
-Entorno de despliegue: Instancia EC2 en Amazon Web Services
-Control de versiones y alojamiento del código: GitHub


## Requisitos

Tener Docker instalado

Tener Git  instalado

##  Estructura Del Proyecto
<div style="display: flex; gap: 10px;">
    <img src="https://i.imgur.com/sUeuFwa.png" alt="Captura de la app" width="300"/>
    <img src="https://i.imgur.com/rT9RRwQ.png" alt="Captura de la app 2" width="300"/>
    <img src="https://i.imgur.com/qxaISyl.png" alt="Captura de la app 3" width="300"/>
</div>


## Instrucciones De Despliegue:
## Instalación

## 1. Clona este repositorio en tu maquina local:
```bash
git clone https://github.com/JuanAgogoo/Telem-tica
```

## 2. Entramos a Telem-tica
```bash
cd Telem-tica
```

## 3. Construimos la imagen Docker con el siguiente comando:
```bash
sudo docker build -t examenfinal:01 .

```

## 4. Ejecutamos el Contenedor:

```bash
sudo docker run -d -p 80:80 examenfinal:01
```

## 5. Comprobamos si se creò

```bash
sudo docker ps
```
## 6. Entramos a la aplicación con la ip publica

```bash
http://ip publica
```

## ¿Cómo lo modificamos?

- **Modificamos el contenido o el diseño fácilmente editando los siguientes archivos:**

    - **app/templates/index.html: Cambiamos el contenido HTML de la página.**


## Hay que parar el contenedor anterior
```bash
docker stop container id
```

## Posteriormente lo borramos
```bash
docker rm container id
```
##  Procedemos a Re-construir la imagen:

```bash
sudo docker build -t examenfinal:01 .
```
## Acà tenemos que volver a ejecutar el contenedor:

```bash
sudo docker run -d -p 80:80 examenfinal:01
```
