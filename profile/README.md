# Products Market - Sistema de E-Commerce

Sistema de marketplace distribuido para comercio electrónico desarrollado con Spring Boot y arquitectura de microservicios.

## 📋 Descripción y Modelo de Datos (UML)
Plataforma de e-commerce que permite a empresas gestionar usuarios, productos y órdenes en tiempo real, con procesamiento automático de transacciones y control de inventario dinámico.

![Diagrama UML](https://github.com/Project-final-Products-Market/.github/blob/main/UML%20PROYECTO.PNG?raw=true)


## 🛠️ Stack Tecnológico

- Java 21 + Spring Boot 3.4.5
- Spring Cloud Gateway (API Gateway)
- Spring Cloud Eureka (Service Discovery)
- MySQL 8.0 (Base de datos)
- RestTemplate (Comunicación entre servicios)
- JUnit 5 + Mockito (Testing)

## 🏗️ Arquitectura de Microservicios

![Arquitectura Microservicios](https://github.com/Project-final-Products-Market/.github/blob/main/Arquitectura%20Microservicios.PNG?raw=true)


| Servicio | Puerto | Función | Endpoint Principal |
|----------|--------|---------|-------------------|
| 🌐 Gateway | 8087 | Enrutamiento y balanceador | http://localhost:8087 |
| 👥 User | 8081 | Gestión de usuarios | /api/users |
| 📦 Product | 8082 | Catálogo e inventario | /api/products |
| 🛒 Order | 8083 | Procesamiento de órdenes | /api/orders |
| 🗺️ Eureka | 8761 | Service discovery | http://localhost:8761 |

## ⚙️ Requisitos del Sistema

Java 21+, Maven 3.8+, MySQL 8.0+

## 🗄️ Configuración de Base de Datos

```sql
CREATE DATABASE marketjosemsp;
```

## 🚀 Orden de Ejecución

1. **Eureka Server**
2. **API Gateway**
3. **Microservicios** a la vez

## 🔗 Acceso al Sistema

- **Eureka Dashboard**: [http://localhost:8761](http://localhost:8761)
- **API Gateway**: [http://localhost:8087](http://localhost:8087)

## 💼 Casos de Uso Principales

```bash
# 1. Crear Usuario
POST http://localhost:8087/api/users
{
  "name": "Juan Pérez",
  "email": "juan@email.com"
}

# 2. Crear Producto
POST http://localhost:8087/api/products
{
  "name": "Laptop Gaming",
  "price": 1299.99,
  "stock": 15
}

# 3. Procesar Orden
POST http://localhost:8087/api/orders
{
  "userId": 1,
  "productId": 1,
  "quantity": 2
}

# 4. Consultar Órdenes
GET http://localhost:8087/api/orders/user/1
```

## 📊 Estados de Órdenes

- 🟡 **PENDING**: Orden creada, pendiente de confirmación
- 🟢 **CONFIRMED**: Orden confirmada, stock reservado
- 🔴 **CANCELLED**: Orden cancelada, stock liberado
- ✅ **DELIVERED**: Orden entregada (estado final)

## ✨ Características Principales

### Funcionalidades de Negocio
- ✅ Gestión completa de usuarios y autenticación
- ✅ Catálogo de productos con control de stock
- ✅ Procesamiento automático de órdenes
- ✅ Gestión de estados del ciclo de vida
- ✅ Coordinación automática entre servicios
- ✅ Analytics y reportes de ventas

### Características Técnicas
- ✅ 🌐 **API Gateway**: Punto único de entrada
- ✅ ⚖️ **Load Balancing**: Distribución automática de carga
- ✅ 🔍 **Service Discovery**: Registro automático de servicios
- ✅ 💾 **Shared Database**: Consistencia de datos
- ✅ 🔧 **Microservicios**: Escalado independiente

### Escalabilidad y Operaciones
- ✅ Múltiples instancias por servicio
- ✅ Balanceador de carga automático
- ✅ Tolerancia a fallos con compensación
- ✅ Monitoreo centralizado via Eureka

### Beneficios para el Negocio
- ✅ Gestión centralizada de inventario
- ✅ Procesamiento de órdenes en tiempo real
- ✅ Control automático de stock
- ✅ Integración fácil con sistemas externos

### Experiencia del Usuario
- ✅ APIs unificadas via Gateway
- ✅ Respuesta rápida en transacciones
- ✅ Consistencia en el manejo de datos
- ✅ Interfaz REST estándar

## 🧪 Colección de Pruebas

Se incluye una colección completa con casos de prueba realistas para validar el sistema:

- 👤 **Gestión de usuarios**: Registro, búsqueda, activación
- 📦 **Catálogo de productos**: CRUD, stock, filtros
- 🛒 **Flujo de órdenes**: Creación, estados, cancelación
- 📊 **Analytics**: Estadísticas, reportes, métricas
- ❌ **Casos de error**: Validaciones y manejo de excepciones

### 📥 Instrucciones de Uso

- Asegúrate de tener todos los microservicios corriendo en `http://localhost:8087`.
- Descarga la colección y ábrela en [Postman](https://www.postman.com/).
- Ejecuta los circuitos de pruebas según el flujo comercial deseado.

📄 **[Descargar colección Postman (JSON)](https://github.com/Project-final-Products-Market/.github/blob/main/Market_Josemsp.json)**


## 🔮 Roadmap de Mejoras

- **Frontend Web** con React
- **Autenticación JWT** centralizada
- **Rate Limiting** en Gateway
- **Containerización** con Docker
- **Dashboard de métricas** avanzado

## 📋 Gestión del Proyecto

🔗 **[Tablero de Trello](https://trello.com/invite/b/682ede3449b93679ac4d81f8/ATTI9a38d437f768f172b32b0ef5c72400ed9105FAA4/products-josemsp-market)** - Seguimiento de tareas y sprints

## 👨‍💻 Sobre el Desarrollador
#### **Jose Manuel Siguero Pérez**

🔗 **[LinkedIn](https://www.linkedin.com/in/jose-manuel-siguero)**

📄 **[Presentación del Proyecto](#)** *(próximamente)*

---

🛒 **Sistema desarrollado para optimizar operaciones de e-commerce**

## ⭐ Agradecimientos

Gracias por revisar este poryecto de microservicios. Si te ha parecido interesante, muestra tu apoyo.

---

🛒 **Sistema desarrollado con ilusión y ganas para revolucionar el comercio electrónico**
