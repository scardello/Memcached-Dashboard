Memchaced Dashboard
===================

Q&D Setup & Start
-----------------

1. Clone repo:

```git clone https://github.com/scardello/Memcached-Dashboard.git```

2. Asegurarse de levantar memcached localmente y ejecutando en el puerto por defecto (11211)

3. Levantar el docker con el server:
```
> cd Memcached-Dashboard
> docker-compose up
```

Si se desea levantar el servicio en 2do plano utilizar la opción -d (`docker-compose up -d`). Para más info de como ejecutar/detener/eliminar/etc ir a [el README del docker](phpdocker/README.md) 

4. Finalmente ingresar al servicio en [localhost:9000](http://localhost:9000) con el user:admin y pass:admin

Original Info
-------------

A dead simple single file Memcached stats dashboard in PHP. The dashboard shows a few basic stats on the configured server and allows to delete/set keys and flush all data.
All assets (CSS ans JavaScript) are loaded from CDN's.

Version
----

0.1.1


##ScreenShots

[![Login](http://i.imgur.com/8H0Yzq4s.png "Login")](http://i.imgur.com/8H0Yzq4.png)
[![Server Info](http://i.imgur.com/VxZIQw7s.png "Server Info")](http://i.imgur.com/VxZIQw7.png)
[![Charts](http://i.imgur.com/mojwMous.png "Charts")](http://i.imgur.com/mojwMou.png)
[![Stored Values](http://i.imgur.com/E1Uebrls.png "Stored Values")](http://i.imgur.com/E1Uebrl.png)


Installation
--------------

```sh
git clone https://github.com/bainternet/Memchaced-Dashboard Memchaced-Dashboard
```

Usage
------
Simple point your browser to installed directory

Default username: admin

Default Password: admin

Change server IP, Port or Default user

```PHP
$ip = '192.23.23.23'; //set your ip address def: 127.0.0.1
$port = '11311'; //set your port def: 112211
$users = array(
    'admin' => 'some_hard_to_crack_pass@$%^',
    'another_user' => 'another_pass'
);
new Simple_memchached_dashboard($ip,$port,$users);
```
License
----

MIT

This Script uses the following resources:
* DataTables - is free open source software, available under the [MIT license](http://www.datatables.net/license/mit).
* Twitter Bootstrap  licensed under [Apache License v2.0](http://www.apache.org/licenses/LICENSE-2.0).
* morris.js licensed under [Simplified BSD License](http://morrisjs.github.io/morris.js/index.html).
* alertify.js is licensed under [MIT](http://www.opensource.org/licenses/MIT).
* jQuery  is licensed [MIT license](http://en.wikipedia.org/wiki/MIT_License).

