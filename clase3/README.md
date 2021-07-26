# **Resumen Clase 3**

### Imagen
Una imagen es un sistema creado previamente en docker con una serie de instrucciones y comandos

las imagen se crean con un Dockerfile y no pueden ser modificadas

### Contenedor

Un contenedor es como una instancia ejecutandose de una imagen.

## Crear imagen y contenedor en Dockerfile

  - creamos directorio llamado mi-primer-docker-file:
  >$ mkdir mi-primer-docker-file

  - creamos el archivo Dockerfile y dentro de este archivo debemos pegar el archivo RUN

  - De nuevo en nuestra creamos otra nueva llamada tatic-html-directory
  >$ mkdir static-html-directory

  - creamos un archivo html
  >$ nano index.html
  Ya con estos dos archivos y directorios estamos listos para crear nuestro contenedor

  - Basados en una imagen de Docker Hub ejecutamos el comando:
  >$ docker image build -t some-content-nginx .

  - Podemos correr nuestro contenedor y visualizarlo en el puerto 8080
  >$ docker run --name some-nginx -d -p 8080:80 some-content-nginx
  En este caso se habilitó el puerto 80 y se hace un mapeo del puerto 8080 del host al contenedor.

  - Podemos verificar con curl mediante
  >$ curl -k localhost:8080