## ¿Qué es una rama?

#### Head

![work flow](img/wf.png)

- `head` Es el commit dónde nos encontramos actualmente.

- Una rama es una *linea de tiempo* de nuestro proyecto.
- Se compone de una *secuencia de commits*.
- Se utilizan para desarrollar nueva funcionalidad, corregir errores, realizar pruebas, etc.

![comparacion](img/comparacion.png)

#### Git permite múltiples ramas

![ramas](img/ramatest.png)

![ramas](img/ramabug.png)

## Operaciones básicas:

### Listar las ramas locales:

`git branch`

![](img/gitbranch.png)

- El simbolo `*` indica la rama a la que apunta el `HEAD`

### Crear rama local

`git branch <NAME>`

![creando ramas](img/ramas.png)

- Creamos la rama, pero `HEAD` sigue apuntando a `master`.

### Cambiar de rama:

`git checkout <NAME>`

![checkout](img/checkout.png)

- Si usamos `git checkout -b <NAME>`, además de crear la rama nos posicionamos sobre ella.

### Eliminar la rama:

`git branch -d <NAME>`

![borrar rama](img/deleterama.png)

- Una rama puede ser borrada si todos sus commits han sido "absorbidos".
- Para forzar un borrado usamos la flag `-D`.

## [Ejemplo practico](https://github.com/exa-tio/ejemplo-login)

En el ejemplo, se nos pide realizar cambios a una pantalla de login. Estas son las tareas que nos asignan:

1. Realizar cambios de color en el título y en el background.
2. Cambiar texto boton a mayusculas.

![ejemplo login](img/login.png)

Realizamos los cambios en la rama "`estilos`".

![cambios en la rama estilos](img/cambiosenrama.png)

- ¿Qué sucede si cambiamos a la rama master con el comando git checkout?
  - que dice el git log?

![rama master](img/enramamaster.png)
![diferencias](img/diferencias.png)

#### Fucionar dos ramas
![merge](img/merge.png)

### Fast forward:
- La fusion se realiza de manera automatica
- No hay conflicto entre una rama y otra (los commits fueron de manera secuencial)
- Se pudo "unir" todo el contenido sin problemas.


¿Que pasaria si otro/s programador/es hubieran hecho otros commits en la rama principal (en este caso `master`).

![conflicto](img/ramasdivergentes.png)

#### Manual merge

El programador es quien debe resolver el conflicto

![conflicto](img/conflicto.png)

Para salir de este estado de "*Merging*" es necesario resolver el conflicto, agregar los archivos al staging area y luego realizar la confirmación. 

> pensemos que son dos cambios apuntando a la misma linea de código en este ejemplo.

#### Confirmación del merge

- Para salir del estado de "merging" es necesario resolver el conflicto, agregar los archivos a la staging area y luego realizar la confrimacion.

![solucion del conflicto](img/solucionconflicto.png)

### Ramas remotas:

 - `git push -u origin <remote> <remote_branch>`
 - `git push -u origin <remote> <local_branch>:<remote_branch>`

Ejemplo:

`git push -u origin estilos`

![switch branch](img/switchbranch.png)

#### ¿Por qué hacer *branches* en el proyecto?

- Para desarrollar software en paralelo e independientemente entre los programadores.
- Para mantener varias versiones del proyecto.
- Para no afectar al código principal.
- Para disminuir errores.

## Resumen:

- `git branch`: lista las ramas locales.
- `git branch <rama>`: crea una nueva rama.
- `git checkout <rama>`: cambia el puntero de HEAD a <rama>.
- `git checkout -b <rama>`: crea la rama y hace que HEAD apunte a ella.
- `git branch -d <rama>`: elimina la rama.
- `git merge <rama>`: fusiona el contenido de la <rama> en la rama dónde estamos parados.
## Bibliografia

[Git book 3.3](https://www.atlassian.com/git/tutorials/using-branches)