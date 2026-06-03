# Prueba Full Stack - Gestor de Conversiones de Moneda

Una aplicación web full stack desarrollada con **Node.js**, **Express**, **Handlebars** y **PostgreSQL** que permite convertir monedas y registrar el historial de operaciones.

## 📋 Descripción

Esta es una aplicación de prueba que implementa un sistema de conversión de monedas con persistencia de datos. Combina un backend robusto con una interfaz de usuario interactiva, permitiendo a los usuarios convertir entre diferentes monedas y consultar el historial de sus operaciones.

## 🛠️ Stack Tecnológico

### Backend
- **Node.js** - Entorno de ejecución JavaScript
- **Express.js** - Framework web minimalista y flexible
- **Express-Handlebars** - Motor de plantillas
- **PostgreSQL** - Base de datos relacional
- **Body-Parser** - Middleware para parsear solicitudes HTTP
- **Axios** - Cliente HTTP para realizar peticiones

### Frontend
- **Handlebars** - Plantillas HTML dinámicas
- **Bootstrap 5** - Framework CSS para diseño responsivo
- **jQuery 3.6** - Librería JavaScript para manipulación del DOM

## 📁 Estructura del Proyecto

```
Prueba Full Stack/
├── index.js                 # Archivo principal del servidor
├── consultas.js            # Funciones de base de datos
├── package.json            # Dependencias del proyecto
├── public/                 # Archivos estáticos (CSS, JS, imágenes)
└── views/
    ├── mainLayout/         # Plantillas de diseño principal
    ├── componentes/        # Componentes reutilizables
    └── Home.handlebars     # Página principal
```

## 🚀 Instalación

### Prerrequisitos
- Node.js (v14 o superior)
- PostgreSQL (instalado y ejecutándose)
- npm (gestor de paquetes de Node.js)

### Pasos de instalación

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/longaresf/Prueba-Full-Stack-Javascript.git
   cd "Prueba-Full-Stack-Javascript/Prueba Full Stack"
   ```

2. **Instalar dependencias**
   ```bash
   npm install
   ```

3. **Configurar variables de entorno**
   
   Crea un archivo `.env` en la raíz del proyecto (si es necesario):
   ```env
   PUERTO=3000
   HOST=localhost
   DB_HOST=localhost
   DB_USER=postgres
   DB_PASSWORD=tu_contraseña
   DB_NAME=nombre_base_datos
   DB_PORT=5432
   ```

4. **Configurar la base de datos**
   
   Asegúrate de que PostgreSQL esté ejecutándose y crea la base de datos necesaria.

5. **Iniciar la aplicación**
   ```bash
   npm start
   ```
   
   O con node directamente:
   ```bash
   node index.js
   ```

6. **Acceder a la aplicación**
   
   Abre tu navegador y ve a: `http://localhost:3000`

## 📝 Funcionalidades

### Conversión de Moneda
- Convertir montos entre diferentes monedas
- Soporte para múltiples pares de monedas
- Historial de conversiones almacenado en la base de datos

### Historial de Operaciones
- Visualizar todas las conversiones realizadas
- Información detallada de cada operación (monto, monedas, fecha)
- Búsqueda y filtrado de operaciones

## 🔌 Endpoints API

### GET `/`
Renderiza la página principal de la aplicación.

**Respuesta:** HTML con la página Home

---

### POST `/convertir`
Realiza una conversión de moneda y la registra en la base de datos.

**Body (JSON):**
```json
{
  "monto": 100,
  "monedaOrigen": "USD",
  "fechaConv": "2024-01-15",
  "monedaDestino": "EUR"
}
```

**Respuesta:** Resultado de la conversión y confirmación del registro

---

### GET `/Buscar`
Obtiene todas las operaciones de conversión registradas.

**Respuesta (JSON):**
```json
[
  {
    "id": 1,
    "monto": 100,
    "moneda_origen": "USD",
    "moneda_destino": "EUR",
    "fecha_conversion": "2024-01-15",
    "resultado": 92.50
  }
]
```

---

### GET `*`
Maneja todas las rutas no definidas con un mensaje de error amigable.

## 🗄️ Esquema de Base de Datos

La aplicación requiere una tabla para almacenar las operaciones de conversión:

```sql
CREATE TABLE operaciones (
  id SERIAL PRIMARY KEY,
  monto DECIMAL(10, 2) NOT NULL,
  moneda_origen VARCHAR(3) NOT NULL,
  moneda_destino VARCHAR(3) NOT NULL,
  fecha_conversion DATE NOT NULL,
  resultado DECIMAL(10, 2) NOT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## 📦 Dependencias

| Paquete | Versión | Descripción |
|---------|---------|-------------|
| express | ^4.18.1 | Framework web |
| express-handlebars | ^6.0.6 | Motor de plantillas |
| body-parser | ^1.20.0 | Middleware para parsear cuerpos de solicitud |
| pg | ^8.7.3 | Driver de PostgreSQL |
| axios | ^0.27.2 | Cliente HTTP |
| bootstrap | ^5.1.3 | Framework CSS |
| jquery | ^3.6.0 | Librería JavaScript |

## 🔧 Scripts Disponibles

```bash
npm test          # Ejecutar tests (actualmente no configurado)
npm start         # Inicia la aplicación
```

## 🤝 Contribuir

Si deseas contribuir al proyecto:

1. Fork el repositorio
2. Crea una rama para tu característica (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia ISC - ver el archivo [LICENSE](LICENSE) para más detalles.

## ✨ Autor

**longaresf** - [GitHub Profile](https://github.com/longaresf)

## 🐛 Solución de Problemas

### El servidor no inicia
- Verifica que Node.js esté instalado: `node --version`
- Asegúrate de estar en el directorio correcto
- Comprueba que el puerto 3000 no esté en uso

### Error de conexión a PostgreSQL
- Verifica que PostgreSQL esté ejecutándose
- Comprueba las credenciales en el archivo `.env`
- Asegúrate de que la base de datos exista

### Dependencias faltantes
- Ejecuta `npm install` de nuevo
- Limpia el caché: `npm cache clean --force`
- Intenta eliminar `node_modules` y vuelve a instalar

## 📞 Soporte

Para reportar problemas o sugerencias, abre un [issue](https://github.com/longaresf/Prueba-Full-Stack-Javascript/issues) en el repositorio.

---

**Última actualización:** Junio 2026
