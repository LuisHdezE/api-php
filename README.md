API RESTful en PHP para administrar bases de datos MySQL
Esta API RESTful escrita en PHP puro permite administrar cualquier base de datos MySQL simplemente cambiando los parámetros de conexión. Se utiliza PDO para gestionar la base de datos y la estructura sigue el patrón Modelo-Vista-Controlador (MVC).

Requisitos
PHP 7.0 o superior
Extensión PDO para PHP
Base de datos MySQL
Instalación
Descarga o clona el repositorio de la API en tu servidor o en tu ordenador local.

Abre el archivo config.php y modifica los parámetros de conexión para que se correspondan con los de tu base de datos MySQL.

php
Copy code
define('DB_HOST', 'localhost');
define('DB_NAME', 'database_name');
define('DB_USER', 'database_user');
define('DB_PASS', 'database_password');
Importa el archivo database.sql en tu base de datos MySQL para crear la tabla users y poblarla con algunos datos de prueba.

Abre un navegador web y accede a la API en la URL correspondiente. Por ejemplo, si has instalado la API en la raíz de tu servidor web, la URL sería http://localhost/.

Uso
La API cuenta con los siguientes endpoints:

GET /users: Devuelve la lista de todos los usuarios en la base de datos.
GET /users/:id: Devuelve los datos del usuario con el identificador especificado en :id.
POST /users: Crea un nuevo usuario en la base de datos.
PUT /users/:id: Actualiza los datos del usuario con el identificador especificado en :id.
DELETE /users/:id: Elimina el usuario con el identificador especificado en :id.
Para probar la API, puedes utilizar una herramienta como Postman o simplemente acceder a los endpoints en un navegador web. Por ejemplo, para obtener la lista de usuarios, accede a http://localhost/users. Para crear un nuevo usuario, envía una solicitud POST a http://localhost/users con los datos del usuario en formato JSON en el cuerpo de la solicitud.

Estructura del proyecto
El proyecto sigue la estructura típica de un proyecto PHP MVC:

index.php: El archivo principal de la API, que enruta las solicitudes a los controladores correspondientes.
config.php: El archivo de configuración que contiene los parámetros de conexión a la base de datos.
controllers/: El directorio que contiene los controladores de la API, que gestionan las solicitudes y las respuestas HTTP.
models/: El directorio que contiene los modelos de la API, que interactúan con la base de datos a través de PDO.
views/: El directorio que contiene las vistas de la API, que generan las respuestas HTML o JSON a las solicitudes.
Contribuir
Si deseas contribuir a la API, puedes enviar un pull request o abrir un issue en el repositorio de GitHub. Agradecemos cualquier contribución o sugerencia para mejorar la API.