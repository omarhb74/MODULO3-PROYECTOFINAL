PROYECTO FINAL MODULO 3 
-----------------------
desarrollado por :Omar Hinojosa Ballon
diplomado en FULL-STACK - Universidad Simon I Patiño

CREACION DE LA BASE DE DATOS POSTGRE
-------------------------------------

-Inicialmente es necesario crear la Base de datos y la tabla Usuarios desde linea de comandos desde el archivo adjunto a este proyecto (table_create) en una base de datos Postgre

creacion de la Base de datos
CREATE DATABASE PROYECTO

creacion de tabla
CREATE TABLE usuario (
	id_usuario serial primary key,
	nombre_completo varchar (50),
	edad integer
)



-Se desarrollo la aplicacion en una base de datos POSTGRE en una maquina virtual dentro el mismo segmento de red

-para realizar la conexion a la base de datos es necesario generar la conexion a la base de datos :

const config = {
    user:'postgres',   //usuario de conexion a la base de datos
    database :'PROYECTO', // nombre de la base de datos, debe respetarse mayusculas
    password:'0000',      //la contraseña en mi base de datos es 0000
    host:'192.168.100.29', // esta es la direccion IP de mi maquina virtual en mi red interna
    port :5432,   // puerto por defecto de conexion a la base de datos POSTGRE
    ssl:false,    // mi base de datos no tiene configurado el socket de configuracion por lo que esta en falso
    idleTimeoutMillis : 30000  //definicion de timeout
}

USO DEL SISTEMA
---------------

de acuerdo al requerimiento se tiene los siguientes modulos o funciones:


LISTA DE USUARIOS : 
-------------------

	FUNCION GET DESDE POSTMAN
	RUTA : localhost:3000/usuarios

AÑADIR USUARIO:
---------------

	FUNCION POST DESDE POSTMAN EN FORMATO JSON
	RUTA : localhost:3000/usuarios

PROMEDIO EDADES:
---------------

	FUNCION GET
	RUTA : localhost:3000/usuarios/promedio

INFORMACION DEL SISTEMA:
-------------------

	FUNCION GET
	RUTA : localhost:3000/usuarios/status





INSTALACION DE MODULOS
----------------------

en nodejs es necesario instalar los siguientes modulos :

    "body-parser": "^1.20.1",
    "express": "^4.18.2",
    "pg": "^8.8.0"


ayuda para instalar:

	npm install body-parser
	npm install express
	npm install pg

INSTALACION DEL SISTEMA
------------------------

unidadDisco:\MODULO3-PROYECTOFINAL\src\index.js
unidadDisco:\MODULO3-PROYECTOFINAL\node_modules
unidadDisco:\MODULO3-PROYECTOFINAL\package.json
unidadDisco:\MODULO3-PROYECTOFINAL\package-lock.json
unidadDisco:\MODULO3-PROYECTOFINAL\readme.txt








