---
layout: post
title: Instalar Go en Linux
---

Una de mis metas para este año 2016 es aprender un nuevo lenguaje de programación, en esta aportunidad quiero aprender Go.
Pero que es Go (o Golang si vas a buscarlo en la web):

![gopher3](/images/gopher3.jpg "gopher3")

### Go

Go, como en su [Pagina Oficial](https://golang.org), definen es un lenguaje de programacion open source diseñado para construir
software simple, cinfiable y eficiente. Estamos hablando de un lenguaje compilado y de tipado fuerte y estatico, que ha llamado
la atención por su velocidad, su manejo de currencia y que permite escalar aplicaciones facilmente. También he de mencionar que
la empresa detrás de Go es Google, así su futuro esta bastante asegurado.

Te preguntarás quienes usan Go hoy en día, he aquí un link con listado de empresas que usan Go:

  - [Listado de Empresas](https://github.com/golang/go/wiki/GoUsers)
  
De todos los casos uno que te invito a leer es el caso de [Iron.io](https://www.iron.io/) y su post [How We Went from 30 Servers to 2: Go](https://www.iron.io/how-we-went-from-30-servers-to-2-go/)
Te estas convenciendo pero quieres una pequeña probada antes de comprometerte, ¡te lo Tengo!, desde la propia pagina Go puedes
experimentar desde la Web con [Go Playground](https://play.golang.org/).

### Instalación en Linux

Si ya estas convencido que quieres aprender Go, ya tenemos el primer requisitos (La motivación),, ahora procedamos a instalarlo en
nuestra PC con GNU/Linux. Lo primero es ir a la sección de descarga de la pagina oficial (aquí esta un [link](https://golang.org/dl/)).
Selecionamos el paquete de acuerdo a nuestra arquitectura ne mi caso 64bits:

  - go1.6.linux-amd64.tar.gz (81MB) (Siendo la ultima disponible para esta fecha)
  
y voy a guardarlo en mi carpeta Descargas (o donde prefieras), abrimos la terminal y nos dirigimos a la carpeta donde esta nuestro 
tar:
  
``` sh
$ cd Descargas
```

ahora ejecutamos el comando tar, pasando la opcion -C [/ruta/a/donde/descomprimir] -xzf [nuestro archivo tar]

``` sh
$ tar -C /usr/local -xzf go1.6.linux-amd64.tar.gz 
```
  
con esto ya tendremos Go en nuestro GNU/Linux, solo falta agregar go a nuestro PATH para ejecutarlo desde cualquier parte,
para eso debemos hacer lo siguiente:
  
``` sh
$ cd ~  # para saltar al Home de nuestro usuario
$ nano .bashrc # en mi caso uso Fedora, pero en la mini tengo LinuxMint así que usaria .profile
```
  
nuestro editor nano abrira nuestro archivo y justoa el final agregamos la siguiente linea:
  
``` sh
export PATH=$PATH:/usr/local/go/bin
```
  
Guardamos con las teclas "Control + O" y salimos con "Control + X", para aplicar estos cambios sin tener que salir de la terminal ejecutamos
  
``` sh
source .bashrc
```
  
y ya tendriamos go accesible en nuestra termina desde cualqueir directorio con el comando
  
``` sh
$ go
```
  
![cowboy-color](/images/cowboy-color.png "cowboy-color")


