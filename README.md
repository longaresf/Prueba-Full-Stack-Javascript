# Integrated JavaScript Full Stack Application

Este repositorio contiene una solución web integral (*End-to-End*) desarrollada completamente en el ecosistema **JavaScript**. El proyecto unifica una robusta API de backend con una interfaz de usuario dinámica y responsiva, demostrando el dominio de la comunicación cliente-servidor, el diseño de arquitecturas RESTful y la persistencia de datos.

## 🧱 Arquitectura del Sistema

La aplicación está dividida en dos componentes principales perfectamente desacoplados:

### 1. Backend (Capa de Servidor)
* **Motor de Servidor:** Diseñado con **Node.js** y el framework **Express**.
* **API RESTful:** Endpoints estructurados para operaciones CRUD (Create, Read, Update, Delete) con respuestas estandarizadas en formato JSON.
* **Persistencia:** Gestión y modelado de datos utilizando PostgreSQL.

### 2. Frontend (Capa de Presentación)
* **Interfaz de Usuario:** Construida utilizando HTML5, CSS3 y JavaScript nativo (ES6+).
* **Consumo Asíncrono:** Comunicación fluida con el backend mediante la Fetch API utilizando patrones de asincronía (`async/await`).
* **Estilos y Layout:** Diseño responsivo y modular con Bootstrap.

## 🛠️ Stack Tecnológico

* **Lenguaje unificado:** JavaScript (ES6+)
* **Entorno de Ejecución:** Node.js
* **Framework Backend:** Express
* **Base de Datos / Almacenamiento:** PostgreSQL.
* **Control de Rutas y Sesiones:** Middlewares de validación, JWT.

## ⚙️ Desafíos de Ingeniería Solucionados

El desarrollo de esta solución Full Stack resolvió problemáticas clave de la integración de sistemas:

1. **Intercambio de Recursos de Origen Cruzado (CORS):** Configuración segura del middleware de CORS en el backend para permitir peticiones controladas desde el dominio del frontend, evitando bloqueos de seguridad en el navegador.
2. **Manejo de Errores Centralizado:** Implementación de bloques de control de excepciones tanto en el cliente (para fallos de red) como en el servidor (para peticiones inválidas), garantizando la estabilidad de la app.
3. **Flujo de Datos Unificado:** Diseño de modelos de datos consistentes que se transforman limpiamente desde los registros de la base de datos hasta los componentes visuales del DOM.

## 🔧 Configuración e Instalación Local

Para levantar todo el ecosistema localmente, sigue estos pasos:

### Prerrequisitos
* Tener instalado **Node.js** (versión LTS recomendada) y **npm**.

### Paso 1: Clonar e instalar dependencias del Backend
1. Clonar el repositorio:
   ```bash
   git clone [https://github.com/longaresf/javascript-fullstack-application.git](https://github.com/longaresf/javascript-fullstack-application.git)
    ```
2. Ingresar a la carpeta del proyecto (o a la carpeta /backend si están separadas):
    Bash
   cd javascript-fullstack-application

3. Instalar los paquetes de Node:
    Bash
   npm install

Paso 2: Configuración y Arranque

1. [Opcional] Si utilizas variables de entorno, configura tu archivo .env basándote en el archivo de ejemplo proporcionado.

2. Iniciar el servidor de desarrollo:
    Bash
   npm run dev  # O 'node index.js' / 'nodemon' según tus scripts de package.json

3. Abre el archivo frontend (index.html o levanta el servidor de cliente si aplica) en tu navegador para interactuar con la aplicación conectada al servidor local.

✒️ Autor

    Francisco Longares - Desarrollador Full Stack JavaScript - longaresf
