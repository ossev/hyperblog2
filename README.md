# hyperblog2
Otro blog de práctica

## Comandos iniciales

_Inicializar un repositorio en local_

```
git init
```
_Revisar el status de los archivos que están pendientes por enviar a staged o por hacerles commit_

```
git status
```

_Guardar los cambios de un archivo en Git_

```
git add
```

_Guardar los cambios en firme de un archivo en la rama_

```
git commit -m "Aqui se pone un nota o nombre al commit"
```

_Borrar un archivo que se haya añadido al repositotio_

```
git rm
```

_Borrar un archivo por completo de la rama_

```
git rm cached
```

_Mostrar la configuración global de git_

```
git config
```

_Mostrar el nombre de usuario guardado en la configuración de git_

```
git config --global user.name
```

_Mostrar el email del usuario guardado en la configuración de git_

```
git config --global user.email
```

_Mostrar el nombre de usuario guardado en la configuración de git_

```
git config --global user.name
```

_Ver la historia de todo el repositorio_

```
git log
```

_Sacar a los archivos del estado staged para devolverlos a su estado anterior_

```
git reset HEAD
```

_Elimina los archivos del área de Staging y del próximo commit pero los mantiene en nuestro disco duro_

```
git rm --cached
```

_Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados)._

```
git rm --force
```


_Mostrar los cambios realizados en el último commit_

```
git show "nombreDelArchivo.extensión"
```

_Mostrar la diferencia de cambios entre los dos últimos commits_

```
git diff
```

_Mostrar la diferencia de cambios entre dos commits en especificos_

```
git diff hashcommit1 hashcommit2
```

_Volver un archivo a un commit específico pero sin borrar los commits aplicado a partir del mismo_

```
git reset #commmit1 --soft
```

_Volver un archivo a un commit específico borrando por completo todos los commits aplicados desde entonces_

```
git reset #commmit1 --hard
```


_Volver un archivo a una versión sin cambiar nada en el staging_

```
git checkout #commmit1
```

_Volver un archivo a la version antes del primer commit_

```
git checkout master archivo.extension
```


_Crear una nueva rama con el nombre de la rama_

```
git branch nombre_rama
```

_Listar las ramas existentes_

```
git branch -l
```

_Elimina una rama_

```
git branch -d nombre_rama
```

_Cambia el nombre de una rama_

```
git branch -m nombre_actual_rama nombre_nuevo_rama
```

_Cambiar a otra rama_

```
git checkout nombre_rama
```

_Crear una nueva rama y se posiciona en ella_

```
git checkout -b nombre_rama
```

_Fusionar dos ramas. Ésto crea automáticamente un nuevo commit cuanod no hay conflictos en la fusión_

```
git merge nombre_de_la_otra_rama
```

Si se produce un conflicto durante el merge, se deben solucionar los conflictos, addicionar y enviar los cambios con un nuevo commit.


_Agregar un origen remoto_

```
git remote add origin "dirección http o ssh"
```

_Traer los cambios del repositorio remoto_

```
git pull origin master
```

_Si al tratar de traer los cambios del remoto, hay datos no relacionados, entonces..._

```
git pull origin master --allow-unrelated-histories
```

_Enviar los cambios del master local al master remoto_

```
git push origin master
```

_Crear las llaves_

```
ssh-keygen -t rsa -b 4096 -C "tu@email.com"
```

_Encender el "servidor" de llaves SSH de tu computadora. En linux y windows_

```
eval $(ssh-agent -s)
```

_Añadir tu llave SSH a este servidor_

```
ssh-add ruta-donde-guardaste-tu-llave-privada
```

_actualizar la URL que guardamos en nuestro repositorio remoto, solo que, en vez de guardar la URL con HTTPS, vamos a usar la URL con SSH_

```
git remote set-url origin url-ssh-del-repositorio-en-github
```