# Evaluación: Plataforma de Procesamiento de Transacciones

Este proyecto consta de tres componentes principales:

1. **API de Recepción y Desencriptado (Java Spring Boot - API 1)**  
2. **API de Procesamiento Interno (Java Spring Boot - API 2)**  
3. **Frontend Angular para ingresar transacciones**

---

## 🔧 Requisitos Previos

- Java 17
- Maven 3.8+
- Node.js v20.11+
- Angular CLI (`npm install -g @angular/cli`)
- IDE sugerido: IntelliJ IDEA / VS Code

---

## 🚀 Ejecución de las APIs

### ✅ API 1 - Recepción y Desencriptado

1. Ubícate en la carpeta del proyecto (por ejemplo: `api-recepcion`).
2. Ejecuta:

```bash
./mvnw spring-boot:run
```

_El servicio se levantará en_ `http://localhost:8080`

#### Endpoint Principal:
- POST `/api/procesar`  
  Recibe datos cifrados desde el frontend.

---

### ✅ API 2 - Procesamiento Interno

1. Ubícate en la carpeta de la segunda API (por ejemplo: `api-procesador`).
2. Ejecuta:

```bash
./mvnw spring-boot:run
```

_El servicio se levantará en_ `http://localhost:8081`


---

## 🌐 Ejecución del Frontend Angular

1. Ubícate en la carpeta `frontend-aes`.
2. Instala dependencias:

```bash
npm install
```

3. Ejecuta el servidor de desarrollo:

```bash
ng serve
```

4. Abre tu navegador en: [http://localhost:4200](http://localhost:4200)


---

## 🧪 Pruebas con Postman

Puedes probar directamente el backend con:

### API 1
- URL: `http://localhost:8080/api/procesar`
- Método: `POST`
- Headers:
  - `Content-Type: application/json`
- Body (ejemplo cifrado):

```json
{
  "operacion": "venta",
  "importe": "1000",
  "cliente": "Juan Pérez",
  "secreto": "<texto cifrado AES>"
}
```

