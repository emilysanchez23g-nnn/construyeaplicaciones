"# marketplace_main" 
Submódulo:
Construye aplicaciones web

Práctica Evaluatoria Parcial 3

Nakashimada Martínez del Cañizo Anna
Prieto Zaragoza Natalia Abigail
Martinez Medina Evan
Durán Covarrubias Liliana
Avila Silva Maximous Alexander
Sanchez Gonzalez Emily

Grupo 5BMPG



Índice:

1. Introducción____________________3
2. Explicación de Comandos__________4
3. Diagrama______________________9
4. Explicación de Archivos__________11
5. Actualización del proyecto _______ 18
6. Ejecución Proyecto______________33
7. Actualización__________________35
8. Conclusión____________________42

   Introducción:

¿Por qué utilizar Django para desarrollar
aplicaciones web?

Django es un framework de alto nivel que permite el
desarrollo seguro y rápido de aplicaciones web. Además
tiene herramientas que facilitan el uso de django de tal
manera que los desarrolladores de aplicaciones con este
programa puedan desarrollar paginas web facilmente y de
manera eficiente, las cuales serán la interfaz de
administración la cual facilita modificar las cosas sin entrar
en el código, tiene una autentificación y ORM incorporada,
velocidad de desarrollo django le da la velocidad y la
potencia de python. Con el programa pillow se crean
scripts para tener una mejor visualización de las imágenes
y además

Explicación de Comandos:

cd Documents : Ese comando se usa para decirle al programa donde
queremos la futura carpeta que vamos a crear.
Cambiar de directorio a Documents.

md dj_projects : El comando md lo utilizamos para crear un nuevo
directorio o carpeta, en este caso nuestra carpeta se llamará
“dj_projects”.

md dj_marketplace : Después de cambiar de directorio, pasamos a
crear una nueva carpeta, usando el mismo comando md pero en esta
ocasión ésta se llamará “dj_marketplace”.

cd dj_marketplace : Cambia de directorio de dj_projects a
dj_marketplace.

python -m venv venv : Va a crear y gestionar entornos virtuales,
permitiendo tener estos entornos Python totalmente separados y aislados.
venv\Scripts\activate : Activará el entorno virtual de Python, además
de que prepara la terminal para instalar paquetes y trabajar en
aislamiento.

pip install django : Lo utilizamos para instalar django en el Command
prompt.

django-admin startproject marketplace_main : Lo usamos para
crear el esqueleto o estructura de un nuevo proyecto Django, que en este
caso es “marketplace_main”.

cd marketplace_main : Cambiamos de directorio a marketplace_main,
el cual es el proyecto que iniciamos con el comando anterior,
“django-admin startproject marketplace_main”.

pip install pillow : Va a instalar pillow en el Command prompt.}

pip list Package Version : Te va a mostrar la lista de versiones que
tienen en ese momento.

pip freeze>requirements.txt : Va a guardar en el entorno virtual
llamado requirements.txt, los paquetes que se instalaron usando pip.

python manage.py startapp store : Sirve para crear una nueva
aplicación dentro del proyecto de Django, en este caso se llama store.

dir : Lo utilizamos para que nos de un listado del contenido de un
directorio, mostrando sus archivos y subdirectorios. Tenemos que buscar
que la app “store” aparezca en el command prompt.

python manage.py makemigrations : Este comando funciona para
crear archivos de migración de base de datos basados en los cambios
realizados en los modelos (models.py)

python manage.py migrate : Ese comando se utiliza para ver si todo en
los comandos va en orden y si está funcionando como deben.

python manage.py createsuperuser : Este comando nos sirve para
poder crear nuestro superusuario. Todo esto para poder acceder al panel
de administración.

python manage.py runserver : Mediante este comando podemos iniciar
el servidor de Django

code . : Esto va a abrir una ventana del programa Visual Studio Code
donde van a salir todos los códigos, y se puede modificar desde ahí.


Diagrama:
La arquitectura MVT es el patrón de diseño que utiliza
django. Django lo utiliza para separar la lógica de la
aplicación, la gestión de datos y la presentación visual.
El propósito principal es mantener el código organizado ,
reutilizable y fácil de mantener.
MTV significa:
Model - maneja los datos y la base de datos
View - contiene la lógica del negocio
Template - define como se muestran esos datos al usuario

