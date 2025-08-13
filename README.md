# 🌸 Sistema de Gestión - Fragancia

Este proyecto es una aplicación web completa para la gestión de una tienda de fragancias. Permite manejar productos, proveedores, clientes, empleados, compras, ventas, usuarios, roles y configuración de seguridad. La aplicación cuenta con autenticación mediante JWT y una interfaz visual desarrollada en HTML y CSS.

(El proyecto no está finalizado al 100%, pero, conforme el cronograma que se tiene con el cliente aún queda mucho tiempo disponible para su entrega y despliegue, pero con la fecha de entrega del proyecto para presentación de clase lamentablemente no pudimos terminarlo a tiempo, lo que si se logró fue cumplir con los requerimientos solicitados tanto por la parte de conexión cliente-servidor y el uso de triggers, proximamente tambien está pensado usar varios procedimientos almacenados)

---

## 🧾 Descripción General

El sistema **Fragancia** está diseñado para cubrir todas las operaciones clave de una tienda de fragancias, incluyendo:

- Gestión de productos  
- Registro de clientes y proveedores  
- Control de inventario mediante compras y ventas  
- Administración de usuarios y roles  
- Módulo de configuración con control de acceso  
- Interfaz de login y menú de administrador  
- Seguridad mediante autenticación con tokens (JWT)  

---

## 🗃️ Funcionalidades Implementadas

| Módulo       | Funciones principales                                              |
|--------------|--------------------------------------------------------------------|
| **Productos**    | Crear, listar, editar y eliminar productos                         |
| **Clientes**     | Crear, listar, editar y eliminar clientes                          |
| **Proveedores**  | CRUD de proveedores (nombre, contacto, dirección, etc.)            |
| **Compras**      | Registrar compras (producto, proveedor, cantidad, fecha)           |
| **Ventas**       | Registrar ventas y actualizar stock automáticamente                |
| **Usuarios**     | Crear, editar, cambiar contraseña, activar/desactivar              |
| **Roles**        | Crear, editar, eliminar roles                                      |
| **Empleados**    | Gestión básica de empleados relacionados a usuarios                |
| **Autenticación**| Login, generación y verificación de token JWT                      |
| **Seguridad**    | Middleware para proteger rutas privadas                             |
| **Menú principal**| Interfaz visual con menú y navegación entre módulos                |

---

## 🛠️ Tecnologías Utilizadas

- **Node.js** y **Express.js** – Backend y API RESTful  
- **MariaDB** – Base de datos relacional (por el momento local, se espera alojar en la nube para cuando salga a produccion)
- **HTML y CSS** – Interfaz visual  
- **JWT (jsonwebtoken)** – Autenticación y protección de rutas  
- **Dotenv** – Configuración por variables de entorno  
- **Cors**, **Morgan**, **Cookie-Parser** – Middlewares útiles para desarrollo  
- **GitHub Web** – Control de versiones y colaboración

---

## 🔐 Rutas Principales de la API

Todas las rutas protegidas requieren autenticación mediante token.

| Ruta                       | Funcionalidad                                |
|----------------------------|----------------------------------------------|
| `POST /api/login`          | Iniciar sesión y obtener token               |
| `GET /api/menu-admin`      | Verificar token y rol del usuario            |
| `/api/productos`           | CRUD de productos                            |
| `/api/clientes`            | CRUD de clientes                             |
| `/api/proveedores`         | CRUD de proveedores                          |
| `/api/compras`             | Registrar y ver compras                      |
| `/api/ventas`              | Registrar y ver ventas                       |
| `/api/usuarios`            | Gestión de usuarios                          |
| `/api/roles`               | Gestión de roles                             |
| `/api/empleados`           | Gestión de empleados                         |
| `/api/verify-session`      | Verificar token activo                       |

---

## 🔐 Seguridad y Autenticación

- El login genera un token JWT válido por tiempo configurable.
- El token se usa para acceder a rutas protegidas.
- Implementado middleware `verificarToken` para proteger accesos no autorizados.

## 🔗 Conexión a la Base de Datos

Se usa un archivo `.env` para configurar las credenciales de conexión a MariaDB:

ejemplo del env:
PORT=5000
DB_HOST=localhost
DB_PORT=3307
DB_USER=XXXX
DB_PASSWORD=XXXX
DB_NAME=fragancia
JWT_SECRET=XXXX
COOKIE_NAME=XXXX

## 🚀 Instrucciones para Ejecutar el Proyecto
1. Clona el repositorio:
2. Instala las dependencias del backend:

- npm install

4. Crea el archivo .env con las credenciales de tu base de datos.

5. Inicia el servidor desde la carpeta raíz del backend:

Debe de imprimir en consola:📍 El servidor estará corriendo en: http://localhost:5000

🔐 Puedes abrir http://localhost:5000/login.html para iniciar sesión desde el navegador.

## 📌 Notas Adicionales
- El frontend se encuentra en la carpeta public, y puede personalizarse fácilmente.

- El sistema está en constante desarrollo, por lo que se seguirán agregando funcionalidades.

- ❌ No se incluye el módulo de devoluciones, ya que fue descartado del alcance actual.

## 💻 Desarrollado por Miguel Salguero *proyecto no terminado :(




