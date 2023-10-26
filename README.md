# CONTROL DE VERSIONES GIT
## Tarea 1 de la materia control de versiones de la maestría  Diseño Web y Desarrollo de Apps.
#### Autor: Jeniffer Alcívar

## INTRODUCCIÓN AL CONTROL DE VERSIONES Y GIT

El control de versiones es la gestión de los diversos cambios que se realizan sobre los archivos, por lo tanto, de esta forma se obtiene un seguimiento en la evolución de un proyecto. Y Git Hub es una excelente palataforma de hospedaje para el control de estas versiones y colaboración en equipo.

Empezamos accediendo a la carpeta donde utilizaremos git.

### git init
Este comando es utilizado para iniciar un repositorio git en la carpeta.

La salida de consola es -> Initialized empty Git repository in C:/Tareas de Maestria/.git/


### git config --global user.name 
Una vez inicializado el git se procede a realizar la configuración de git con este comando para el registro del usuario.

Ingreso en la consola -> git config --global user.name "Jenii23"

### git config --global user.email
Este comando también forma parte de la configuración, sirve para el registro del email del usuario.

Ingreso en la consola -> git config --global user.email "jenifferal2397@hotmail.com"

### git config --list
Con este comando puedo revisar la configuración git que tengo registrada.

Entre la extensa lista en la salida de consola respecto a la configuración se encuentra este resultado -> user.name=Jenii23
user.email=jenifferal23972@hotmail.com

### git status
El git status sirve para obtener información sobre lo que he realizado. 

Se obtiene información como la rama en la que estoy ubicado, si hay o no commits y los archivos que tienen actualizaciones y no han sido subidos a git.

La salida de consola  es ⬇︎

On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        control-versiones-git/

nothing added to commit but untracked files present (use "git add" to track)

### git add 
Este comando es utilizado para agregar cambios realizados en los archivos. 

Las formas en las que mas se utiliza este comando es  como:

**- git add .** -> es para agregar cambios realizados en el directorio de trabajo.

**- git add nombredelarchivo** -> es parar agregar al repositorio git un archivo en específico, por lo tando, se indica el comando y el nombre del archivo.

### git commit 
Comando utilizado para registrar los cambios realizados en el repositorio. Sin embargo, los cambios deben ser previamente preparados con git add para posteriormente ser guardados con git commit. 

**- git commit -m "descripción del cambio que se está subiendo."** -> Este comando con **-m** permite agregar una breve descripción del cambio que se esta realizando, debe ser lo suficientemente descriptivo para recordar qué cambios se realizaron.

Salida de consola ⬇︎
[master (root-commit) 37a123b] subiendo la tarea
 1 file changed, 1 insertion(+)
 create mode 160000 control-versiones-git
 
Ahora al ejecutar el comando **git status** 