1. El usuario hace una solicitud (request) HTTP a django
, el cual busca en urls.py que vista debe manejar.
2. Django ejecuta la view donde procesa la información
en caso de necesitar datos accede a los modelos y
prepara la información para el Template.
3. View usa el modelo el cual se traduce en una tabla
4. View pasa los datos al template
5. Django envía la respuesta al navegador del usuario.

Explicación de los archivos:
Settings.py, urls.py, models.py, views.py

Settings.py: El archivo settings.py es básicamente donde se guarda toda
la información del proyecto en Django, dentro del archivo se guardan
cosas como: la base de datos,las apps que usamos, el idioma, la zona
horaria, etc. Este archivo es muy importante, ya que sin él, Django no

sabría dónde guardar toda la información del proyecto y todo se perdería
o estaría desorganizado.

Es como la configuración que todos los teléfonos tienen, desde ahí
podemos cambiar y configurar cosas del celular. Lo mismo pasa con este
archivo, si nosotros queremos cambiar algo de nuestro proyecto; como
por ejemplo: cambiar el idioma, agregar más aplicaciones, etc.
Tendremos que ir al archivo settings.py, todo se modifica desde ahí.
Así que, gracias a este archivo nosotros podemos decidir cómo se va a
comportar nuestro proyecto y las herramientas que vamos a utilizar.

urls.py: El archivo urls.py sirve para manejar las direcciones o rutas
(como links) dentro de nuestro proyecto de Django. Su función es decirle
al programa qué página debe mostrar cuando el usuario entra a una
dirección específica dentro del sitio web, para que cuando nosotros
queramos ir al inicio, Django mediante este archivo va a saber qué
mostrarnos en la pantalla.
Pues básicamente sirve como una guía o puede ser como un mapa que
ayuda a mostrar las direcciones específicas, nos ayuda a mantener todo
organizado.
Este archivo de urls.py es muy importante, porque sin él, Django pues no
sabría que mostrar en cada dirección, entonces todas las partes o páginas
de nuestro sitio no servirían, quedarían sin acceso. Así que se podría decir
que el urls.py es como el GPS del sitio web, nos ayuda a guiar al proyecto
e indicar hacia donde enviar cada solicitud, gracias a esto los usuarios
podemos navegar por las distintas partes del sitio.
En resumen, urls.py se encarga de conectar todas las direcciones del sitio,
para mostrarnos en la pantalla lo que debe ser, así cada página tiene su
propio camino dentro del proyecto.

models.py: El archivo models.py en un proyecto en Django sirve para
definir cómo se van a guardar los datos en la base de datos. Es como el
diseño o la estructura de la información que usa nuestra aplicación.
En este archivo se crean modelos, que son básicamente clases de python
que muestran tablas en la base de datos.
Por ejemplo, podemos tener un modelo de “Producto” con campos como
nombre, precio y descripción, y Django se encarga de crear
automáticamente la tabla con esos datos.
Lo bueno del archivo de models.py es que no tienes que escribir código
SQL complicado. Django traduce todo por nosotros y nos deja trabajar
con los datos de una forma más sencilla y ordenada. Así podemos crear,
leer, actualizar o borrar registros directamente desde el código.
En pocas palabras, models.py es el archivo donde defines qué datos
existen en tu proyecto y cómo se guardan. Es la parte que se encarga de
todo lo que tiene que ver con la base de datos.

views.py: Es un archivo en un proyecto de Django que contiene las
vistas, que son funciones de Python que reciben solicitudes HTTP y
devuelven respuestas HTTP. Este archivo centraliza la lógica de la
aplicación web, incluyendo la obtención de datos, su procesamiento y la
generación del contenido que se muestra al usuario en el navegador.
Funciones Principales de Views.py.
Contener la lógica de la aplicación: Agrupan toda la lógica necesaria
para generar una respuesta específica a una URL, como mostrar una lista
de productos, el detalle de un artículo o procesar un formulario.

Interactuar con modelos: Pueden acceder y manipular datos de la base
de datos a través de los modelos de Django.

