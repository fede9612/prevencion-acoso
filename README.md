> Incluir aquí las medallas de Waffle y Travis.

[![Waffle.io - Columns and their card count](https://badge.waffle.io/fede9612/prevencion-acoso.svg?columns=backlog)](https://waffle.io/fede9612/prevencion-acoso)
[![Build Status](https://travis-ci.com/fede9612/prevencion-acoso.svg?branch=master)](https://travis-ci.com/fede9612/prevencion-acoso)

# Prevención acoso

## Software necesario

* OpenJDK 1.8
 
 1.Ejecutamos la consola y escribimos el siguientes comandos para actualizar el índice de paquetes.
  ```console
  root@root:~$ sudo apt-get update
  ```
  2.Luego ejecutaremos la siguiente linea para realizar la instalación
  ```console
  root@root:~$ sudo apt-get install default-jdk
  ```
  3.Y finalmente para comprobar que java 8 está instalado ejecutaremos
   ```console
  root@root:~$ java -version
  
  java version "1.8.0_191"
  Java(TM) SE Runtime Environment (build 1.8.0_191-b12)
  Java HotSpot(TM) 64-Bit Server VM (build 25.171-b12, mixed mode)
  ```
  
  Para más información acerca de la configuración visite el siguiente [link](https://www.digitalocean.com/community/tutorials/como-instalar-java-con-apt-get-en-ubuntu-16-04-es)
  
* Maven

 1. Ejecutamos la consola y escribimos el siguientes comandos para actualizar el índice de paquetes.
 ```console
 root@root:~$ sudo apt update
 ```
  
  2. Luego instalamos Maven con el siguiente comando
  ```console
  root@root:~$ sudo apt install maven
  ```  
  3. Finalmente ejecutaremos lo siguiente para ver si se instaló correctamente
   ```console
   root@root:~$ mvn -version
   ```
   Mostrará este mensaje
   ```console
    Apache Maven 3.5.2
    Maven home: /usr/share/maven
    Java version: 10.0.2, vendor: Oracle Corporation
    Java home: /usr/lib/jvm/java-11-openjdk-amd64
    Default locale: en_US, platform encoding: ISO-8859-1
    OS name: "linux", version: "4.15.0-36-generic", arch: "amd64", family: "unix"
   ```
* MySQL

  Acceder al siguiente [link](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-16-04) y seguir los pasos.
* Eclipse
  
  Si ya se tiene Java instalado seguir desde el [tutorial](https://websiteforstudents.com/how-to-install-eclipse-oxygen-ide-on-ubuntu-167-04-17-10-18-04/) paso 2, sino empezar desdes el paso 1.

## Configuración del entorno

* Crear la base de datos.

   Crearemos la base de datos accediendo a una consola y entrar el entorno de mysql con `mysql -u nombreDeUsuario -p password`, una vez dentro ejecutamos el comando`create database prevencionAcoso` 
* Cargar los datos iniciales.

  Dentro del IDE Eclipse buscaremos la clase llamada "DataGenerator", encima de ella precionaremos click derecho -> Run as -> Java Application
* Importar el proyecto en Eclipse.

  Dentro del IDE Eclipse nos iremos a File -> Import -> buscamos Existing Maven Projects -> buscamos el directorio donde se encuentra nuestro repo, lo seleccionamos y presionamos Finish.

## Hacer funcionar la aplicación desde consola Linux
 1. Abrimos una consola situados en el directorio donde tenemos nuestro proyecto.
 1. Escribimos el siguiente comando para iniciar el server y visualizar la aplicación en la url localhost:8080
     ```console
     root@root:~$ mvn jetty:run
 1. Para detener el server precionamos `Ctrl + c`
 
