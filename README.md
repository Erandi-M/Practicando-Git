# Practicando-Git
Repo para poner en práctica comandos de git y resolver incidencias con merge
a)- intuyendo que, tenemos las bases de git ya establecidas individualmente, en estas primera "sesion" tomemos en cuenta los siguientes comandos que al final cito pretendiendo reforzar acciones que desempeñaremos cuando nos toque liderar un equipo de trabajo...


A3.4 Apéndice C: Comandos de Git - Ramificación y fusión
Ramificación y fusión
En Git, solo existen unos pocos comandos que implementan la mayor parte de la funcionalidad de ramificación y fusión.
rama de git
Este git branchcomando es, en realidad, una herramienta de gestión de ramas. Permite listar las ramas existentes, crear nuevas, eliminarlas y renombrarlas.
La mayor parte de Git Branching se centra en el branchcomando y se utiliza a lo largo de todo el capítulo. Lo presentamos por primera vez en Crear una nueva rama y analizamos la mayoría de sus otras características (listado y eliminación) en Gestión de ramas .
En la sección de Seguimiento de ramas, utilizamos la **git branch -uopción**[^1] para configurar una rama de seguimiento.
Finalmente, en la sección de Referencias de Git , repasaremos algunas de las funciones que realiza en segundo plano .
**git checkout**[^2]
Este git checkoutcomando se utiliza para cambiar de rama y extraer el contenido al directorio de trabajo.
Nos encontramos por primera vez con el comando en Switching Branches junto con el git branchcomando.
Vemos cómo usarlo para comenzar a rastrear ramas con la **--trackbandera**[^3] en Seguimiento de ramas .
Lo utilizamos para reintroducir conflictos de archivos en **--conflict=diff3**[^4] Checking Out Conflicts .
Analizamos con mayor detalle su relación git reseten Reset Demystified .
Finalmente, entramos en algunos detalles de implementación en The HEAD .
**git merge**[^4]
Esta git mergeherramienta se utiliza para fusionar una o más ramas con la rama que has seleccionado. A continuación, la rama actual se actualizará con el resultado de la fusión.
Este git mergecomando se introdujo por primera vez en el libro "Basic Branching" . Aunque se utiliza en varias partes del libro, existen muy pocas variaciones del mergecomando; generalmente solo se usa git merge <branch> con el nombre de la rama que se desea fusionar.
Explicamos cómo hacer una fusión comprimida (donde Git fusiona el trabajo pero simula que es solo una nueva confirmación sin registrar el historial de la rama en la que se está fusionando) al final de Forked Public Project .
Repasamos en detalle el proceso y el comando de fusión, incluyendo el **-Xignore-space-changecomando** y la **--abortbandera** para abortar una fusión problemática en Fusión avanzada .
Aprendimos cómo verificar las firmas antes de fusionar si tu proyecto utiliza la firma GPG en Firma de confirmaciones .
Finalmente, aprendimos sobre la fusión de subárboles en Fusión de subárboles .
**git mergetool**
Este git mergetoolcomando simplemente inicia una herramienta externa de ayuda para fusiones en caso de que tengas problemas con una fusión en Git.
Lo mencionamos brevemente en Conflictos básicos de fusión y explicamos en detalle cómo implementar su propia herramienta de fusión externa en Herramientas externas de fusión y diferencia .
**git log**
Este git logcomando se utiliza para mostrar el historial registrado de un proyecto, desde la instantánea de confirmación más reciente hacia atrás. Por defecto, solo muestra el historial de la rama actual, pero se le pueden especificar diferentes ramas o cabeceras, o incluso varias, para explorar. También se usa con frecuencia para mostrar las diferencias entre dos o más ramas a nivel de confirmación.
Este comando se utiliza en casi todos los capítulos del libro para ilustrar la historia de un proyecto.
Presentamos el comando y lo analizamos en detalle en Visualización del historial de confirmaciones . Allí examinamos la opción **-py** para tener una idea de lo que se introdujo en cada confirmación y las opciones y para ver el historial de forma más concisa, junto con algunas opciones sencillas de filtrado por fecha y autor.**--stat--pretty--oneline**
Al crear una nueva rama, la utilizamos con la **--decorateopción de visualizar fácilmente dónde se encuentran los punteros de rama y también utilizamos la --graphopción de ver cómo se ven los historiales divergentes.
En "Equipos pequeños privados" y "Rangos de confirmaciones" explicamos la branchA..branchBsintaxis para usar el git logcomando y ver qué confirmaciones son exclusivas de una rama en relación con otra. En " Rangos de confirmaciones" profundizamos bastante en este tema.
En Registro de fusión y Punto triple, explicamos cómo usar el **branchA…​branchB**formato y la **--left-rightsintaxis** para ver qué se encuentra en una rama o en la otra, pero no en ambas. En Registro de fusión, también analizamos cómo usar la **--mergeopción** para depurar conflictos de fusión y cómo usarla **--cc**para ver los conflictos de confirmación de fusión en el historial.
En RefLog Shortnames utilizamos la **-gopción** de ver el registro de referencias de Git a través de esta herramienta en lugar de recorrer las ramas.
En la sección de Búsqueda, analizamos el uso de las opciones **-S**y **-L**para realizar búsquedas bastante sofisticadas de algo que sucedió históricamente en el código, como por ejemplo, ver el historial de una función.
En Firma de confirmaciones vemos cómo usar **--show-signature**para agregar una cadena de validación a cada confirmación en la **git logsalida** en función de si fue firmada válidamente o no.
**git stash**
Este git stashcomando se utiliza para almacenar temporalmente el trabajo no confirmado con el fin de limpiar el directorio de trabajo sin tener que confirmar el trabajo inacabado en una rama.
Esto se trata prácticamente en su totalidad en Almacenamiento y Limpieza .
*etiqueta git*
Este git tagcomando se utiliza para añadir un marcador permanente a un punto específico del historial del código. Generalmente se usa para cosas como versiones.
Este comando se presenta y se explica en detalle en la sección de Etiquetado , y lo utilizamos en la práctica en la sección de Etiquetado de tus versiones .
También explicamos cómo crear una etiqueta firmada con GPG usando la **-sbandera** y cómo verificar una con la **-vbandera** en Firmar su trabajo .



**referencias**
       Nombre                        Tipo                          Sirve para
[^1]: **--git stach -u opcion**      Comando+opcion
[^2]
