---
layout: página
title: Generador de aplicaciones Express
description: Aprenda cómo utilizar la herramienta del generador de aplicaciones Express para crear rápidamente un esqueleto para sus aplicaciones Express.js, configuración de streamlining y configuración.
menu: iniciador
lang: es
redirect_from: /es/starter/generator.html
---

# Generador de aplicaciones Express

Utilice la herramienta de generador de aplicaciones, `express`, para crear rápidamente un esqueleto de aplicación.

Puede ejecutar el generador de aplicaciones con el comando `npx` (disponible en Node.js 8.2.0).

```bash
$ npx express-generator
```

Para versiones anteriores de Node, instale el generador de aplicaciones como un paquete global npm y luego ejecute:

```bash
$ npm install -g express-generator
$ express
```

Muestre las opciones de mandato con la opción `-h`:

```bash
$ express -h

  Usage: express [options] [dir]

  Options:

    -h, --help          output usage information
        --version       output the version number
    -e, --ejs           add ejs engine support
        --hbs           add handlebars engine support
        --pug           add pug engine support
    -H, --hogan         add hogan.js engine support
        --no-view       generate without view engine
    -v, --view <engine> add view <engine> support (ejs|hbs|hjs|jade|pug|twig|vash) (defaults to jade)
    -c, --css <engine>  add stylesheet <engine> support (less|stylus|compass|sass) (defaults to plain css)
        --git           add .gitignore
    -f, --force         force on non-empty directory
```

Por ejemplo, el código siguiente crea una aplicación Express denominada _myapp_. La aplicación será creada en una carpeta llamada _myapp_ en el directorio de trabajo actual y el motor de vistas será asignado a <a href="https://pugjs.org/" target="_blank" title="Documentación de Pug">Pug</a>:

```bash
$ express --view=pug myapp

   create : myapp
   create : myapp/package.json
   create : myapp/app.js
   create : myapp/public
   create : myapp/public/javascripts
   create : myapp/public/images
   create : myapp/routes
   create : myapp/routes/index.js
   create : myapp/routes/users.js
   create : myapp/public/stylesheets
   create : myapp/public/stylesheets/style.css
   create : myapp/views
   create : myapp/views/index.pug
   create : myapp/views/layout.pug
   create : myapp/views/error.pug
   create : myapp/bin
   create : myapp/bin/www
```

A continuación, instale las dependencias:

```bash
$ cd myapp
$ npm install
```

En MacOS o Linux, ejecute la aplicación con este mandato:

```bash
$ DEBUG=myapp:* npm start
```

En Windows, utilice este mandato:

```bash
> set DEBUG=myapp:* & npm start
```

En Windows PowerShell, utilice este comando:

```bash
PS> $env:DEBUG='myapp:*'; npm start
```

A continuación, cargue `http://localhost:3000/` en el navegador para acceder a la aplicación.

La aplicación generada tiene la siguiente estructura de directorios:

```bash
.
├── app.js
├── bin
│   └── www
├── package.json
├── public
│   ├── images
│   ├── javascripts
│   └── stylesheets
│       └── style.css
├── routes
│   ├── index.js
│   └── users.js
└── views
    ├── error.pug
    ├── index.pug
    └── layout.pug

7 directories, 9 files
```

<div class="doc-box doc-info" markdown="1">
La estructura de la aplicación creada por el generador es sólo una de las muchas formas de estructurar las aplicaciones Express. Puede utilizar esta estructura o modificarla según sus necesidades.
</div>

### [Anterior: Hola Mundo](/{{ page.lang }}/starter/hello-world.html)&nbsp;&nbsp;&nbsp;&nbsp;[Siguiente: Enrutamiento básico](/{{ page.lang }}/starter/basic-routing.html)
