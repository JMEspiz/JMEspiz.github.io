En esta nueva entrada voy a compartirles mi experiencia de como instalar WordPress de forma local usando LAMPP.  

# ¿Que es WordPress?

WordPress, según su sitio [oficial](https://wordpress.org), es un Software Web que puedes usar para construir hermosas sitios web, blog o aplicaciones.

# ¿Que es LAMPP?

XAMPP es software libre que nos brinda un stack completo para el desarrollo de aplicaciones Web. La X significa que es multiplataforma y dependiendo del sistema operativo adopta un nombre, LAMPP en el caso de Linux, MAMPP en el caso de Mac OS X y WAMPP en el caso de Windows. La A hace referencia al servidor Web Apache, la M es por el sistema de gestión de base de datos MariaDB (Fork de MySQL, desde las versiones 5.5.30 y 5.6.14) y los lenguajes de programación PHP y Perl. 

### Consideraciones antes de continuar

Desde mi punto de vista veo mas factible instalar y configurar los servicios por separado, (Apache, MariaDB y PHP), pero esta instalación la hice en una PC con Elementary OS Freya de un compañero que le esta dando una oportunidad a las distribuciones GNU/Linux y hasta el momento esta enamorado de su distribución. Por ende, la instalación va a ser basada a usuarios finales con poca o ninguna experiencia con la terminal. Debido a que yo solo iba a ser un mediador y mi compañero haría la instalación el mismo (Aprender haciendo) fue mas viable elegir el stack LAMPP usando XAMPP. A continuación te describo los pasos que seguimos:

### Instalar LAMPP

- Descargar el archivo de instalación de XAMPP desde la web de Apache Friends, haciendo [click Aquí](https://www.apachefriends.org/es/index.html), seleccionamos el archivo para nuestra plataforma (Linux en este caso) y la guardamos por ejemplo en la carpeta Descarga.

- Una vez finalizada la descarga tendremos un archivo .run, deberemos darle los permisos necesario para ejecutarlo y hacer la instalacion, para eso abriremos la termina y correremos los siguientes comandos.

``` sh
$ cd Descargas 
```

Con esto entraremos en la carpeta descarga, para asignarle los permisos necesarios usaremos el siguiente comando, e ingresar tu clave de usuario:

``` sh
$ sudo chmod 755 xampp-linux-5.6.19-0-installer.run
```

**consejo:**  puedes apoyarte con la tecla tabulador para autocompletar el nombre de archivo, por ejemplo escribes xampp y presionas la tecla tabulador y autocompletara todo.

Para instalar solo necesitamos correr el .run como usuario administrador para ello usamos el comando:

``` sh
$ sudo ./xampp-linux-5.6.19-0-installer.run
```

Esto nos abrirá un asistente de instalación, dejaremos las configuraciones por defecto y haremos click en siguiente  la veces que  necesarias y dejaremos que se completa la instalación: 

![xampp](/images/xampp.png)

si dejamos la casilla marcada y hacemos click en finish, nos mostrar el panel de control de xampp, donde veremos los servicios que estan corriendo, verifiquemos que  estan corriendo los servicios de Apache y MySQL

![xamp_panel](/images/xampp_panel.png)

**Nota:**  Cada vez que quieras acceder a este panel basta con escribir en la terminal

``` sh
$ sudo ./opt/lampp/share/xampp-control-panel/xampp-control-panel
```

Verificaremos que nuestra instalación vaya bien, para eso nos dirigimos al navegador y en la varra de dirección escribimos:

``` sh
localhost
```

![xampp_worked](/images/xampp_worked.jpg)

En la siguiente publicación crearemos la base de datos e instalaremos WordPress, para no hacer mas largo este articulo.

``` python
print exit()
```
