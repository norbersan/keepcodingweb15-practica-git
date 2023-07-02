- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
	git reset --hard HEAD~1
	lo que necesitaba son 2 cosas:
			1.- mover el puntero head al commit anterior
			2.- actualizar el working copy con los cambios de dicho commit
			git reset HEAD~1 habria heco lo primero pero no lo segundo
	con el flag --head realizo las dos aciones en un solo comando

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
git reflog pare obtener el hash del commit descartado
git merge <hash> para hacer un commit fast forward y mover de nuevo el puntero al commit que previamente habia descartado

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No se creo ningun conflicto puesto que en la rama main el archivo git-nuestro .md no se habia modificado en ninguna linea

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
si, habia conflictos porque en ambas ramas se habian modificado las mismas linesa del archibo git-nuestro.md

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
no hubo conflictos, era un merge fast forward


- ¿Qué comando o comandos utilizaste en el paso 25?
git log --graph

* commit 5ce01534950fecd494798511d1bb37b0ff6d838a (HEAD -> main)
| Author: Norberto Sánchez <norber_san@hotmail.com>
| Date:   Sun Jul 2 14:54:08 2023 +0200
|
|     title added to git-nuestro.md
|
*   commit bf5a33c307970f87e27b0995388d630b8b504b45 (title, styled)
|\  Merge: f3e09c0 e8e8e63
| | Author: Norberto Sánchez <norber_san@hotmail.com>
| | Date:   Sun Jul 2 14:44:06 2023 +0200
| |
| |     merged from htmlify. conflicts solved
| |
| * commit e8e8e638d3806f39e5e314f973ac0fccfa299e52 (htmlify)
| | Author: Norberto Sánchez <norber_san@hotmail.com>
| | Date:   Sun Jul 2 14:41:16 2023 +0200
| |
| |     git-nuestro htmlified
| |
* | commit f3e09c0e5e776672bd3cb363fd8d43e9fd537e45
|/  Author: Norberto Sánchez <norber_san@hotmail.com>
|   Date:   Sun Jul 2 14:08:49 2023 +0200
|
|       modified git-nuestro
|
* commit cd486b298e503bb763c23d6a36cda70285c9b8a1
  Author: Norberto Sánchez <norber_san@hotmail.com>
  Date:   Sun Jul 2 14:00:04 2023 +0200

      initial commit
	  
	  

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
si, podria ser un fast forward porque no hay mas commits main a partir de main a los que se pueda perder acceso

- ¿Qué comando o comandos utilizaste en el paso 27?
git reset HEAD~1

- ¿Qué comando o comandos utilizaste en el paso 28?
git restore git-nuestro.md

- ¿Qué comando o comandos utilizaste en el paso 29?
git branch -D title
- ¿Qué comando o comandos utilizaste en el paso 30?
git merge <hash>
para hacer un fast forward y rehacer los cambios, antes hice un reflog para conocerel hash


- ¿Qué comando o comandos usaste en el paso 32?
- ¿Qué comando o comandos usaste en el punto 33?
en los pasos 32 y 33, en ambos casos busque los hashescorrespondientes con git log sobre la rama main
y despues hice un git checkout usando el hash correspondiente

