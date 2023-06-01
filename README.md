- # ¡Práctica de GitHub!

  ¡Hola a todos! Este es un repositorio ficticio divertido para practicar y perfeccionar sus habilidades de GitHub. Vamos a usar MUCHO GitHub, por lo que es importante que seas bueno en todo esto.

  ## Configurar

  - Crea una cuenta en [Github](https://github.com/)
  - [Descarga](https://translate.google.com/website?sl=auto&tl=es&hl=es&client=webapp&u=https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) `git` en tu computadora.

  - Los usuarios de Windows deben instalar [git bash](https://translate.google.com/website?sl=auto&tl=es&hl=es&client=webapp&u=https://gitforwindows.org/) . Siga estas [instrucciones de instalación](https://github-com.translate.goog/rsokl/CogWorks_2017_Info/blob/master/WindowsGitInstructions.md?_x_tr_sl=auto&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=wapp)

  ## Templates

  Lo PRIMERO que debe hacer es usar el botón de “templates” de este repositorio, para crear una copia exacta en tu cuenta de Git.

  ## Clonación

  Lo SEGUNDO que debe hacer es clonar este repositorio en su escritorio.

  - Notas: ¿Qué ES un repositorio? De los tutoriales oficiales de GitHub, un repositorio "abarca la colección completa de archivos y carpetas asociados con un proyecto, junto con el historial de revisión de cada archivo".

  ¿Qué es la clonación? Más o menos lo que parece. Todo el contenido interesante de este repo se encuentra actualmente en GitHub (en lo que se llama un **repositorio remoto** ), y lo queremos en nuestra computadora (en un **repositorio local** ). Entonces, ¡necesitamos *clonar* una copia en nuestra computadora! Esto también significa que para clonar un repositorio, debe estar conectado a Internet.

  En su terminal, querrá escribir:

  ```sh
  git clone https://github.com/(user_name)/git-for-practice-with-branch.git
  ```

  Básicamente, lo que hace es llegar a GitHub y copiar todo su contenido en un *repositorio local* en su computadora.

  ¡Felicitaciones! Ahora, tienes un repositorio en tu computadora.

  ## Agregar archivos

  Agregar archivos a un repositorio local es exactamente de la misma manera que agregaría archivos a una carpeta, sin embargo, agregarlo al repositorio remoto en GitHub requiere algunos pasos. Por el bien de la práctica, haga un archivo .txt usando su nombre (si su nombre es John Smith, algo como john_smith.txt funcionará). Para hacerlo más divertido, ¡escribe una broma! Nada a lo que te apegues, porque la gente probablemente se meterá con estos archivos mientras prueba el repositorio ficticio.

  ¡Gran trabajo! Ahora, su repositorio local tiene un archivo .txt con una broma. Ahora, también queremos *cambiar* el repositorio remoto para reflejar las actualizaciones que hicimos. Antes de agregar archivos, primero debe recordar qué archivos ha agregado/cambiado en primer lugar. Puedes hacer esto por:

  ```sh
  git status
  ```

  Este comando mostrará una lista de todos los archivos que cambió en un código de colores, pero como solo agregó un archivo, solo aparece un archivo. Ahora que se acordó de los archivos que deseaba agregar, puede realizar los cambios de la siguiente manera:

  ```sh
  git add (your full name here).txt
  ```

  Cuando agrega archivos, los **prepara** para la confirmación y comienza a **rastrearlos** . También puede organizar archivos independientemente de la conexión a Internet, ya que no está cargando ni descargando nada. El seguimiento de archivos en git es muy conveniente: una vez que se rastrean, puede ver ediciones y versiones anteriores.

  Ahora, una vez que los agregamos y preparamos para la confirmación, ¡realmente necesitamos confirmar!

  ## Commit

  El tutorial de git describe la confirmación de los cambios como "tomar una instantánea de los cambios para incluirlos en el historial del proyecto". Me gusta pensar en las confirmaciones como **estados guardados** en un videojuego. Por ejemplo, tiendes a guardar tu juego después de cada hito: obtener un elemento genial, vencer a un minijefe, después de una escena LARGA, etc. De esa manera, si te equivocas o tu juego se apaga, tienes un archivo guardado para dirigir de regreso. ¡Los compromisos son así! Después de terminar una función o crear una nueva clase y confirmar, si en algún momento se equivoca, puede volver a sus confirmaciones anteriores.

  Entonces, ¿cómo nos comprometemos? Cualquier cambio que haya *preparado* (agregado) se *confirmará* (se convertirá en parte del historial del proyecto) una vez que escriba:

  ```sh
  git commit -m "my first commit!"
  ```

  El `-m`es una parte muy importante del comando. Designa que, la cosa entre comillas, es un *mensaje de compromiso* . ¡ Con CADA confirmación **necesitas** un mensaje de confirmación! (Si no hace -m, lo llevará a una pantalla extraña para escribir su propio mensaje de confirmación. -m es más fácil). Los mensajes de confirmación son solo una descripción útil de lo que cambió y por qué el cambio era necesario. , pero en realidad pueden ser lo que quieras.

  Al igual que los archivos provisionales, la confirmación no requiere acceso a Internet; sus cambios no se cargan realmente hasta que presiona, sobre lo cual aprenderá en la siguiente sección.

  Otra nota importante es que, si NO agrega un archivo y confirma, el archivo no se confirma incluso si se edita y guarda. ¡Más sobre esto más adelante!

  ## Push

  Luego, una vez que haya agregado su archivo y lo haya confirmado, escriba:

  ```
  git push
  ```

  Este comando final actualiza el repositorio remoto (origen) con cualquier confirmación realizada localmente en una rama (maestro). Las cosas que NO están confirmadas NO se actualizarán en el repositorio remoto.

  ¡Dulce! ¡Has *enviado* tus cambios al repositorio remoto y ahora tiene tu divertido archivo .txt!

  Como nota, dado que su repositorio remoto está almacenado en GitHub, necesitará una conexión a Internet para hacerlo.

  ## Pull

  Digamos que muchas más personas TAMBIÉN escribieron chistes y los enviaron al repositorio remoto. ¡Desafortunadamente, su propio repositorio local no tiene esos cambios! Podemos actualizar nuestro repositorio local con ESTO:

  ```sh
  git pull
  ```

  Esto es excelente si está trabajando en equipo y uno de sus compañeros ha realizado cambios que desea compartir con el grupo.

  Al igual que empujar, necesitará Internet para extraer de GitHub.

  ## Merge

  No solo puede agregar nuevos archivos, también puede editar los existentes y actualizarlos en el repositorio remoto exactamente de la misma manera que agregaría los nuevos. Git FUSIONARÁ tu repositorio local con el remoto, actualizándolo.

  Git es incluso lo suficientemente inteligente como para fusionar líneas en el *mismo archivo* . Digamos que Ryan y yo estamos trabajando en dos partes separadas del código en `file1.py`. Escribo una función llamada `hello_world()`y Ryan escribe una función llamada `random_function()`. Primero, no tengo la función de Ryan en mi repositorio local y él no tiene la mía. Pero, ambos decidimos confirmar y enviar al repositorio remoto. Git en realidad *fusionará* nuestras dos versiones de `file1.py`para hacer una con *ambos `hello_world()`y `random_function()`.* Sin embargo, algo a tener en cuenta es que si varias personas editan las mismas líneas/secciones a la vez e intentan impulsar sus confirmaciones, es posible que obtenga un error llamado conflicto de **combinación** . ¡Más sobre eso más tarde!

  ## Branchs

  Supongamos que está trabajando en un *proyecto un poco ambicioso* que no está seguro de si funcionará o no y, aunque desea confirmar los cambios, no desea actualizar el repositorio remoto y perder el trabajo anterior. Otra característica interesante de GitHub es crear diferentes **ramas** .

  ### Creando una nueva rama

  Primero, comencemos con la creación de nuestra rama con:

  ```
  git checkout -b (branch name)
  ```

  Para ver todas sus sucursales, `git branch -v`las listará todas. Deberías ver una `master`sucursal y tu propia sucursal.

  ### Cambio de ramas

  Para cambiar entre ramas, usamos el `checkout`comando.

  ```
  git checkout (branch name)
  ```

  ¡Una nota importante sobre el trabajo en las ramas! Cualquier cambio que realice en una rama NO afectará a la otra rama. Entonces, si agrega un montón de archivos a una rama, su rama maestra no tendrá idea de que esos archivos existen. Del mismo modo, puede eliminar, cambiar el nombre, editar cualquier cosa que desee en una rama y hacer que sus otras ramas permanezcan exactamente igual.

  Para volver a verificar en qué sucursal se encuentra, simplemente escriba:

  ```
  git branch
  ```

  ### Push a esa nueva rama

  ¡Comprometerse y agregar a diferentes ramas es exactamente lo mismo! Sin embargo, empujar requiere un poco de esfuerzo. Si intenta simplemente presionar, obtendrá un error. En su lugar, querrás escribir:

  ```
  git push origin (branch name)
  ```

  El origen designa a qué control remoto estamos empujando y la rama indica desde qué rama estamos empujando.

  ### Merge a la Rama Maestra

  ¡Ahora ha editado su código en su rama separada y fue exitoso! Es hora de volver a fusionarse con la rama principal. Si está trabajando en su **propio código** , puede volver a fusionarse con la rama maestra sin problemas. Sin embargo, si está trabajando en **el código con otros,** querrá hacer una solicitud de extracción en su lugar.

  #### Fusión a la Rama Maestra

  Primero, volvemos a la rama maestra:

  ```
  git checkout master 
  ```

  A continuación, los fusionamos con este simple comando:

  ```
  git merge (branch name) 
  ```

  Si te sientes tan inclinado a eliminar tu rama anterior, usa:

  ```
  git branch -d (branch name) 
  ```

  Ahora, las sucursales se fusionan en SU computadora. ¡Es hora de actualizar el repositorio remoto para reflejar eso! Al igual que estamos empujando desde una rama, agregue y confirme y finalmente presione así:

  ```
  git push
  ```

  ¡Felicitaciones, has fusionado las ramas con éxito!

  ## Volver a una confirmación anterior

  ¿Accidentalmente cometiste algo que arruinó un montón de cosas? ¿Te gustaría poder volver atrás en el tiempo cuando tu código (más o menos) funcionaba? Afortunadamente, tenemos la capacidad de viajar en el tiempo (metafóricamente) gracias a Github. Entonces, primero necesitamos ver todos nuestros compromisos anteriores para decidir a cuál volver. Escribir a máquina:

  ```
  git log 
  ```

  Verá un montón de confirmaciones, mensajes de confirmación y **hashes de confirmación** (las cosas que parecen `12345678901234567890123456789012345678ab`). ¡Estos son importantes! Encuentre el hash de confirmación de la confirmación a la que desea volver y luego escriba:

  ```
  git checkout (commit hash) .
  ```

  El . es importante, ya que establece su rama a la actual. ¡Finalmente, confirme sus cambios y su repositorio debería reiniciarse!

  **Nota importante:** volver a una confirmación anterior solo "rebobinará" los ARCHIVOS SEGUIDOS (los eliminados, los renombrados, ¡siempre que estén rastreados!). Los archivos que NO se rastrean no se restablecerán.

  ## Conflictos comunes y cosas divertidas

  ### Fusionar conflictos!

  Digamos que Ryan y yo estamos editando un archivo. Ambos extraemos los cambios del repositorio y decidimos trabajar en el mismo archivo. Sin embargo, decido que quiero actualizar la variable `x`para que sea igual a 5 mientras que Ryan actualiza `x`para que sea igual a 7. Ambos cambiamos la MISMA línea en el código y luego decidimos empujar/tirar de nuestros cambios.

  ```
  <<<<<<< HEAD
  x = 5
  =======
  x = 7
  >>>>>>> my_branch
  print (x)
  ```

  ¡Ahora tenemos un conflicto de fusión! ¿Que significa exactamente? Bueno, git suele ser bastante inteligente en cuanto a poder fusionar cambios. Si Ryan y yo editamos dos variables/funciones/fragmentos de código separados, incluso si están en el mismo archivo, git generalmente puede fusionarlos. Sin embargo, si ambos hacemos cambios conflictivos (editando la MISMA línea en dos cosas diferentes, editando líneas cercanas, etc.) se lanza git. Git en realidad EDITA mi archivo para mostrarme dónde me equivoqué.

  Afortunadamente, esta es una solución fácil. Elimine el `<<<<<<< HEAD`y el `=======`y el `>>>>>>> my_branch`, y luego elija qué edición le gustaría usar. Vuelve a empujar, ¡y deberías ser bueno! ¡Algunos editores de código como Visual Studio Code realmente resaltarán los conflictos de combinación y le darán un cuadro de diálogo para que pueda elegir rápidamente la versión que le gustaría!

  Ahora que sabemos qué son los conflictos de combinación, intentemos crear uno. Podemos hacer esto creando dos ramas que entren en conflicto y luego tratando de fusionarlas.

  Primero, cree una nueva rama

  ```
  git branch (insert name of branch here)
  ```

  Edite su archivo de texto de broma de antes, agregue los cambios y confírmelo. Ahora, vaya a la rama que creó ejecutando:

  ```
  git checkout (name of the branch you just created)
  ```

  Como antes, cambie el archivo **en la(s) misma(s) línea(s) que acaba de cambiar** , agregue los cambios y confírmelo. Luego, realiza el pago en la rama maestra y cuando ejecutes:

  ```
  git merge (name of the branch you just created)
  ```

  deberías estar recibiendo un error, diciéndote:

  ```
  CONFLICT (content): Merge conflict in (filename here)
  Automatic merge failed; fix conflicts and then commit the result.
  ```

  Ahora, si cierra y vuelve a abrir el archivo de texto que estaba modificando, debería ver un conflicto de fusión como el que se muestra arriba. Elija la versión que le gustaría conservar, póngala en escena y confírmela. ¡Su conflicto de combinación ahora está resuelto!

  ### ¿Descomprometer/Desagregar?

  Uh oh, NO quise enviar ese archivo. Afortunadamente, si desea anular la confirmación, simplemente cambie a una confirmación anterior (detallada en la sección anterior).

  **¡Desagregar** es otra cosa que puedes hacer! Hay algunas maneras de hacer esto que dependen de la situación. Por lo general, si escribe, `git status`le dirá todos los archivos preparados para la confirmación y le dirá qué hacer si desea quitar la preparación de un archivo para la confirmación. Lo más probable es que sea uno de estos comandos:

  - `git rm --cached (file)`
  - `git reset HEAD (file)`
  - `git checkout --(file)`

  ### Eliminar y mover archivos a través de Git

  Si quiere asegurarse de que git esté rastreando todos sus cambios, es una buena práctica eliminar y mover archivos a través de git. `git rm (filename)`eliminará los archivos y `git mv (file_from) (file_to)`los moverá.

  ### .gitignore

  Git define los archivos en tres tipos: con seguimiento, sin seguimiento e ignorados. **Los archivos ignorados** son archivos que git ignora explícitamente. Para designar un archivo como ignorado, debe acceder al archivo .gitignore a mano y agregar una ruta a ese archivo. Hay patrones específicos sobre cómo hacer esto, por lo que recomiendo leer [este](https://translate.google.com/website?sl=auto&tl=es&hl=es&client=webapp&u=https://www.atlassian.com/git/tutorials/saving-changes/gitignore) artículo.

  ### Herramientas Git

  ¡Github es tan popular que la mayoría de los IDE lo han integrado! Por ejemplo, algunos pueden rastrear qué archivos están comprometidos, encontrar conflictos de fusión para usted y mucho más. Si prefiere usar un IDE para la codificación, es una buena idea ver qué características de git tiene.

  ### Comandos útiles de git

  - `git add -u`- agregar todos los archivos SEGUIDOS
  - `git add .`- agregar todos los archivos en el directorio.
  - `upstream`- establece la relación entre las ramas para ahorrar pulsaciones de teclas
  - `git status`- ver qué archivos están preparados, modificados o sin seguimiento
  - `git status -uno`- ver qué archivos se organizan y modifican de todos los archivos rastreados
  - `git diff`- mostrar los cambios entre confirmaciones, confirmación y árbol de trabajo, etc.
  - `git init`- crea un archivo .git y señala que este directorio es un repositorio. **No haga un repositorio dentro de otro repositorio, puede generar confusión.**

  ## ¡Pruebalo por ti mismo!

  Este es el repositorio ficticio, así que siéntase libre de causar estragos en él. Empuja, tira, haz tantas ramas como quieras, ¡lo que creas que te dará más práctica!

  Aquí hay algunos enlaces para ver más cosas divertidas que hacer con Github. Trucos geniales de github de Google, etc. ¡Explora y diviértete!

  - [https://git-scm.com/book/en/v2](https://translate.google.com/website?sl=auto&tl=es&hl=es&client=webapp&u=https://git-scm.com/book/en/v2)
  - [https://help.github.com/articles/github-glossary/](https://translate.google.com/website?sl=auto&tl=es&hl=es&client=webapp&u=https://help.github.com/articles/github-glossary/)
  - [https://guides.github.com/](https://translate.google.com/website?sl=auto&tl=es&hl=es&client=webapp&u=https://guides.github.com/)
