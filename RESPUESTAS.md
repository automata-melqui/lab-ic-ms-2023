# Respuestas

Indica tu nombre a continuación: 

Por cada etapa agrega una sección abajo y escribe las respuestas a las preguntas de cada etapa.

## ETAPA 1

¿Cuál es la diferencia entre los archivos con el verbo `Create` con los archivos con el verbo `Add`?
Los archivos Create contienen sentencias SQL DDL para crear tablas y los archivos Add contienen sentencias SQL DML para agregar registros en las tablas creadas.

¿Cómo se llama el servicio que se declara en el archivo `docker-compose.yml`?

El servicio se llama flyway.

¿Cuál es el comando que se ejecuta en el servicio declarado?

-locations=filesystem:/flyway/sql -connectRetries=60 migrate

## ETAPA 2

¿Qué pasa si cambias el nombre del servicio de `postgres` a `db`? ¿Qué otros cambios tendrías que hacer?

Se debe modificar el nombre de la dependencia del servicio flyway postgres ==> db
Se debe cambiar la variable de entorno POSTGRES_SERVER ==> db en el archivo .env

## ETAPA 3

¿Qué te llama la atención?

Que la estructura del archivo define comandos a ejecutar en 2 etapas `build` y `deployment` además define un usuario no root por seguridad (según lo visto en clases).

¿Cómo se relacionan el archivo `docker-compose.yml` y el archivo `movies-api/Dockerfile`?

Que el archivo `docker-compose.yml` levanta un contenedor utilizando las instrucciones(comandos) descritos en el archivo `Dockerfile` dentro de la carpeta `movies-api`.

¿Qué crees que hace el atributo `context` debajo de `build` (está en la linea 6 del archivo `docker-compose.yml`)?

Agrega otra raíz o path donde debe existir un `Dockerfile` para generar un contenedor.
...