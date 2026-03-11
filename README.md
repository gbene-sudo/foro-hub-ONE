# Foro Hub ONE

API REST desarrollada en **Java con Spring Boot** que simula el funcionamiento básico de un foro de discusión.  
El sistema permite crear, consultar, actualizar y eliminar tópicos dentro de un foro, gestionando la información mediante una base de datos relacional.

Este proyecto fue desarrollado como parte del **challenge del programa Oracle Next Education (ONE) - Backend**.

---

# Tecnologías utilizadas

- Java 17
- Spring Boot
- Spring Data JPA
- Hibernate
- MySQL / H2
- Maven
- REST API
- Postman / Insomnia para pruebas

---

# Funcionalidades

La API permite realizar las siguientes operaciones:

## Tópicos

- Crear un nuevo tópico
- Listar todos los tópicos
- Consultar un tópico específico por ID
- Actualizar un tópico existente
- Eliminar un tópico

Cada tópico contiene información como:

- Título
- Mensaje
- Autor
- Curso
- Fecha de creación

---

# Estructura del proyecto

```
foro-hub
│
├── controller
│   └── TopicController
│
├── model
│   └── Topic
│
├── repository
│   └── TopicRepository
│
├── service
│   └── TopicService
│
├── dto
│   └── TopicDTO
│
└── ForoHubApplication
```

Esta arquitectura sigue una separación de responsabilidades típica de aplicaciones **Spring Boot**:

- **Controller** → maneja las peticiones HTTP  
- **Service** → contiene la lógica de negocio  
- **Repository** → acceso a la base de datos  
- **Model** → entidades del sistema  
- **DTO** → transferencia de datos entre capas

---

# Instalación y ejecución

## 1. Clonar el repositorio

```bash
git clone https://github.com/gbene-sudo/foro-hub-ONE.git
```

## 2. Entrar en la carpeta del proyecto

```bash
cd foro-hub-ONE
```

## 3. Ejecutar la aplicación

Con Maven:

```bash
mvn spring-boot:run
```

O desde tu IDE (IntelliJ / Eclipse) ejecutando la clase:

```
ForoHubApplication
```

---

# Endpoints principales

| Método | Endpoint | Descripción |
|------|------|------|
| GET | /topicos | Lista todos los tópicos |
| GET | /topicos/{id} | Obtiene un tópico por ID |
| POST | /topicos | Crea un nuevo tópico |
| PUT | /topicos/{id} | Actualiza un tópico |
| DELETE | /topicos/{id} | Elimina un tópico |

---

# Ejemplo de request

### Crear un tópico

POST `/topicos`

```json
{
  "titulo": "Error con Spring Boot",
  "mensaje": "No puedo iniciar mi aplicación",
  "autor": "Nombre",
  "curso": "Spring Boot"
}
```

---

# Pruebas de la API

Podés probar los endpoints usando:

- Postman
- Insomnia
- cURL

Ejemplo:

```bash
curl http://localhost:8080/topicos
```

---

# Mejoras futuras

- Autenticación con **Spring Security + JWT**
- Paginación de resultados
- Validaciones con **Bean Validation**
- Sistema de usuarios
- Documentación con **Swagger / OpenAPI**

---

# Autor

**Gaspar Benegas**

GitHub:  
https://github.com/gbene-sudo
