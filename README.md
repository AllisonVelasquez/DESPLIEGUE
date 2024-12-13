# DESPLIEGUE

## DOCKER
Gestor de servicios/procesos pero mas eficiente.
...

### Contenedor =Proceso

```
node -->, tambien para entornos.
```

## DOCKERFILE 

Esta en la carpeta padre del proyecto y debe contener:
node.. ------------- (importa mucho la version) poruqe es la que estamos usando
copy . . 
expose 5000
ejectuamos npm start --------- node usa npm (gestor de libreria) controla dependencias usa package.json
Se pueden levantan por individual

## DOCKERCOMPOSE
No hay aplicacion que tenga solo un contenedor, se necesita un orquestador. Tambien se pueden crear redes
Si queremos levantar mas contenedores, se cambia el nombre y se añade, se configura la red y añades una variable de entorno para que se modifique antes de compilarse

## Levantar los contenedores

```
docker compose build
docker compose up -d
```

### extras:
codigo en caso de errores para borrar todo

```
docker rm -f $(docker ps -aq)
docker rmi -f $(docker images -q)
docker network prune -f
```
