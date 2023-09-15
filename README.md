# turbotraffic API

# coleccion de Postman

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/20082346-bc29e6b0-254a-43ee-bb21-a18ea354c0ba?action=collection%2Ffork&source=rip_markdown&collection-url=entityId%3D20082346-bc29e6b0-254a-43ee-bb21-a18ea354c0ba%26entityType%3Dcollection%26workspaceId%3D3fc380d8-cc70-4f32-8659-3199f494a889)

# clonacion del repositorio e inicializacion de los submodulos

```bash
git clone git@github.com:gabrielcontrerasv/turbotraffic.git
cd turbotraffic 
git submodule init
git submodule update --recursive
git submodule update --remote
```
## conexion de dos microservicios usando mongoose 

para construir la aplicacion ejecute el siguiente comando estando en la ruta de la carpeta del proyecto.

```bash
docker-compose up
```

este comando ejecutara la creacion de los microservicio y los conectara mediante las rutas que estan establecidas en el docker-composer-yml apuntando a cada app

## informacion importante. puertos y configuraciones establecidas a nivel global

- microservicio 1 : get_info_app opera en el puerto 3000 interno 3000
- microservicio 2 : set_info_app opera en el puerto 3000 interno 3001 externo
- microservicio 3 : mongodb opera en el puerto 27017 interno y 27018 externo 

## como acceder a los microservicios via http ##

para visualizar como se exponen se abre un navegador y se escribe en la barra de direcciones localhost:3000 o localhost:3001 esto se expone con el objetivo de poderlo visualizar desde el navegador, sin embargo no es necesario el navegador para validar los resultados

## comprobar mediante postman

- cree una peticion http de tipo post con el objetivo de enviar los datos.

## recomendaciones ##

1. defina los encabezados como application/json
2. seleccione el checkbox raw
3. al final de la seccion seleccion en la lista desplegable la opcion json
2. en el body de la peticion debe enviar un objeto con la siguiente estructura
```bash
{
    data: "contenido del campo a almacenar"
}
```
 importante el campo debe ser un string pues tiene validaciones 

# comprobacion de los resultados 


## mediante un gestor de base de datos que puede descargarlo para su sistema operativo de preferencia

1. descargue el gestor de base de datos desde esta web https://www.mongodb.com/try/download/compass
2. instalelo en el computador donde esta ejecutando del docker-compose.yml
3. conectese por medio del puerto que se determinó (27018)
4. cree la base datos para que los microservicios puedan almacenar la informacion