Devolver respuestas: Retornan un objeto HttpResponse que puede ser
texto plano, una página HTML renderizada a partir de una plantilla, una
redirección o un archivo de imagen, entre otros.

Organizar la aplicación: Sirven como el punto central para organizar las
diferentes "vistas" o funcionalidades de una aplicación de Django.

¿Para qué sirve el folder “templates/store”? Básicamente el folder de
templates/store sirve para guardar los archivos html que definen cómo se
va a ver nuestra página web, estos archivos sirven para el diseño y la
estructura de la página, como por ejemplo los archivos: base.html,
home.html, etc.

Actualización del proyecto:

Forms.py (LoginForm, SignupForm, NewItemForm)
LoginForm: Es quien permite a los usuarios ingresar sus credenciales o
datos (nombre del usuario, contraseña)y acceder a ciertos privilegios
dentro del programa.

SignupForm: Es la clase que maneja el registro de los usuarios. Sirve
para recibir los datos(nombre usuario, correo, contraseña,etc), valida la
información y procesa y guarda los datos.

NewItemForm: Es una clase de formulario para crear o registrar nuevos
elementos en la aplicación.

Views.py (login(), logout_user(), detail(), add_item())
login(): Es la vista que se encarga de manejar el proceso de inicio de
sesión de los usuarios, principalmente muestra el formulario, procesa las
credenciales, valida al usuario y la contraseña, crea una sesión y redirige
al usuario.
logout_user(): Es una vista personalizada para cerrar la sesión del
usuario. Se encarga de eliminar la información del usuario, limpia la
sesión actual y no devuelve nada.
detail(): Es la función o la clase que sirve para mostrar los detalles de un
solo objeto de la base de datos identificado por su ID.
add_item(): Es una función definida para manejar la lógica de agregar
un nuevo elemento (ítem) a la base de datos.

Decorador @login_required
Funciona para restringir el acceso a ciertas vistas o funciones de la
aplicación, permitiendo solo a los usuarios que han iniciado sesión
acceder a ellas. Es una forma de añadir funciones sin modificar el código.

Urls.py (Las rutas a cada acción nueva en views)
Sirve para mostrar una página a detalle de un objeto usando su
ID(Usuario).

store/templates (item.html, login.html, signup.html,
navigation.html, form.html)
Item: Sirve para poner las imagenes de marketplace para que se vea el
producto que se va a vender
login.html:sirve para registrarse en el servidor de la tienda de
marketplace.
Login: Sirve para registrarse en la tienda de marketplace como nuevo
usuario.
Signup: Sirve para iniciar sesión en la tienda en dado caso de que tengas
una cuenta en el servidor ya iniciada.
Navigation: Funciona para organizar la página web, para que se pueda
ver bien además que con claridad para todos como los usuarios,
programadores y computadora.
Form: Sirve para poder ingresar iniciando sesión por medio de la
solicitudes definiendo de cuando se usan las plantillas de signup.html y
login.html.

Ejecución del proyecto:


Actualización:



Conclusión:

Durante este trabajo aplicamos los aprendizajes que nos proporcionó el
profesor en clase, también como realizar las prácticas. Usamos programas
como Django, visual studio code, y programas externos. También nos
ayudamos entre equipo y nos ayudamos a completar los códigos o
corregir errores.
Incluso varias veces nos confundimos en algunos pasos, ya que al inicio
estábamos un poco perdidos, pero buscamos tutoriales para poder
avanzar y lograr terminar nuestro proyecto en tiempo y forma. Gracias a
la comunicación de todos nuestros integrantes ayudando en este trabajo,
se nos hizo más sencillo y mucho más eficiente para todos la elaboración
de este proyecto.
Aprendimos para qué sirven algunos comandos que son esenciales para la
creación de una página web, así que gracias a esto, en un futuro se nos
hará mucho más fácil la creación de nuestra propia página web, porque
ahora sabemos cómo se usan y qué hacen dentro de nuestro proyecto.
De esta forma, aprendimos a crear una página web desde cero en Django
mediante códigos en Visual Studio Code y comandos en CMD. Nosotros
anteriormente ya habíamos creado páginas web, pero usábamos más
herramientas para diseñar de forma visual, esta vez creamos todo a base
de códigos.
