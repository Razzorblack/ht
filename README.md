Software obligatorio para ejecutarlo.

Homestead. -> Guía de instalación en la web oficial de Laravel.

node.js -> Es un entorno de ejecución de javascript, no lo vamos a usar pero es necesario tenerlo instalado para usar npm.

npm -> Gestor de paquetes javascript, es el gestor de paquetes principal de node.js

git -> https://git-scm.com/

php 5.4 o superior

composer -> Gestor de paquetes php

ruby -> No lo usamos directamente pero nos hace falta para que gulp pueda compilar sass.

python -> No lo usamos directamente pero hace falta para instalar paquetes npm.

Puede que se me pase alguno por alto, pero principalmente son estos.

Es importante todos esten referenciados en la variable PATH del sistema para poder ejecutarlos desde cmd.
Creo que la mayoría durante la instalación dan la posibilidad de instalarlo como variables del sistema. Si alguno no da la opción hay que hacerlo manualmente.


Para desarrollar yo uso phpStorm y webStorm, con el primero es suficiente. Además te recomiendo tener instalado Sublime Text para abrir algún fichero random rápidamente.

(No es raro que la instalación de todo esto levante más de un dolor de cabeza)

Cliente.

e2e sirve para hacer pruebas tipo test sobre el código desarrollado, por ahora no nos interesa y la podemos omitir por completo.

src contiene todo el código de la interfaz gráfica. 

Es lo que vamos a editar para hacer los cambios de la parte gráfica.

gulp: es un sistema que ayuda a automatizar tareas. Antiguamente, en versiones anteriores de gulp, todos los ficheros dentro de /gulp  estaban incluidos en gulpfile.js. Pero como se hizo muy grande, para tenerlo ordenado está dentro de /gulp.

Qué tipo de tareas hace gulp?
Nosotros desarrollamos sobre /src, donde puedes ver que hay unos cuantos ficheros, pues gulp se encarga de generar 2 o tres ficheros (index.html, app.js, etc) que son equivalentes a todo lo que hay /src, pero mucho menos pesados y más optimizados.

El cliente es lo que descarga en el navegador cuando se abre la página web. El cliente carece de funcionalidades, de por sí, quien piensa es el backend, el server.

Cómo se comunican cliente y server?

Mediante API REST (busca en Google para comprender que es, tampoco te ralles mucho porque no tiene gran misterio). Cuando el cliente detecta un evento, por ejemplo hacer clic sobre el botón de añadir torneo, el controlador del cliente hace una petición http a la ruta asociada a ese botón. Dicha ruta sería algo así como "www.servidor.com/torneos/add" (la ruta es /torneos/add), y está definida en el servidor. Cuando el servidor detecta que se ha llamado a dicha ruta, gestíona la petición mediante un controlador del servidor.
