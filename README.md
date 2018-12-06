> Incluir aquí las medallas de Waffle y Travis.

[![Waffle.io - Columns and their card count](https://badge.waffle.io/fede9612/prevencion-acoso.svg?columns=backlog)](https://waffle.io/fede9612/prevencion-acoso)
[![Build Status](https://travis-ci.com/fede9612/prevencion-acoso.svg?branch=master)](https://travis-ci.com/fede9612/prevencion-acoso)

# Prevención acoso

## Software necesario

Explicar aquí cómo instalar lo siguiente:
* JDK 1.8
  1.Ejecutamos la consola y escribimos el siguientes comandos
  ```console
  root@root:~$ sudo add-apt-repository ppa:webupd8team/java
  root@root:~$ sudo apt-get update
  root@root:~$ sudo apt-get install oracle-java8-installer
  ```
  2.En la instalación java instala un paquete de configuración pero para mejor seguridad de que sea instalado ejecutaremos
  ```console
  root@root:~$ sudo apt-get install oracle-java8-set-default
  ```
  3.Y finalmente para comprobar que java 8 está instalado ejecutaremos
   ```console
  root@root:~$ java -version
  
  java version "1.8.0_191"
  Java(TM) SE Runtime Environment (build 1.8.0_191-b12)
  Java HotSpot(TM) 64-Bit Server VM (build 25.171-b12, mixed mode)
  ```
  
* Maven

 1. Iremos al [enlace](https://maven.apache.org/download.cgi) y descargaremos Maven.
  
  2. Descomprimimos el archivo y ejecutamos los siguientes comandos
  ```console
    root@root:~$ sudo mv ~/Downloads/apache-maven-3.3.9 /opt
    root@root:~$ sudo gedit /etc/bash.bashrc
  ```
   Al final del archivo añadir las siguientes líneas
  ```console
    export MAVEN_HOME=/opt/apache-maven-3.3.9
    export M2_HOME=/opt/apache-maven-3.3.9
    export PATH=$PATH:$M2_HOME/bin
  ```
   Cerramos el archivo
  
  3. Finalmente ejecutaremos lo siguiente para ver si se instaló correctamente
   ```console
    mvn -version
  ```
* MySQL
* Eclipse

## Configuración del entorno

Explicar aquí cómo hacer lo siguiente:
* Crear la base de datos.
* Cargar los datos iniciales.
* Importar el proyecto en Eclipse.

## Hacer funcionar la aplicación desde consola Linux
 1. Abrimos una consola situados en el directorio donde tenemos nuestro proyecto.
 1. Escribimos mvn jetty:run para iniciar el server y visualizar la página en la url localhost:8080
 1. Para detener el server precionamos `Ctrl + c`
 
