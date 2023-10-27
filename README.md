# CONTROL DE VERSIONES GIT
## Tarea 1 de la materia control de versiones de la maestría  Diseño Web y Desarrollo de Apps.
#### Autor: Jeniffer Alcívar

## INTRODUCCIÓN AL CONTROL DE VERSIONES Y GIT

El control de versiones es la gestión de los diversos cambios que se realizan sobre los archivos, por lo tanto, de esta forma se obtiene un seguimiento en la evolución de un proyecto. Y Git Hub es una excelente palataforma de hospedaje para el control de estas versiones y colaboración en equipo.  
### CONCEPTOS FUNDAMENTALES DE GIT
**commit:** obtiene los cambios que se han realizado en el proyecto del repositorio.  
**branch (rama):**  es versión del trabajo que se esta desarrollando donde se trabaja de forma independiente sin afectar al proyecto principal del repositorio.  
**head (puntero):**  puntero en la consola para indicar la rama actual a la que se esta apuntando o se realizaron los nuevos commits o cambios en el repositorio.  
**staging area (índice):** es un espacio intermedio donde se pueden revisar y preparar los cambios que se han realizado.


Empezamos accediendo a la carpeta donde utilizaremos git.

### ▪ git init
Este comando es utilizado para iniciar un repositorio git en la carpeta.

La salida de consola es ⬇︎  
Initialized empty Git repository in C:/Tareas de Maestria/.git/


### ▪ git config --global user.name 
Una vez inicializado el git se procede a realizar la configuración de git con este comando para el registro del usuario.

Ingreso en la consola ⬇︎  
git config --global user.name "Jenii23"

### ▪ git config --global user.email
Este comando también forma parte de la configuración, sirve para el registro del email del usuario.

Ingreso en la consola ⬇︎   
git config --global user.email "jenifferal2397@hotmail.com"

### ▪ git config --list
Con este comando puedo revisar la configuración git que tengo registrada.

Entre la extensa lista en la salida de consola respecto a la configuración se encuentra este resultado -> user.name=Jenii23
user.email=jenifferal23972@hotmail.com

### ▪ git status
El git status sirve para obtener información sobre lo que he realizado. 

Se obtiene información como la rama en la que estoy ubicado, si hay o no commits y los archivos que tienen actualizaciones y no han sido subidos a git.

La salida de consola  es ⬇︎

On branch master

No commits yet

Untracked files:  
  (use "git add < file >..." to include in what will be committed)   
        control-versiones-git/

nothing added to commit but untracked files present (use "git add" to track)

### ▪ git add 
Este comando es utilizado para agregar cambios realizados en los archivos. 

Las formas en las que mas se utiliza este comando es  como:

- **git add .** -> es para agregar cambios realizados en el directorio de trabajo.  
- **git add nombredelarchivo** -> es parar agregar al repositorio git un archivo en específico, por lo tando, se indica el comando y el nombre del archivo.  

### ▪ git commit 
Comando utilizado para registrar los cambios realizados en el repositorio. Sin embargo, los cambios deben ser previamente preparados con git add para posteriormente ser guardados con git commit. 

- **git commit -m "descripción del cambio que se está subiendo."** -> Este comando con **-m** permite agregar una breve descripción del cambio que se esta realizando, debe ser lo suficientemente descriptivo para recordar qué cambios se realizaron.

Salida de consola ⬇︎  
![Alt text](image-3.png)
 
Ahora al ejecutar el comando **git status** la salida de consola será diferente ⬇︎

![Alt text](image-2.png)

### ▪ git log 
Con este comando se obtiene un historial de los commit realizados en el repositorio 

Salida de consola ⬇︎   
![Alt text](image-1.png)

### ▪ git diff
Este comando muestra detalladamente lo que ha sido modificado en el archivo. Las líneas con signo **+** son las que se han agregado y los que tienen el signo **-** las eliminadas.

Salida de consola ⬇︎  

![Alt text](image.png)

Para salir de la ejecución de este comando se presiona **q**

