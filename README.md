# ¿QUÉ ES GIT?
- Git es un sistema de control de versiones (VCS, por sus siglas en inglés), diseñado para llevar un registro de cambios en los archivos de un proyecto en el que trabajan una o más personas.

- Fue desarrollado por Linus Torvalds, el creador de Linux, en 2005, con el objetivo de ayudar a la comunidad open source a colaborar en proyectos de software, haciendo un manejo y seguimiento de los cambios propuestos por cada participante.

# ¿CÓMO FUNCIONA? / _commits_ y BRANCHES
- Un repositorio Git es un directorio en tu disco duro, en donde los cambios a los archivos son rastreados, de manera que se puede regresar a cualquier versión del pasado.

- Git mantiene el registro de los cambios importantes que ocurren en el repositorio. El usuario trabaja sobre copias de los archivos del proyecto (más sobre esto en la sección "Área de trabajo", más adelante), y cuando está convencido de sus avances hace un _commit_, que actualiza el repositorio para incluirlos. Los _commits_ enviados por el usuario, se van encadenando, uno tras otro, para guardar un histórico completo. Gráficamente, cada _commit_ es un nodo, ligado a un _commit_ anterior y a uno posterior.
![](imagenes/master_branch.png)

- En cualquier momento es posible regresar a cualquier _commit_ y seguir trabajando desde ese punto.

# RAMAS (BRANCHES) y MERGES
- Si un usuario quiere trabajar en una línea paralela, dejando la versión principal de su proyecto intacta, puede generar una nueva rama, a partir de cualquier _commit_ en la historia.
![](imagenes/branches.png)

- El usuario que puede elegir a qué rama quiere enviar sus cambios (en qué rama hace sus _commits_).
- La nueva rama puede ser fusionada (_merge_) con la rama _master_ más adelante; sólo será necesario resolver los posibles conflictos, si es que la rama principal también fue modificada. Como se observa en la figura, mientras el usuario trabajó en la rama "Some Feature" haciendo dos _commits_, también hizo un _commit_ en la rama _master_, de manera que al fusionar (_merge_) es posible que tenga que resolver conflictos entre archivos.

# ÁREA DE TRABAJO
- Los nodos (_commits_) en las gráficas anteriores, representan versiones "estables" del proyecto. Es decir, no es deseable que cambios que hace un autor mientras desarrolla sus ideas se vean reflejados de inmediato en las versiones rastreadas por Git.

- Para esto, un repositorio Git, además de rastrear versiones pasadas, tiene un _área de trabajo_ (_workspace_). Los cambios que haga el usuario a los archivos en el _workspace_ no se verán reflejados en ninguna de las ramas rastreadas por Git sino hasta que el autor haga un _commit_, que integrará los cambios hechos en los archivos del _workspace_ a la rama que el usuario elija. El _commit_ actualiza la rama, agregando un nuevo nodo al final.

# ¿CÓMO COLABORAR CON GIT?
- Todo lo que hemos mencionado hasta ahora sucede localmente en la computadora de un usuario. Pero los mismos principios se utilizan para colaborar con un equipo de personas, cada una de las cuales tendrá una copia local del repositorio en su disco duro.
- Flujo de trabajo para colaborar con Git:
 1. Se define un repositorio de origen (_origin_) que puede ser guardado en un servidor propio, o en sitios como GitHub o GitLab.
 2. Los participantes clonan (_clone_) el repositorio _origin_ en sus computadoras, generando una copia local, que pueden modificar sin temor de que sus cambios entren en conflicto con los de otros participantes.
 3. Un colaborador modifica los archivos en su área de trabajo local.
 4. El colaborador hace un _commit_ con estos cambios, actualizando alguna de las ramas de su repositorio local.
 5. El colaborador envía un _pull request_ (ya hablaremos de esto) al repositorio origen, para que los administradores revisen y, en su caso, acepten los cambios y sean integrados (_merge_).
 6. Los demás colaboradores descargan los cambios propuestos (_fetch_), y los integran (_merge_) a sus ramas locales.

# GUÍA PASO A PASO PARA COLABORAR CON GIT Y GITHUB

- Ve a https://github.com y crea una cuenta.

- Descarga e instala el cliente git GitHub Desktop:
   https://desktop.github.com

- Elige la opción "Sign into Github.com" e los datos de tu cuenta de GitHub
![](imagenes/GitHub_desktop_login.png)

- Elige la opción "Clone a Repository":
https://desktop.github.com)
![](imagenes/GitHub_desktop_clone_1.png)

- En el primer campo, ingresa la dirección de este repositorio (https://github.com/dacocp/AprendeGit) y en el segundo, la ruta donde desees guardar la copia local (se sugiere dejarlo como está por default):
![](imagenes/GitHub_desktop_clone_2.png)

- En la pantalla siguiente, verás la lista de cambios en tu área de trabajo, que no han sido sincronizados (_commit_) con tu _master branch_. Como el repositorio está recién clonado, debe mostrar: _0 changed files_
![](imagenes/GitHub_desktop_pantalla_inicio.png)
