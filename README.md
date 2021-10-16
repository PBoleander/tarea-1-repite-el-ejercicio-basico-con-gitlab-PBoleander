[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-f059dc9a6f8d3a56e377f745f24479a46679e63a5d9fe6f495e02850cd0d8118.svg)](https://classroom.github.com/online_ide?assignment_repo_id=5970122&assignment_repo_type=AssignmentRepo)
# tarea1-peps

## Pascual Barrer Ferrer

---

## Comandos básicos de Git

Primero creamos una carpeta para contener el repositorio en local e iniciamos en él git:

![](Capturas/1a_parte_gitlab.png)

A continuación hacemos un `git status` (vemos que no hay nada), creamos un primer archivo y escribimos algo en él, lo añadimos a git y hacemos `commit`:

![](Capturas/2a_parte_gitlab.png)

Creamos el repositorio en GitLab para tener un remoto al que subir/bajar los archivos. Le damos un nombre cualquiera y clicamos en el botón azul de crear proyecto:

![](Capturas/crear_repo_gitlab.png)

En la siguiente pantalla copiamos la línea `git remote add origin...`:

![](Capturas/2a_parte_crear_repo_gitlab.png)

y la ejecutamos en la terminal:

![](Capturas/add_origin_gitlab.png)

Ahora nuestro git local ya tiene asociado nuestro nuevo repositorio GitLab como remoto. Todos los `push` y `pull` apuntarán a ese repositorio.

Para comprobar que todo funciona podemos hacer un `push` y guardaremos los nuevos cambios en el remoto:

![](Capturas/push_gitlab.png)

A continuación añadimos una segunda línea al archivo pero no añadimos el cambio a git (no lo registramos). Si ejecutamos un `reset` al HEAD seguido de un `checkout` devolveremos el archivo al estado en el que se encuentra en git. Dicho de otra manera, todos los cambios que no hayamos registrado en git se desharán como podemos ver si volvemos a mirar el archivo (sólo está la línea original):

![](Capturas/reset_checkout_gitlab.png)

Pero esto no se limita a recuperar la última versión guardada en git sino que se puede recuperar cualquier versión que esté registrada en git. Para comprobarlo añadiremos más cambios a nuestro archivo:

![](Capturas/checkout_primer_commit_gitlab.png)

Rescatando el commit inicial a través de su hash (e39f7e2) podemos recuperar una versión en concreto. Aunque tuviéramos 100 versiones de un archivo podríamos recuperar la versión que quisiéramos.