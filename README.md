# Prueba

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.1.1.
Archivos necesarios para la imagen son 
.dockerignore
Dockerfile
en el archivo dockerfile fijarse en la linea:

COPY --from=builder /ng-app/dist/prueba /usr/share/nginx/html

En esta linea deben cambiar el comando "prueba" por su proyecto en angular para enviarlo a docker


luego de los archivos son los pasos de correr docker
Nota: se omite la instalacion de docker ya que dependen del sistema operativo, en windows solicitara habilitar hyper-v
Paso 1. comando 1 
Dentro de la carpeta deben realizar lo siguiente:
$docker build -t prueba .
donde "prueba" es la carpeta creada como proyecto de angular, esto genera la imagen docker :)

Paso 2 comando 2
$docker run -p 8080:80 prueba
con este comando ustedes pueden correr la imagen docker esto levantara el nginx (servidor) en http://localhost:8080 --> exito!!
