# User Service

Microservicio para la gestión de usuarios de Perfulandia.

## Requisitos

- Java 17+
- Maven 3.9+
- MySQL corriendo (por defecto en XAMPP) con la base de datos `db_perfulandia`

## Configuración

1. Clona o descomprime este proyecto.
2. Crea la base de datos en MySQL (XAMPP):
   ```sql
   CREATE DATABASE IF NOT EXISTS db_perfulandia;
   ```
3. En `src/main/resources/application.properties`, ajusta usuario/contraseña si es necesario.

## Ejecutar

```bash
mvn clean install
mvn spring-boot:run
```

El servicio levantará en `http://localhost:8080`.

## Endpoints

- `POST /api/v1/users`  
  Crear un usuario.  
  ```json
  {
    "username": "johndoe",
    "password": "secret",
    "email": "john@example.com",
    "role": "USER"
  }
  ```

- `GET /api/v1/users/{id}`  
  Obtener por ID.

- `GET /api/v1/users/username/{username}`  
  Obtener por nombre.

- `DELETE /api/v1/users/{id}`  
  Eliminar.
