markdown
# 📚 Biblioteca API

API RESTful para gestión de libros (CRUD completo) con Node.js, Express y MySQL.

## 🚀 Características

- CRUD completo (Create, Read, Update, Delete)
- Autenticación por sesión (cookie)
- Validaciones en capa de negocio
- Búsqueda por título/autor
- Códigos de estado HTTP correctos
- Arquitectura por capas (routes → controllers → models)

## 📋 Requisitos previos

- Node.js (v16+)
- MySQL (XAMPP / WAMP / independiente)

## 🛠️ Instalación

``` 
git clone https://github.com/tu-usuario/biblioteca-api.git
cd biblioteca-api
npm install
⚙️ Configuración
1.	Crear archivo .env:
 
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=
DB_NAME=biblioteca_db
PORT=3000
SESSION_SECRET=mi_secreto_seguro
2.	Ejecutar script SQL (phpMyAdmin o terminal)
3.	Iniciar servidor:
 
npm run dev


## Endpoints

| Método | Ruta | Descripción | Auth |
|---------|------|-------------|------|
| GET | /api/libros | Listar libros | No |
| GET | /api/libros?buscar= | Buscar libros | No |
| GET | /api/libros/:id | Obtener libro | No |
| POST | /api/libros | Crear libro | 🔒 API Key |
| PUT | /api/libros/:id | Actualizar libro | 🔒 API Key |
| DELETE | /api/libros/:id | Eliminar libro | 🔒 API Key |

## Seguridad

### API Key

Los endpoints de escritura (POST, PUT y DELETE)
requieren el siguiente header:


Si el cliente no envía este header o el valor es incorrecto,
el servidor responde con status 401 Unauthorized.

### HTTPS

HTTPS es la versión segura del protocolo HTTP.
Permite cifrar la comunicación entre el cliente y el servidor,
evitando que terceros puedan interceptar información sensible.

En producción es fundamental utilizar HTTPS para proteger
credenciales, cookies, tokens y datos enviados por la API.