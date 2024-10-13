# Gestor_Usuarios_APP_FLASK_MVC
# backend_web1

Este repositorio contiene el backend de una aplicación web para gestionar usuarios de manera segura, utilizando contraseñas con hash para asegurar la integridad del sistema. Está desarrollada con Flask siguiendo el patrón MVC.

## Índice
- [Descripción](#descripción)
- [Deploy](#despliegue-en-producción)
- [Características](#características)
- [Requisitos previos](#requisitos-previos)
- [Instalación](#instalación)
- [Estructura del proyecto MVC](#estructura-del-proyecto-mvc)
- [Despliegue en Railway](#despliegue-en-railway)
- [Despliegue en Render](#despliegue-en-render)
- [Licencia](#licencia)

## Descripción

Aplicación web para gestionar usuarios, implementada con Flask y MySQL, diseñada siguiendo el patrón MVC. Ofrece funciones CRUD para la administración de usuarios, asegurando las contraseñas con hash.

## Despliegue en producción

Accede a la aplicación en: [https://backend-web1.onrender.com](https://backend-web1.onrender.com)

## Características

- Gestión de usuarios (crear, leer, actualizar, eliminar).
- API RESTful.
- Contraseñas almacenadas con hash.
- Despliegue en Render.

## Requisitos previos
- Python 3.x
- MySQL
- Pip
#Los demás requerimientos están en: `requirements.txt`.

## Instalación
Clona este repositorio:

bash
Copiar código
git clone https://github.com/CrisJurado10/backend_web1.git
cd backend_web1
Crea y activa un entorno virtual:

bash
Copiar código
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
Instala las dependencias:

bash
Copiar código
pip install -r requirements.txt

Creación de la base de datos en MySQL:
sql
Copiar código
CREATE DATABASE railway;
USE railway;

CREATE TABLE usuarios (
    id INT AUTO_INCREMENT PRIMARY KEY,
    usuario VARCHAR(100) NOT NULL,
    correo VARCHAR(100) NOT NULL,
    contraseña VARCHAR(100) NOT NULL
);

Configura las variables de entorno para la base de datos en .env: (Para el uso de manera local)
env
Copiar código
MYSQL_USER=<tu_usuario>
MYSQL_PASSWORD=<tu_contraseña>
MYSQL_DB=<railway>

Ejecuta la aplicación:
terminal
Copiar código
flask run

Estructura del proyecto MVC
controllers/: Lógica de negocio y gestión de rutas.
models/: Definición de modelos de la base de datos.
static/: Archivos estáticos como CSS o imágenes.
templates/: Archivos HTML.

## Despliegue en Railway
La aplicación recupera datos de una base de datos MySQL alojada en un servidor de Railway.

## Despliegue en Render
Este proyecto está configurado para ejecutarse en Render con un archivo Procfile que define el comando de inicio para la aplicación.

## Licencia
Este proyecto está bajo la Licencia MIT.


