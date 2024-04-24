# Afianzar-conocimientos-Docker

Integrantes:

Salomé Acosta Montaño: 2242581
Salome.acosta@correounivalle.edu.co

Emily Nuñez Ordoñez: 2240156
Emily.nunez@correounivalle.edu.co

Sara Yineth Suárez Reyes: 2241923
Sara.suarez@correounivalle.edu.co

Sheila Marcela Valencia Chito: 2243011
Sheila.valencia@correounivalle.edu.co

Victoria Andrea Volverás Parra: 2241874
Victoria.volveras@correounivalle.edu.co

Link al video en YouTube: https://youtu.be/sGWvWWmUoM8

Descripción de la tarea:

Se crea una red de Docker llamada "pg_network", un volumen llamado "pg_db" para almacenar los datos de la base de datos "tarea_db" y se ejecuta un contenedor de PostreSQL conectado a la red, utilizando el volumen para almacenar los datos. También se establecen variables de entorno para configurar la base de datos, su usuario y contraseña. Usa la imagen versión 15 etiquetada como "15-bookworm".

Se ejecuta otro contenedor de PostreSQL, llamado "pg_client" conectado a la misma red "pg_network" y que también utililza el volumen "pg_db", para compartir los mismos datos de la base de datos que el servidor. Para este contenedor se utiliza la imagen de PostreSQL versión 15.

Se realiza la verificación de que los contenedores, volúmenes y redes se crearon correctamente, y dentro de "pg_server", conectado a la base de datos "tarea_db", se crea la tabla "pg_tabla", se inserta un registro y se consulta para verificar que los datos se hayan guardado. Luego, se conecta al servidor desde el contenedor del cliente y se verifica que los datos se puedan acceder también desde allí.

En pocas palabras, "pg_server" actúa como el servidor de la base de datos y "pg_client" se utiliza para interactuar con el servidor desde una perspectiva cliente; ambos pueden acceder a la información de la base de datos.

Se detienen y eliminan los contenedores creados y se eliminan el volumen y la red utilizados.