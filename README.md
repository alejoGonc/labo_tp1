# INSTRUCTIVO DE USO:

## Clonando el repo:
- Abri la consola de comandos de tu compu. Busca 'cmd' dentro de tus aplicaciones de windows
- En la consola parate sobre la carpeta donde quieras guardar el repositorio. En mi caso, lo hice dentro de una carpeta que se llama UBA de esta forma: **cd Desktop/UBA**
- En el repositorio de github, busca el boton verde de 'Code', anda a la solapita de 'https' y copía la URL
- Volviendo a la consola, escribí: **git clone *url-que-copiaste-antes***
- Se te va a crear una carpeta que se llama labo_tp1 con los archivos que estan en el repositorio
- Parandote sobre esta nueva carpeta 'labo_tp1' usar el comando: **venv/Scripts/activate**, luego de ejecutar esto, deberia aparecerte en la consola, antes de la ruta, un (venv), esto significa que el entorno virtual esta activado, sirve para que no tengamos problemas de versiones en el proyecto.
- Si el paso anterior salió bien, falta instalar todas las librerias necesarias con: **pip install -r requirements.txt**

## Subiendo tus cambios:
- Antes de empezar, debemos crear un branch de desarrollo para no pisar el main branch (y borrar todo lo que hicieron los otros), esto se hace con: **git checkout -b *nombre-branch***
    - En mi caso: **git checkout -b desarrollo-alejo**
- Luego de modificar y trabajar los archivos, debemos hacer stage de los cambios: **git add *nombre-archivo.ext***
    - Por ej: **git add main.ipynb**
    - Con **git status** podemos ver todos los archivos en stage que falta hacer commmit
- Ahora hacemos el commit y agregamos un mensaje: **git commit -m 'grafico distribución de pasajeros agregada'**
- Mandamos los cambios al repositorio con: **git push origin *nombre-branch***
    - Por ej: **git push origin desarrollo-alejo**
- Ahora debemos ir al repositorio en github y crear un pull request desde la pestaña de pull request :) 
    - En la pestaña buscamos el boton verde que dice 'New pull request'
    - Dejamos como base el branch main y ponemos en compare nuestro branch de desarrollo. Aca le estamos diciendo a github que nos gustaria meter nuestros cambios de desarollo en la main branch
    - Nos va a mostrar todos los cambios que hiicimos en los distintos archivos
    - Podemos agregar alguna descripcion o comentario respecto a los cambios, y creamos el pull request