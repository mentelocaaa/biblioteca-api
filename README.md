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
