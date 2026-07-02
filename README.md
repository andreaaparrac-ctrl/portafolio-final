# 💧 Fuente de Vida - E-Commerce de Agua Embotellada

Este proyecto constituye la entrega definitiva del **Portafolio Final del Módulo 7**. Consiste en una aplicación web transaccional completa para una distribuidora de agua purificada en Pelluhue, construida bajo estándares profesionales de arquitectura limpia, consistencia relacional y ciberseguridad defensiva.

🔗 **Enlace al Repositorio Público de GitHub:** https://github.com/andreaaparrac-ctrl/portafolio-final


---

## Requisitos Previos
*   Java Development Kit (JDK) 21 instalado.
*   Servidor local de PostgreSQL en ejecución.
*   IDE Eclipse o Spring Tool Suite (STS) con soporte para Maven.

## 🛠️ Instrucciones de Ejecución Local

Para levantar el proyecto de forma correcta en su entorno, por favor siga estos pasos:

1. Asegúrese de tener un esquema vacío creado en su servidor local de **PostgreSQL** llamado: `ecommerce-db-m3`
2. Si sus credenciales locales de PostgreSQL difieren de las estándar, puede editarlas en las líneas 3 y 4 del archivo `src/main/resources/application.properties`.
3. El sistema está configurado en modo portable seguro (`spring.jpa.hibernate.ddl-auto=update`), lo que significa que el motor creará automáticamente todas las tablas relacionales y el catálogo inicial en su primer arranque.
4. ## 🛠️ Instrucciones de Ejecución Local en Eclipse / STS
- Abra su entorno de desarrollo **Eclipse o Spring Tool Suite (STS)**.
- Importe el proyecto haciendo clic en: **File ➡️ Import ➡️ Existing Maven Projects**, seleccione la carpeta raíz y presione **Finish**.
- Para limpiar y descargar dependencias, haga clic derecho sobre la raíz del proyecto, seleccione **Run As ➡️ Maven clean**, y luego realice un **Maven install**.
- Para iniciar la aplicación, haga clic derecho sobre el proyecto, seleccione **Run As ➡️ Spring Boot App**.
5. Abra su navegador web e ingrese a la ruta local de desarrollo: `http://localhost:8081`


---

## 🔑 Rutas Principales y Credenciales de Prueba

El componente `DataInitializer` puebla la base de datos de manera automatizada al arrancar, habilitando los siguientes accesos para la revisión de la comisión:

### 🌐 1. Rutas Públicas (Acceso Libre)
*   **Inicio / Landing Page:** `/` (Incluye carrusel dinámico e información de la distribuidora).
*   **Inicio de Sesión:** `/login` (Protegido con escudo nativo contra ataques de fuerza bruta).
*   **Creación de Cuenta:** `/register` (Módulo de alta de nuevos clientes).

### 🛒 2. Rutas de Usuario CLIENT (Cliente de Prueba)
*   **Credenciales:** Correo: `globenuci@gmail.com` | Contraseña: `cliente123`
*   **Rutas Seguras:** `/catalogo` (Tienda de compras) y `/perfil` (Autogestión de datos y direcciones).
*   *Características:* Acceso al carrito lateral flotante interactivo (permite incrementar `+`, decrementar `-` y eliminar `🗑️` unidades con validación estricta de stock en tiempo real).

### ⚙️ 3. Rutas de Administrador ADMIN (Panel Gerencial)
*   **Credenciales:** Correo: `andrea.a.parrac@gmail.com` | Contraseña: `admin123`
*   **Ruta Segura:** `/admin/products` (Módulo administrativo restringido).
*   *Características:* Redirección automatizada para la gestión completa del inventario comercial de la distribuidora de agua.

---

## 📸 Presentación Visual del Sistema (Vistas Principales)

El proyecto cuenta con una interfaz responsiva integrada con Bootstrap 5 y Thymeleaf, distribuida de la siguiente manera:
1.  **Vista Home (`/`):** Presentación de la marca con carrusel automatizado de productos destacados.
2.  **Vista Catálogo (`/catalogo`):** Grilla comercial de bidones y dispensadores que gatilla la apertura lateral del carrito de compras controlado desde el servidor.
3.  **Vista Admin (`/admin/products`):** Panel de control exclusivo para la actualización inmediata de precios y existencias físicas de inventario.

---
*Desarrollado por Andrea Parra para el Portafolio Profesional.*