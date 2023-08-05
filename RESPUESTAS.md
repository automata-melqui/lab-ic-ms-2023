# Respuestas

Indica tu nombre a continuación: 

Por cada etapa agrega una sección abajo y escribe las respuestas a las preguntas de cada etapa.

## ETAPA 1

¿Cuál es la diferencia entre los archivos con el verbo `Create` con los archivos con el verbo `Add`?
Los archivos Create contienen sentencias SQL DDL y los archivos Add contienen sentencias SQL DML

¿Cómo se llama el servicio que se declara en el archivo `docker-compose.yml`?
El servicio se llama flyway

¿Cuál es el comando que se ejecuta en el servicio declarado?

-locations=filesystem:/flyway/sql -connectRetries=60 migrate

## ETAPA 2

¿Qué pasa si cambias el nombre del servicio de `postgres` a `db`? ¿Qué otros cambios tendrías que hacer?

Se debe modificar el nombre de la dependencia del servicio flyway postgres ==> db
Se debe cambiar la variable de entorno POSTGRES_SERVER ==> db en el archivo .env


...