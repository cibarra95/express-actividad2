#Install packages
``` npm install && npm run dev```

#Actividad 2
Se pide diseñar e implementar el API CRUD para un modelo "Post" que de servicio a parte de la colección Postman con la que venimos trabajando.
1. Diseño modelo
Diseñar un modelo Mongoose de "Post" con al menos los siguientes campos y validaciones en su esquema:
- id: string
- createdAt: Date
- updatedAt: Date
- title: string, requerido, más de 5 caracteres
- text: string, requerido, más de 5 caracteres
- author: string, requerido

1. Diseño API CRUD HTTP
Codificar los siguientes endpoints de acceso público (sin autenticación necesaria)
1. POST /api/posts
- Recibe body JSON con los campos title, text y author.
- Devuelve HTTP 201 con el detalle JSON del Post creado en la Base de Datos en memoria
- Devuelve HTTP 400 si hay errores en la validación del body de la petición contra el esquema definido

2. GET /api/posts
- Devuelve HTTP 200 OK con el listado JSON de posts almacenados en la Base de Datos en memoria

3. GET /api/posts/<id>
- Devuelve 200 OK con detalle de un Post JSON almacenado en la Base de Datos en memoria
- Devuelve 404 si el post no existe en la Base de Datos en memoria

4. PATCH /api/posts/<id>
- Recibe body JSON con alguno de los campos title, text y author.
- Devuelve 200 OK con detalle de un Post JSON almacenado en la Base de Datos en memoria tras modificar sus atributos con lo indicado en el body
- Devuelve 404 si el post no existe en la Base de Datos en memoria

5. DELETE /api/posts/<id>
- Devuelve HTTP 204 tras eliminar el post id == <id> de la Base de Datos en memoria
- Devuelve 404 si el post no existe en la Base de Datos en memoria

Entrega
repositorio git público que contenga proyecto node.js excluyendo el directorio node_modules.
El comando "npm start" debe ejecutar un servidor express.js en el puerto 8000.
El entregable debe contener una colección exportada desde Postman que consuma el api desarrollado
Se deberá adjuntar un video de corta duración con una grabación de pantalla donde el alumno haga una breve demostración de la aplicación resultante, explicando además el código desarrollado sobre el editor de código y mostrando las peticiones sobre postman
