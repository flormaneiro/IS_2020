
# IS_UCEL
Pagina web de "Ingenieria de software" de UCEL

## Empezando

### Prerequisitos
Con el gestor de paquetes de la distribución de linux utilizada, instalar el siguiente software:
* [Git](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/set-up-git#setting-up-git). Check on Git Bash `git --version`
* [GitHub Desktop](https://desktop.github.com/)
* [Markdownpad](http://markdownpad.com) o [Typora](https://typora.io/)

### Instalación

Descargar el proyecto git en ambiente local:
	- git clone https://github.com/flormaneiro/IS_2020.git 


Probar: http://localhost:9021/cesig/swagger-ui.html



Para correr el servidor desde el eclipse:
1. Ir a la pestaña 'Boot Dashboard'
2. click derecho en 'cesig-service'
3. Open Config
4. Setear:
	- Main type -> coop.tecso.cesig.Application
	- Profile -> local 
5. click derecho en 'cesig-service' y Start

Si en el log no hay ningún error, entrar en la url https://drive.google.com/open?id=1FNZn3xurF6GYh08cKGkvicjcAAHWRhoOqu8YjAiLYoY


## Despliegue
Existe un entorno de desarrollo en el servidor 172.16.17.21. Para este entorno se utiliza integración continua, desencadenada por cada push a la rama *develop* del GIT.
El despliegue en los distintos entornos se hace construyento un archivo war que contiene a la aplicación. Para construir el archivo war desde la línea de comandos:

	- mvn -Dmaven.test.skip=true package  

## Tecnologías

* Spring Boot 1.5.6
* Postgres 9.6


## Configuración de la DB

Para conectarse a la base de datos de desarrollo de tecso, agregar el nombre de hosts: 172.16.17.23 siatdm01d 

Si se desea crear una base de datos local, se debe crear una base de datos en Postgres con el nombre cesig:
	
	CREATE DATABASE cesig-local;
	CREATE USER cesig WITH ENCRYPTED PASSWORD 'yourpass';
	GRANT ALL PRIVILEGES ON DATABASE cesig-local TO cesig;

Para llenar la base de datos se deben correr los scripts que están en la carpeta **cesig-service/src/main/resources/db** y modificar el archivo  **application-local.yml** del proyecto cesig-service, agregando los datos de conexión a la nueva base creada.

## Coding Conventions
[Coding Conventions](./CODINGCONVENTIONS.md)

## Errores Comunes
[Errores Comunes](./COMMONERROR.txt)


## CM
[CM](https://drive.google.com/open?id=1FNZn3xurF6GYh08cKGkvicjcAAHWRhoOqu8YjAiLYoY)


https://jekyllrb.com/docs/usage/




* [Jekyll](https://jekyllrb.com/docs/installation/)
* [Bundler](https://bundler.io/)
* **Jekyll** on CMD `jekyll -v`
* [Bundler](https://bundler.io/)
