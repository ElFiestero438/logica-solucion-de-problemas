# 🏦 AppBank — Sistema Bancario con Spring Boot

## 📋 Descripción del Proyecto
**AppBank** es una aplicación desarrollada con **Spring Boot** que simula un sistema bancario básico.  
Permite **gestionar clientes, cuentas y transacciones**, además de realizar **depósitos, retiros, transferencias** y **aplicar intereses**.  

El proyecto incluye:
- Exposición de **endpoints REST**.
- **Documentación interactiva con Swagger UI**.
- **Colección de pruebas con Postman (Thunder Client)** para validar el correcto funcionamiento de los endpoints.

---

## ⚙️ Tecnologías Utilizadas

| Tecnología | Descripción |
|-------------|-------------|
| **Java 21** | Lenguaje principal del proyecto |
| **Spring Boot 3.5.7** | Framework backend |
| **Maven** | Sistema de gestión de dependencias |
| **Spring Web** | Para construir y exponer las APIs REST |
| **Spring Validation** | Validación de datos de entrada |
| **Springdoc OpenAPI (Swagger UI)** | Documentación y pruebas de los endpoints |
| **Thunder Client (VS Code)** | Pruebas y validación de los endpoints REST |
| **JUnit 5** | (Opcional) Pruebas unitarias |

---

## 🚀 Cómo Ejecutar el Proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/appbank.git
Entra en el directorio del proyecto:

bash
Copiar código
cd appbank
Ejecuta la aplicación:

bash
Copiar código
mvn spring-boot:run
Abre tu navegador y visita:

bash
Copiar código
http://localhost:8080/swagger-ui.html
📚 Endpoints Principales
Módulo	Método	Endpoint	Descripción
Clientes	POST	/api/bank/customers	Crear un nuevo cliente
GET	/api/bank/customers	Listar todos los clientes
GET	/api/bank/customers/{customerId}	Consultar cliente por ID
Cuentas	POST	/api/bank/customers/{customerId}/accounts	Crear cuenta asociada a un cliente
GET	/api/bank/accounts/{accountId}	Consultar cuenta por ID
GET	/api/bank/customers/{customerId}/accounts	Listar cuentas de un cliente
Transacciones	POST	/api/bank/accounts/{accountId}/deposit	Depositar en una cuenta
POST	/api/bank/accounts/{accountId}/withdraw	Retirar de una cuenta
POST	/api/bank/accounts/{fromAccountId}/transfer	Transferir entre cuentas
GET	/api/bank/accounts/{accountId}/transactions	Consultar transacciones
Intereses	POST	/api/bank/accounts/{accountId}/apply-interest	Aplicar intereses

🧭 Documentación con Swagger
La documentación interactiva de la API está disponible en:

bash
Copiar código
http://localhost:8080/swagger-ui.html
📸 Capturas de Swagger


	

🧪 Pruebas con Thunder Client (Postman)
Todas las pruebas se realizaron usando la extensión Thunder Client en Visual Studio Code.

📸 Capturas de Thunder Client
Captura	Descripción	Imagen
1️⃣	Crear Cliente (POST /customers)	
2️⃣	Crear Cuenta (POST /accounts)	
3️⃣	Depósito (POST /deposit)	
4️⃣	Retiro (POST /withdraw)	
5️⃣	Transferencia (POST /transfer)	

🧩 Estructura del Proyecto
css
Copiar código
appbank/
├── src/
│   ├── main/java/com/logsoluprobl/appbank/
│   │   ├── controller/       → Controladores REST
│   │   ├── model/            → Entidades principales (Customer, Account, etc.)
│   │   ├── service/          → Lógica de negocio
│   │   └── exception/        → Manejo de excepciones
│   └── resources/
│       └── application.properties
├── docs/                     → Capturas Swagger y Thunder Client
├── pom.xml                   → Dependencias Maven
└── README.md
🧠 Autor
👤 Sebas Orrego Lopera
Desarrollador Java | Spring Boot | REST APIs

📧 [Tu correo o portafolio opcional]

🏁 Notas Finales
✔️ Todos los endpoints fueron testeados en Swagger y Thunder Client
✔️ El proyecto está listo para ejecución y evaluación
✔️ Capturas disponibles en la carpeta docs/