1. Dependencias de Spring para el servicio de usuarios:
•	Spring Web: Permite construir aplicaciones web, incluidas aplicaciones RESTful, con el uso de Spring MVC. Incluye herramientas para crear controladores, manejar solicitudes HTTP, y devolver respuestas en distintos formatos, como JSON o XML.
•	Spring Dev Tools: Proporciona herramientas de desarrollo que mejoran la experiencia al programar en Spring, como reinicios automáticos de la aplicación, deshabilitar la caché en vistas, y ofrecer soporte para debugging.
•	Spring Data JPA: Es una parte de Spring Data que simplifica el acceso a bases de datos relacionales usando el API de Java Persistence (JPA). Facilita la creación de repositorios y la realización de operaciones CRUD sin escribir mucho código.
•	MySQL Driver: Permite que la aplicación Spring Boot se conecte a bases de datos MySQL, proporcionando el conector JDBC necesario para comunicarse con la base de datos MySQL.
2. Decoradores en la clase Alumno:
•	@Entity: Indica que la clase es una entidad JPA y que su estado se guardará en la base de datos. Esto significa que cada instancia de esta clase representa una fila en una tabla de la base de datos.
•	@Table: Especifica detalles de la tabla de la base de datos donde se guardará la entidad. Puede incluir el nombre de la tabla, esquemas, y configuraciones adicionales para el mapeo de la tabla en la base de datos.
•	@Id: Identifica el campo que será usado como clave primaria de la entidad.
•	@GeneratedValue: Indica que el valor del campo será generado automáticamente, generalmente para claves primarias que se incrementan de forma automática en la base de datos.
3. @Transactional:
•	El decorador @Transactional en Spring se usa para definir el alcance de una transacción en un método. Las transacciones permiten agrupar operaciones para que se ejecuten como una unidad: si una operación falla, todas las demás pueden revertirse. Existen opciones como readOnly = true para optimizar el rendimiento en métodos de solo lectura y propagation para controlar el comportamiento en transacciones anidadas.
4. Conceptos en Spring Boot:
•	ResponseEntity<?>: Es una clase que representa toda la respuesta HTTP, incluyendo el cuerpo de respuesta, el estado HTTP, y los encabezados. Se usa para personalizar las respuestas devueltas por los controladores, como códigos de error o encabezados personalizados.
•	Optional: Es una clase contenedora que puede o no contener un valor no nulo. Se usa comúnmente para evitar NullPointerException y proporciona métodos funcionales como ifPresent y orElse para trabajar de manera segura con valores opcionales.
•	@PathVariable: Se usa en los métodos de controladores de Spring para capturar variables directamente de la URL. Por ejemplo, en una URL como /alumnos/{id}, el id puede capturarse y usarse en el método.
5. Servidor Eureka en Spring Cloud:
•	Eureka Server: Es un servidor de nombres y descubrimiento de servicios de Netflix, integrado en Spring Cloud. Permite que los microservicios se registren y se descubran mutuamente en un entorno distribuido, mejorando la escalabilidad y la tolerancia a fallos. El servidor Eureka actúa como un directorio de servicios, donde los servicios cliente pueden registrarse y consultarse entre ellos
