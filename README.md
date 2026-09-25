# 💰 App de Gestión de Finanzas Personales (Full-Stack)

Una aplicación móvil Full-Stack diseñada para el control de ingresos y gastos personales en tiempo real, desarrollada con una arquitectura limpia, comunicación HTTP asíncrona y persistencia en base de datos relacional.

---

## 📸 Capturas de Pantalla & Demostración

| Vista Principal (Lista) | Registro / Edición |
| :---: | :---: |
| ![Movimientos](frontend/screenshots/movimientos.png) | ![Editar Movimiento](frontend/screenshots/nuevo_movimiento.png) |

---

## 🚀 Tecnologías y Herramientas

### **Frontend (Aplicación Móvil)**
- **Flutter & Dart**: Framework multiplataforma para la construcción de interfaces nativas.
- **HTTP / REST API Client**: Integración de peticiones asíncronas con consumo de endpoints REST (`GET`, `POST`, `PUT`, `DELETE`).
- **Material Design 3**: Componentes de UI modernos, manejo de estados dinámicos e interacciones con gestos (`Dismissible`).

### **Backend (API RESTful)**
- **Java 17 & Spring Boot**: Framework robusto en capa de servicio y controlador REST.
- **Spring Data JPA / Hibernate**: Mapeo objeto-relacional (ORM) para interacción con PostgreSQL.
- **PostgreSQL**: Base de datos relacional para la persistencia de movimientos financieros.
- **Gradle**: Gestor de dependencias y automatización de construcción del proyecto.

---

## 🛠️ Funcionalidades del Sistema (CRUD Completo)

- 📥 **Consulta de Movimientos (`GET /api/movimientos`)**: Carga dinámica de transacciones clasificadas en ingresos y gastos.
- ➕ **Registro de Movimiento (`POST /api/movimientos`)**: Formulario con validación estricta de campos, categorías y montos.
- ✏️ **Edición en Tiempo Real (`PUT /api/movimientos/{id}`)**: Carga automática de datos existentes para su actualización y persistencia.
- 🗑️ **Eliminación con Confirmación (`DELETE /api/movimientos/{id}`)**: Remoción de registros mediante gesto de deslizar (*swipe to delete*) y cuadro de diálogo interactivo.

---

## ⚙️ Instrucciones para la Ejecución Local

### **Prerrequisitos**
- JDK 17 instalado.
- Flutter SDK 3.x configurado.
- Instancia local de PostgreSQL activa (Puerto predeterminado: `5432`).

### **1. Configurar y Ejecutar el Backend (Spring Boot)**
```bash
# Ingresar al directorio backend
cd backend

# Ejecutar la aplicación con Gradle
./gradlew bootRun