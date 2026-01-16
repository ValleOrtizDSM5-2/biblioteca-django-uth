# Descripción del proyecto:
Este proyecto es un Sistema de Biblioteca web desarrollado con Django, MySQL, GitHub y desplegado en PythonAnywhere. Permite gestionar libros, autores, editoriales, categorías y préstamos a través de un panel de administración de Django, mientras que las vistas públicas ofrecen funcionalidades de consulta, búsqueda y visualización de estadísticas. El sistema incluye autenticación, CRUD completo en el admin, y un frontend responsivo con Bootstrap 5.

# Tecnologías utilizadas:
- Backend: Django 4.2, Python 3.10+
- Base de datos: MySQL 8.0+
- Frontend: HTML5, CSS3, Bootstrap 5, JavaScript, Font Awesome
- Control de versiones: Git, GitHub
- Despliegue: PythonAnywhere
- Herramientas: VS Code, MySQL Workbench, OBS Studio (grabación)
- Dependencias principales: mysqlclient, pillow, django-environ

# Instrucciones de instalación:
1. Clonar el repositorio:

git clone https://github.com/USERNAME/biblioteca-django-uth.git
cd biblioteca-django-uth

2. Crear y activar entorno virtual:

python -m venv venv
# Windows:
.\venv\Scripts\activate
# Linux/Mac:
source venv/bin/actívate

3. Instalar dependencias:

pip install -r requirements.txt

4. Configurar base de datos MySQL:

CREATE DATABASE biblioteca_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

*Crear usuario y asignar privilegios.

5. Configurar variables de entorno:
Crear un archivo .env en la raíz del proyecto con:

DB_NAME=biblioteca_db
DB_USER=biblioteca_user
DB_PASSWORD=Pass123456!
DB_HOST=localhost
DB_PORT=3306
SECRET_KEY=tu-clave-secreta
DEBUG=True

6. Aplicar migraciones y crear superusuario:

python manage.py migrate
python manage.py createsuperuser

7. Ejecutar servidor de desarrollo:

python manage.py runserver

*Acceder a http://127.0.0.1:8000/

# Estructura del proyecto:
biblioteca_django/
├── biblioteca_project/       # Configuración principal de Django
├── libros/                   # Aplicación principal
│   ├── models.py            # Modelos: Autor, Libro, Categoría, Editorial, Préstamo
│   ├── views.py             # Vistas públicas
│   ├── urls.py              # Rutas de la app
│   ├── admin.py             # Configuración del panel admin
│   └── templates/libros/    # Templates HTML
├── templates/base/          # Template base (base.html)
├── static/                  # Archivos estáticos (CSS, JS, imágenes)
├── .env                     # Variables de entorno (NO subir a GitHub)
├── .gitignore              # Archivos excluidos de Git
├── requirements.txt         # Dependencias de Python
└── README.md               # Documentación del proyecto

# Información del autor:
- Nombre: Agustín Eduardo Valle Ortiz
- Asignatura: Aplicaciones Web Orientadas a Servicios
- Universidad: Universidad Tecnológica de Hermosillo (UTH)
- Cuatrimestre: 2026-1
- Profesor: Bernardo Prado Diaz
- GitHub: ValleOrtizDSM5-2
- PythonAnywhere: ValleOrtizAgustin