## TRABAJO EN EQUIPO CON GIT   
### FLUJO DE TRABAJO TÍPICO  
### ▪ git checkout  
Es un comando utilizado para cambiar entre ramas, ingresando el comando y el nombre de la rama. Pero si se ingresa solo el comando sin ningún otro argumento, muestra la rama actual en la que se está ubicado. Otra forma de utilizar este comando es para crear una nueva rama en el respositorio agregando después del comando **-b** y el nombre de nueva rama.

Salida de consola para obtener la rama en la que se está ubicado con el comando **git checkout** ⬇︎

![Alt text](image-5.png)

Salida de consola para la creación de una nueva rama con el comando **git checkout -b** ⬇︎  

![Alt text](image-4.png)

Salida de consola para cambiar de rama con el comando **git checkout nombre_rama** ⬇︎

![Alt text](image-6.png)

### ▪ git branch
Comando para listar, crear o eliminar ramas en el repositorio git. Si se ejecuta el comando sin ningún argumento se muestra un listado de las ramas existentes e indica en que rama se encuentra posicionado.

Salida de consola para listar las ramas con el comando **git branch** ⬇︎  

![Alt text](image-7.png)

Salida de consola para la creación de una nueva rama con el comando **git branch nombre_rama** ⬇︎   

![Alt text](image-8.png)

Salida de consola para eliminar una rama **git branch -d nombre_rama** ⬇︎  

![Alt text](image-9.png)

### ▪ git merge
Este comando es utilizado para combinar dos ramas en las que se esten desarrollando diferentes versiones.  
Primero se debe estar ubicado en la rama a la que se le va a agregar lo que contiene otra rama y ejecutar el comando seguido del nombre de la rama que se desea combinar. **git merge nombre_rama**.  
Salida de consola al combinar la rama main con la rama JenifferAlcivar/FuncionesPython ⬇︎   

![Alt text](image-11.png)

Por lo tanto, si se ejecuta el comando **git log** podremos ver que ya tenemos un merge de estas dos ramas.  

![Alt text](image-12.png)

### ETIQUETAS Y VERSIONADO SEMÁNTICO

### ▪ git tag
Este comando sirve para crear, listar y eliminar etiquetas que permiten llevar un correcto versionamiento en la historia del repositorio. Extisten varias formas de utilizarlo, entre ellas está utilizar solo el comando **git tag** sin argumentos para obtener una lista de todas las etiquetas registradas. Para crear una nueva etiqueta se debe ingresar el comando **git tag nombre_etiqueta** seguido del nombre de la etiqueta. Por otra parte, si se desea eliminar una etiqueta, se ingresa el comando y se le agrega **-d** seguido del nombre de la etiqueta a eliminar.

Salida de la consola para el comando de crear una nueva etiqueta **git tag nombre_etiqueta** y listar etiqeutas**git tag** ⬇︎  
![Alt text](image-13.png)   

Salida de consola para el comando eliminar etiqueta **git tag -d nombre_etiqueta**     
![Alt text](image-14.png)

En cuanto al versionado semántico es una nomenclatura utilizada para nombrar las versiones. Y el utilizado es X,Y, Z.   
- **X** -> Cuando se realizan modificaciones muy importantes.
- **Y** -> Se agregan nuevas caracteristicas al proyeccto.
- **Z** -> Cuando solo se relizan cambios menores.

### ▪ .gitinigore  
Es un archivo de texto utilizado para especificar archivos que no deben ser rastreados o ingorados por el controlador de versiones. Para crear un archivo .gitignore, simplemente se crea un archivo llamado **.gitignore** en la raíz del repositorio y se agregan los patrones que se desean ignorar.

![Alt text](image-15.png)  

Posteriormente se verifica tener una carpeta donde se encuentre almacenado los archivos que solo se quieren mantener localmente y sean ignorados por git. Para este ejemplo se tiene la carpeta **/logs**  

![Alt text](image-16.png)

