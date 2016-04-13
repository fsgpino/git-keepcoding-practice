# GIT KeepCoding Practice

This is a practice of Git, gitHub &amp; Sourcetree course (Keepcoding)

## Resolution to questions

### ¿Qué comando utilizaste en el paso 11? ¿Por qué?

El comando ejecutado fue `git reset --hard HEAD~1`. Con el comando reset puedo desplazar la rama a otro commit e indicándole *HEAD~1* puedo descender justo al commit anterior del que la cabeza está apuntando actualmente. Puesto que piden que no mantenga working directory uso el parámetro *--hard*.

### ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

El comando ejecutado fue `git reset --hard HEAD@{1}`. En este caso quiero acceder al commit en el que en el paso anterior donde mi HEAD apuntaba a el. Usando la sintaxis de reflog puedo recuperarlo indicándole *HEAD@{1}*.

### El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

No. Pero tampoco hay cambio alguno, se obtiene el mensaje 'Already up-to-date.' puesto que la rama styled ya contiene todos los cambios de master.

### El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

Si, el archivo contiene conflictos puesto que hemos editado las líneas mismas en ambas ramas. Una vez modificado y resuelto el conflicto con un commit el merge quedará concluido.

### El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

 No, se realizará un Fast-forward dejando la rama master en el mismo commit que la rama styled. Esto se debe a que el grafo de commits hasta este punto es lineal. (Es verdad que existe una rama, pero esta se ha unido a la otra antes de donde queremos realizar el merge)

### ¿Qué comando o comandos utilizaste en el paso 25?

El comando ejecutado fue `git log --graph`.

### El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Si, de no haberlo indicado el merge habría sido fast-forward puesto que el grafo es lineal y no tiene ninguna ramificación hasta el commit al que queremos hacer merge.

### ¿Qué comando o comandos utilizaste en el paso 27?

El comando ejecutado fue `git reset HEAD~1`.

### ¿Qué comando o comandos utilizaste en el paso 28?

El comando ejecutado fue `git checkout -- .`.

### ¿Qué comando o comandos utilizaste en el paso 29?

El comando ejecutado fue `git branch -D title`.

### ¿Qué comando o comandos utilizaste en el paso 30?

El comando ejecutado fue `git reset --hard HEAD@{1}`.

### ¿Qué comando o comandos usaste en el paso 32?

En este punto se nos pide que volvamos al commit inicial, dependiendo de si queremos mover HEAD o la rama Master ejecutaremos estos comandos respectivamente `git checkout d7adcec` o `git reset d7adcec`. El valor *d7adcec* son los 7 primeros caracteres del identificador del commit inicial obtenido con el comando `git log`.

### ¿Qué comando o comandos usaste en el punto 33?

En este punto se nos pide que volvamos al commit final, dependiendo de como hayamos actuado en el paso anterior se ejecutaran unas ordenes u otras. Si anteriormente movimos HEAD con el comando `git checkout master` volveremos al commit final, pero si desplazamos la rama Master al commit donde nos encontramos, entonces deberemos recurrir al comando `git reset --hard HEAD@{1}`.
