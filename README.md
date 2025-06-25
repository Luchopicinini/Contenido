🎬 API de Gestión de Contenido – Cine Plus
Este proyecto es una API REST desarrollada en Java usando Spring Boot, diseñada para gestionar contenido audiovisual — películas, series y documentales — simulando una plataforma de streaming llamada Cine Plus. La API permite crear, consultar, actualizar y eliminar contenido, implementando prácticas modernas como documentación automática con Swagger y navegación HATEOAS para enriquecer las respuestas.

🚀 Objetivos del Proyecto
Construir un microservicio RESTful completo y escalable.

Aplicar una arquitectura limpia y por capas.

Documentar la API automáticamente con Swagger (OpenAPI).

Mejorar la navegabilidad de la API mediante HATEOAS.

Gestionar dependencias y compilación con Maven.

⚙️ Tecnologías Utilizadas
Java 17

Spring Boot

Spring Web

Spring Data JPA

Spring HATEOAS

Swagger (Springdoc OpenAPI)

Maven

H2 Database (base de datos en memoria para desarrollo)

📦 Funcionalidades Principales
Método HTTP	Endpoint	Descripción
GET	/api/contenido	Listar todo el contenido
GET	/api/contenido/{id}	Obtener contenido por ID
POST	/api/contenido	Crear contenido nuevo
PUT	/api/contenido/{id}	Actualizar contenido existente
DELETE	/api/contenido/{id}	Eliminar contenido

🗂️ Estructura del Proyecto y Archivos Clave
Archivos de configuración Maven
.mvn/, mvnw, mvnw.cmd: Scripts para ejecutar Maven sin instalarlo globalmente, asegurando consistencia entre entornos.

pom.xml: Archivo principal de Maven donde se declaran dependencias, plugins y configuraciones de compilación.

Paquete principal: src/main/java/cine/plus/cl/contenido
Organizado siguiendo el patrón MVC y arquitectura en capas:

Carpeta	Función
assemblers	Clases para convertir entidades en representaciones enriquecidas (ej. con HATEOAS).
config	Configuraciones del proyecto (Swagger, seguridad, etc.).
controller	Controladores REST que exponen los endpoints (ContenidoController, ContenidoControllerV2).
model	Clases que representan las entidades del dominio (ej. Contenido.java).
repository	Interfaces que extienden de JpaRepository para acceso a base de datos sin SQL manual.
service	Lógica de negocio que conecta controladores y repositorios.
ContenidoApplication.java	Clase principal con el método main que arranca la aplicación Spring Boot.

Recursos y pruebas
src/main/resources: Archivos de configuración (application.properties), plantillas y recursos estáticos.

src/test: Pruebas unitarias e integradas para validar funcionalidades.

📌 Resumen de Capas y Responsabilidades
Capa	Responsabilidad
Controller	Exponer endpoints REST para interacción con la API
Service	Implementar la lógica de negocio
Repository	Gestionar acceso y manipulación de datos en la base
Model	Representar las entidades y datos del dominio
Assembler	Transformar modelos a DTOs enriquecidos (con HATEOAS)
Config	Configuraciones adicionales como Swagger y seguridad