![](https://i1.wp.com/jrgonzalez.es/wp-content/uploads/2019/01/git-logo.png?fit=180%2C180&ssl=1)

![](https://github.com/Sebas1130/hyperblog/network/members) ![](https://img.shields.io/github/forks/pandao/editor.md.svg) ![](https://img.shields.io/github/tag/pandao/editor.md.svg) ![](https://img.shields.io/github/release/pandao/editor.md.svg) ![](https://img.shields.io/github/issues/pandao/editor.md.svg) ![](https://img.shields.io/bower/v/editor.md.svg)

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
