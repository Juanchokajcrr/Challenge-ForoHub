# Challenge-ForoHub
Implementacion de Java y Spring para la creacion del Back-End de un foro llamado - Foro Hub.

Here is a detailed and well-structured `README.md` for your project. It covers description, setup, usage, technologies, and more.

# Api-foroH

## Descripción

Api-foroH es una API RESTful desarrollada con Spring Boot para gestionar una aplicación de foro. Proporciona endpoints para autenticación de usuarios, publicación de temas, comentarios y más. El backend utiliza MySQL para la persistencia de datos y JWT para autenticación segura.

## Características

- Registro y autenticación de usuarios (JWT)
- Crear, leer, actualizar y eliminar temas del foro
- Comentar en los temas
- Control de acceso basado en roles
- Manejo de errores con respuestas personalizadas

## Tecnologías

- Java 17+
- Spring Boot
- Spring Security (JWT)
- MySQL
- Maven
- Hibernate/JPA

## Primeros pasos

### Requisitos previos

- Java 17 o superior
- Maven
- Servidor MySQL

### Variables de entorno

Configura las siguientes variables de entorno o en `src/main/resources/application.properties`:

- `DB_HOST`: Host de MySQL (ejemplo: `localhost:3306`)
- `DB_PASSWORD`: Contraseña de root de MySQL
- `JWT_SECRET`: Clave secreta para generación de tokens JWT

### Instalación

1. Clona el repositorio:
   ```sh
   git clone https://github.com/your-username/api-foroH.git
   cd api-foroH
   ```

2. Configura la base de datos:
   - Crea una base de datos MySQL llamada `foroH`.
   - Actualiza `application.properties` con tus credenciales.

3. Compila el proyecto:
   ```sh
   mvn clean install
   ```

4. Ejecuta la aplicación:
   ```sh
   mvn spring-boot:run
   ```

## Endpoints de la API

| Método | Endpoint                  | Descripción                  | Requiere Auth |
|--------|---------------------------|------------------------------|---------------|
| POST   | `/auth/register`          | Registrar nuevo usuario      | No            |
| POST   | `/auth/login`             | Login y obtener token JWT    | No            |
| GET    | `/topics`                 | Listar todos los temas       | Sí            |
| POST   | `/topics`                 | Crear nuevo tema             | Sí            |
| GET    | `/topics/{id}`            | Obtener detalles de un tema  | Sí            |
| POST   | `/topics/{id}/comments`   | Agregar comentario al tema   | Sí            |

## Uso

- Utiliza un cliente API (ejemplo: Postman) para interactuar con los endpoints.
- Autentícate usando el token JWT en el header `Authorization`:
  `Authorization: Bearer <token>`

## Esquema de la base de datos

- `users`: Credenciales y roles de usuario
- `topics`: Temas del foro
- `comments`: Comentarios en los temas

## Pruebas

Ejecuta las pruebas unitarias e integrales con:

```sh
mvn test
```

## Licencia

Este proyecto está bajo la licencia MIT.

## Autor

- [Juanchokajcrr](https://github.com/Juanchokajcrr)
```
