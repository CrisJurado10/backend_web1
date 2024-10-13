# Gestor_Usuarios_APP_FLASK_MVC
# backend_web1

Este repositorio contiene el backend de una aplicación web para gestionar usuarios,de manera segura teniendo una base de datos con contraseñas tipo hash asegurando la seguridad e integridad del sistema, desarrollada con Flask siguiendo el patrón MVC.

## Índice
- [Descripción](#descripción)
- [Deploy](#despliegue-en-producción)
- [Características](#características)
- [Requisitos previos](#requisitos-previos)
- [Instalación](#instalación)
- [Estructura del proyecto](#estructura-del-proyecto)
- [Despliegue en Railway](#despliegue-en-railway)
- [Licencia](#licencia)

## Descripción

Aplicación web para gestionar usuarios, implementada con Flask y MySQL, diseñada siguiendo el patrón MVC. Ofrece funciones CRUD para la administración de usuarios, y está lista para despliegue en Render.

### Despliegue en producción

Accede a la aplicación en: [https://backend-web1.onrender.com](https://backend-web1.onrender.com)

## Características

- Gestión de usuarios (crear, leer, actualizar, eliminar).
- API RESTful.
- Autenticación básica.
- Configurado para despliegue en Render.

## Requisitos previos

- Python 3.x
- MySQL
- Pip

Dependencias listadas en `requirements.txt`:

```plaintext
blinker==1.8.2
click==8.1.7
colorama==0.4.6
Flask==3.0.3
Flask-MySQLdb==2.0.0
gunicorn==23.0.0
itsdangerous==2.2.0
Jinja2==3.1.4
MarkupSafe==3.0.1
mysql-connector-python==9.0.0
mysqlclient==2.2.4
packaging==24.1
Werkzeug==3.0.4


## Instalación
1. Clona este repositorio:
   ```bash
   git clone https://github.com/CrisJurado10/backend_web1.git
   cd backend_web1

2. Crea y activa un entorno virtual:

bash
Copiar código
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate

3. Instala las dependencias:
bash
Copiar código
pip install -r requirements.txt

4. Creación de la BDD en MySQL:
CREATE database railway
USE railway; 


SELECT * FROM railway.usuarios;

CREATE TABLE usuarios (
    id INT AUTO_INCREMENT PRIMARY KEY,
    usuario VARCHAR(100) NOT NULL,
    correo VARCHAR(100) NOT NULL,
    contraseña VARCHAR(100) NOT NULL
);


5. Configura las variables de entorno para la base de datos en .env:
env
Copiar código
MYSQL_USER=<tu_usuario>
MYSQL_PASSWORD=<tu_contraseña>
MYSQL_DB=<nombre_base_datos>


Ejecuta la aplicación:
terminal
Copiar código
flask run

## Estructura del proyecto MVC
controllers/: Lógica de negocio y gestión de rutas.
models/: Definición de modelos de la base de datos.
static/: Archivos estáticos como CSS o imágenes.
templates/: Archivos HTML.

## Despliegue en Render
Este proyecto está configurado para ejecutarse en Render con un archivo Procfile que define el comando de inicio para la aplicación.

## Despliegue en Railway
La página web recupera data de una base de datos MySQL alojada en un servidor de Railway.

## Licencia
Este proyecto está bajo la Licencia MIT.

