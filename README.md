# 🏦 Proyecto Lógica - Solución de Problemas (API Bancaria)

Este proyecto consiste en una **API REST de un sistema bancario**, desarrollada en **Java Spring Boot**, con el objetivo de aplicar principios de **programación orientada a objetos**, **buenas prácticas**, y **gestión de servicios RESTful**.  

El proyecto simula operaciones bancarias básicas como la creación de clientes, apertura de cuentas y manejo de transacciones.

---

## 🚀 Tecnologías utilizadas

- **Java 17**
- **Spring Boot**
- **Swagger UI**
- **Thunder Client / Postman** (para pruebas)
- **Maven**
- **JSON**

---

## ⚙️ Funcionalidades principales

### 👤 Módulo de Clientes (`/api/bank/customers`)
- **POST** → Crear un nuevo cliente  
- **GET** → Obtener todos los clientes  
- **GET** `/api/bank/customers/{id}` → Obtener un cliente por su ID  

📸 Ejemplo de creación y consulta de clientes en **Thunder Client**:

![Crear cliente](./Customers.png)
![Consultar cliente](./Crear%20cuenta.png)

---

### 💰 Módulo de Cuentas (`/api/bank/accounts`)
- **POST** `/api/bank/customers/{customerId}/accounts` → Crear una nueva cuenta para un cliente  
- **GET** `/api/bank/accounts/{accountId}` → Consultar los detalles de una cuenta  

📸 Ejemplo de creación y consulta de cuentas:

![Crear cuenta](./Crear%20cuenta.png)

---

### 💳 Operaciones Bancarias
- **POST** `/api/bank/accounts/{accountId}/deposit` → Realizar un depósito  
- **POST** `/api/bank/accounts/{accountId}/withdraw` → Realizar un retiro  

📸 Ejemplo en Swagger UI:

![Swagger](./swagger.png)
![Swagger 2](./swagger2.png)
![Swagger 3](./swagger3.png)
![Swagger 4](./swagger4.png)

---

## 📘 Documentación con Swagger UI

El proyecto incluye documentación generada automáticamente con **Swagger UI**.  
Para acceder a ella, una vez que el servidor está corriendo, entra a:

http://localhost:8080/swagger-ui/index.html

yaml
Copiar código

---

## 🧪 Ejemplo de flujo completo

1. Crear un cliente con un `POST /api/bank/customers`
2. Crear una cuenta asociada con `POST /api/bank/customers/{id}/accounts`
3. Consultar la cuenta con `GET /api/bank/accounts/{accountId}`
4. Realizar depósitos o retiros con los endpoints `/deposit` y `/withdraw`

---

## 📂 Estructura del proyecto

src/
├── main/
│ ├── java/
│ │ └── com.bank/
│ │ ├── controller/
│ │ ├── model/
│ │ ├── service/
│ │ └── BankApplication.java
│ └── resources/
│ ├── application.properties
│ └── static/
└── test/

yaml
Copiar código

---

## 🧑‍💻 Autor

**Sebastián Orrego Lopera**  
[Repositorio en GitHub](https://github.com/ElFiestero438/logica-solucion-de-problemas)

---

## 🏁 Ejecución del proyecto

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/ElFiestero438/logica-solucion-de-problemas.git
Abrir el proyecto en IntelliJ IDEA o VS Code

Ejecutar la clase principal BankApplication

Acceder al servidor en:

arduino
Copiar código
http://localhost:8080
📸 Resultados finales
El sistema fue probado exitosamente con Thunder Client y Swagger UI, mostrando respuestas correctas para todas las operaciones REST definidas.