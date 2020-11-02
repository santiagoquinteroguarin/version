## Comandos De GIT 🤩

* ls -al --> lista todos los archivos y los ocultos
* history --> muestra el historial de comandos utilizados
* git rm -R file-name --> eliminar un archivo o un directorio
* git rm --cached file-name --> remueve archivos del staging en git pero no del disco
* git rm --force --> remueve los archivos del stagin y del disco
* cat file-name --> muestra el contenido del archivo en la terminal
* git log --> historial de commit en los archivos
* git show file-name --> muestra los cambios realizados desde el inicio
* git show --> nos muestra en que rama estamos
* git diff #hash del commit --> compara los cambios del ultimo commit con anteriores o dos commit 
* git reset HEAD --> saca los archivos del staging y listo
* git reset #hash del commit --soft --> vuelve a los cambios de ese commit pero lo que este en stagin se mantendra
* git reset #hash del commit --hard --> vuelve a esa version
* git pull origin master--> trae los ultimos cambios del servidor remoto
* git branch name-rama --> crea una rama con una copia del ultimo commit de master
* git checkout name-rama --> migrar de una rama a otra
* git merge nombre-rama --> hacer la unión de las ramas siempre desde master
* git log --all --graph --decorate --oneline --> ver el historial del proyecto
* alias tree="git log --all --graph --decorate --oneline" --> generar alias
* git tag -a v0.1 -m "Message" --> crear un tag para un punto de historia
* git tag --> ver tags
* git tag -d nombretag --> eliminar tag
* git push origin --tags --> mandar tags al remoto
* git push origin :refs/tags/nombretag --> borrar tags del remoto
* git push origin otherrama --> mandar otra rama al remoto
* git log --graph --> historia
* git commit --amend --> si mandaste un cambio a staging y creaste un commit y te falto algun cambio por hacer, lo haces lo agregas y con este comando agregas ese nuevo cambio a ese commit anterios
* git grep palabraparabuscar


## El flujo de un pull request

Se trabaja en una rama paralela los cambios que se desean (git checkout -b **rama**)
Se hace un commit a la rama (git commit -am ***'Comentario'**)
Se suben al remoto los cambios (git push origin **rama**)
En GitHub se hace el pull request comparando la rama master con la rama del fix.
Uno, o varios colaboradores revisan que el código sea correcto y dan feedback (en el chat del pull request)
El colaborador hace los cambios que desea en la rama y lo vuelve a subir al remoto (automáticamente jala la historia de los cambios que se hagan en la rama, en remoto)
Se aceptan los cambios en GitHub
Se hace merge a master desde GitHub
Importante: Cuando se modifica una rama, también se modifica el pull request.

powerlevel9k/powerlevel9k
agnoster