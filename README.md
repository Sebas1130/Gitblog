![](https://i1.wp.com/jrgonzalez.es/wp-content/uploads/2019/01/git-logo.png?fit=180%2C180&ssl=1)


# MODULO #1 COMANDOS BASICOS DE GIT 

#####  LAS CLASES ANTERIORES SOLO SON PRATICAS DE COMO CONFIGURAR Y DESCARGAR TU EDITOR DE CODIGO 

#### CLASE 
  
  * COMO CONFIGURAR MI GIT Y INICIALIZAR MI REPOSITORIO 

* Ciclo de vida o estados de los archivos en Git:

#####  Cuando trabajamos con Git nuestros archivos pueden vivir y moverse entre 4 diferentes estados 
 * (cuando trabajamos con repositorios remotos pueden ser más estados, pero lo estudiaremos más adelante):

#####  El primero comando para utilizar es :
	$ git init :  

Este hc que git se inicie en el repositorio .
En otras palabras le da a entender a git que este el el archivo que tiene que seguir y en donde se van a hacer cambios normal mente se hc en la primera carpeta del arhivo para que le pueda hacer seguimiento a todo la app o archivo que estes manejando 

#####  El segundo comando es
	$ git status   
Este indica el estado en que se encuentra tu app o archivo que estes monitoreando .
En pocas palabras si se le hacen cambios,  si se hace referencia a otros comandos dependiendo el estado de tu archivo. Si se le han echo  cambios te indicara que se le debe hacer un git add , y si el archivo no ha sufrido cambios te indicara que el archivo sigue igual y que esta esperando un cambio 


##### El tercer comando es :

	$ git add  
Este comando nos sirve para indicarle a git que han ocurrido unos cambios y que nesesitamos guardar. Pero estos cambios quedan guardados en la memoria ram de tu pc aqui todavia no se han guardado en Git. Aqui los cambios  se encuentrar en staging y se liberaran con el siguiente comando que espera  git a que realises que es  
 
 	$ git commit -m 
   

 El cuarto comando es Uno de los mas importantes ya que con el mandamos ya directamente los cambios a un repositorio de git en la nube o en la web ya aqui git hc se encarga de administrar el archivo y puedes acceder a ellos cuando quieras y ver los cambio que se 
 han echo con el Comando
 
 	$git log nombre_archivo

##### ¿ Que son los archivos traqueados ?

 Los Archivos Tracked son los archivos que viven dentro de Git, no tienen cambios pendientes y sus últimas actualizaciones han sido guardadas en el repositorio gracias a los comandos 
 
 	$ git add 
	$ git commit.
	
####   VOLVER EN EL TIEMPO EN NUESTRO REPOSITORIO UTILIZANDO REST Y CHECKOUT 
 El Comando git checkout + ID del Commit nos permite viajar en el tiempo. Podemos volver a cualquier verison anterior de un archivo especifico o incluso del proyecto entero. Esta tambien es la forma de crear ramas y movernos entre ellas .

#####  Hay dos formas de usar git reset 
El primero el git reset t --hard. Este borra toda la informacion que tengamos en el area de satging (perdiendo todo para siempre borrandolo)

 	$ git reset + ID commit --hard
El segundo comando es  git reset  --soft ES un poco mas seguro por que que mantien alli los archivos del area de staging para que podamos aplicar nuestros ultimos cambios pero desde un commit anterior

	$ git reset + ID commit --soft

##### GIT RESET VS GIT RM 

	$ git rm
Este comando nos ayuda a eliminar archivos de Git sin eliminar su historial del sistema de versiones. Esto quiere decir que si necesitamos recuperar el archivo solo debemos “viajar en el tiempo” y recuperar el último commit antes de borrar el archivo en cuestión.

Recuerda que git rm no puede usarse así nomás. Debemos usar uno de los flags para indicarle a Git cómo eliminar los archivos que ya no necesitamos en la última versión del proyecto:

	$ git rm --cached 
Elimina los archivos del área de Staging y del próximo commit pero los mantiene en nuestro disco duro.

	$ git rm --force 
Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).

	$ git diff  
Sirve para ver los cambios realizados a un archivo despues de hacerle commit o hacerle un git add muestra los cambios cuantos cambios se realizaron, quien los realizo y tambien la fecha. 

# MODULO #2  
##### FLUJO DE TRABAJO BASICO CON UN REPOSITORIO REMOTO 

Lo primero que debes hacer es traer el repositorio del servidor donde esta montado una copia eso lo puedes hacer com :

	$ git clone 
Esto traera una copia de los archivos a tu area de trabajo y a tu repositorio local 

	$ git clone + url_del_servidor_remoto  
Sirve para clonar un repositorio lo trae y coloca una copia en el area de trabajo y otra en el repositorio local 

	$ git push 
Luego de hacer git add y git commit debemos ejecutar este comando para mandar los cambios al servidor remoto. Pero que pasa si Desde el servidor remoto hacen una actulizacion tendras que volver a hacer el proceso de traerlo con el git clone y todo te cuento que no hay un comando que nos hace la vida mas facil ese es el comando git fecht.

	$ git fetch 
Lo usamos para traer actualizaciones del servidor remoto y guardarlas en nuestro repositorio local (en caso de que hayan, por supuesto).

Pero Git fecht solo trae los cambios al area de trabajo ahora toca volver a mandarlos al repositorio local y al staging area eso lo podemos solucionar con el siguiente 
comando

	$ git merge 
También usamos el comando git merge con servidores remotos. Lo necesitamos para combinar los últimos cambios del servidor remoto y nuestro directorio de trabajo.

	$ git pull 
Básicamente, git fetch y git merge al mismo tiempo.

##### PASOS PARA CONECTARTE CON EL SERVIDOR REMOTO CON NOMBRE ORIGIN 

Primero: Guardar la URL del repositorio de GitHub con el nombre de origin.
 El comando es el siguiente para guardar el repositorio origin:
 
 	$ git remote add origin URL.

Segundo: Verificar que la URL se haya guardado correctamente:

	$ git remote
	$ git remote -v

 Tercero: Traer la versión del repositorio remoto y hacer merge para crear un commit con los archivos de ambas partes. Podemos usar git fetch y git merge o solo el git pull con el 
 flag --allow-unrelated-histories:
 
	
	$ git pull origin master --allow-unrelated-histories

 Por último, ahora sí podemos hacer git push para guardar los cambios de nuestro repositorio local en GitHub:
 
	$ git push origin master
