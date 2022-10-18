# Sistemas_Operativos1
Esta es la práctica 1 de Sistemas Operativos I.

Se trata de desarrollar un script en BASH que proporcione un funcionamiento similar al mandato du
de UNIX, el cual se denominará midu. A continuación, se describe los requisitos funcionales de este
script

Se trata de desarrollar un script de shell similar al mandato du de UNIX, aunque con una funcionalidad
reducida. El programa se denominará midu y su sintaxis será la siguiente:

                                  midu [opciones] [camino1,camino2,…]

El comando recorre el listado de caminos (si no se indica ninguno se utilizará el directorio de trabajo
actual “.”), para cada uno de los posibles caminos, comprueba si “caminoX” es un directorio o un
fichero regular.


- Para el primero de los casos (directorio) se recorre recursivamente los ficheros regulares y
subdirectorios que penden de cada “caminoX”, evaluando las opciones especificadas hasta
que se conoce el resultado de dicha evaluación (verdadero o falso), en cuyo caso se mueve al
siguiente nodo. Cuando se recorre todo un subdirectorio se imprime su ruta, su tamaño total (en
bloques de 1024bytes=1KB) y un salto de línea. En este caso, no se imprimen las rutas y tamaños
de los ficheros regulares que se vayan recorriendo (se acumula su tamaño relacionado con el
directorio del que pende/cuelga).

- Si la ruta de “caminoX” se corresponde con un fichero regular, simplemente, se imprime su ruta
y su tamaño (en bloques de 1024bytes=1KB), sempre que se cumplan las condiciones de
evaluación de las posibles opciones.

El parámetro opciones podrá incluir cualquier una combinación de las opciones descritas (ninguna,
alguna o todas, antes de los posibles caminos).

Las opciones que se deben desarrollar son las siguientes:

-d niveles
Desciende como máximo niveles (entero no negativo) niveles de directorios por
debajo de los argumentos de la línea de órdenes. “-maxdepth 0” significa que
sólo se mostrarán por pantalla los correspondientes -d niveles.

-S
Para los directorios no se imprime el tamapo de los subdirectorios.

--exclude=PATRON

Si la base del nombre del nodo, bien sea fichero regular o directorio (es decir, el
camino o ruta indicado quitando los directorios/subdirectorios de los niveles
superiores) concuerda con el patrón del shell PATRON, entonces, se excluyen
esos nodos coincidentes del cálculo del tamaño (y, por ende, tampoco se
imprimen en pantalla). Dicho patrón puede incluir los metacaracteres: ‘*’ y ’?’.

A modo de ejemplo, considérese el árbol de directorios situado debajo del directorio $HOME, tal y
como aparece a continuación, donde los subdirectorios con marcados en letra verde.

El programa midu deberá realizar un correcto tratamiento de todos los errores.
NOTA IMPORTANTE: Está prohibido utilizar el comando du del sistema para implementar el script
midu propuesto en este proyecto práctico.

Para realizar el programa se recomienda encarecidamente estudiar con detalle la página de manual
referente al bash, donde se encuentra casi todo lo necesario para realizar la práctica. Para poder
guardar dicha información en un fichero pdf (bash.pdf) se deberán ejecutar los siguientes comandos:

man –t bash > bash.ps
ps2pdf bash.ps

Análogamente deberá hacerlo para la página de manual referente al comando du.
Para las dudas sobre este proyecto práctico, podéis poneros en contacto con el profesor de la
asignatura bien vía Campus Virtual o en el correo Ivan.GDiaz@uclm.es para solicitar tutorías.

BY: RAUL JIMENEZ Y PABLO BLAZQUEZ