Ahora se ignora esta carpeta en el archivo **.gitignore**  indicando el nombre de la carpeta con un **/** para hacer referencia que se está indicando una carpeta. De esta forma todos los archivos que pertenezcan a esta carpeta seran ignorados.

![Alt text](image-17.png)

Pero si se trata de solo ignorar un archivo, basta con solo indicar el nombre del archivo con su extensión en una línea del **.gitignore**.

![Alt text](image-18.png)

### HOOKS DE GIT Y AUTOMATIZACIÓN DE TAREAS

### ▪ hooks
Son scripts que se ejecutan automaticamente cuando ocurre un evento en el repositorio git. Permiten una personalización del comportamiento interno de git y desencadenar acciones personalizadas. Los hooks se almacenan en el subdirectorio hooks del directorio, en **.git/hooks** siendo **.git** una carpeta que viene oculta en el repositorio.

Para ver los hooks se accede primero a la carpeta oculta **.git** y dentro de ella se lista los archivos. 

![Alt text](image-19.png)

Dentro estará la carpeta **hooks** y posteriormente los hooks que se encuentran previamente almacenados.

![Alt text](image-20.png)

## GIT AVANZADO  
### ▪ git rebase
Este comando se utiliza para integrar cambios de una rama a otra, logrando así modificar la historia del proyecto. Si realizamos una comparación con merge, se puede decir que el git rebase si modifica el hisotrial. Es utilizado para lidiar con errores de push, cambiar la base de una rama y agrupar varios commits que esten relacionados con la misma funcion o corrección de errores.

Se realiza un commit.  
 
![Alt text](image-21.png)

Se verifica el log de esta rama.  

![Alt text](image-22.png)

Y el log de la rama principal main.  
 
![Alt text](image-23.png) 

Entonces hay que ubicarse en la rama donde se realizó el commit y posteriormente hacerle un rebase al main.

![Alt text](image-24.png) 

Se ejecuta git log nuevamente y se obtiene un nuevo resultado.

![Alt text](image-25.png)

Ahora tiene los commit de main mas el commit que había realizado en la rama.


- **git rebase -i**: Entre los otros comandos de **git rebase** se encuentra el **git rebase -i**, utilizado para interectuar con los commits. Cuando se ejecuta este comando se obtiene un editor de texto del commit indicado al cual se le puede cambiar el orden, fusionarlo, eliminar, entre otras acciones.   
Para utilizar esta variante del git rebase, se debe indicar en la consola el comando seguido del id del commit.  
![Alt text](image-26.png)  

A continuación, se abre un editor de texto en la consola del sistema.

![Alt text](image-27.png)  

Se obtiene el nombre del commit y los comandos que se pueden utilizar en él. En este caso edito el pick y le indico la **r** para editar el mensaje del commit y guardo.

![Alt text](image-28.png)

Ahora se tiene acceso a editar el mensaje, por lo tanto, se modifica y guarda.  

![Alt text](image-29.png)  

Ahora al ejecutar git log se puede ver el nombre del commit modificado.

![Alt text](image-30.png)

Se realiza el mismo proceso para fusionar, eliminar y entre otras opciones que aparecen disponibles al ejecutar el **git rebase -i**.

### ▪ git stash  
Este comando permite almacenar cambios locales temporalmente. Es muy útil para esos cambios en los archivos que no se les quiere hacer un commit en el repositorio git.  
Primero debe estar desarrollado lo que se quiere mantener localmente y ejecutar el comando. 

![Alt text](image-32.png)  

- **git stash list**: Para listar los stash almacenados, solo se debe ejeuctar el comando seguido de **list**.  
![Alt text](image-33.png)

- **git stash pop**: Permite recuperar el último stash y aplicarlo a la rama actual.  

  ![Alt text](image-34.png) 

- **git stash apply stash@{0}**: Permite aplicar los cambios del último stash guardado.

- **git stash pop stash@{0}**: Permite recuperar el último stash y aplicarlo a la rama actual.


### ▪ git cherry-pick
Este comando permite aplicar los cambios introducidos por uno o más commits a otra rama. Para utilizar este comando primero se debe cambiar a la rama destino y luego ejecutar el comando **git cherry-pick <commit>**, donde **<commit>** es el hash del commit que se quiere aplicar.



### ▪ git revert

