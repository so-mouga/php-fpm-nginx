# Docker-PHP7 - Kevin Mougammadaly

Une application qui permettra d'avoir les environnements suivants: 
- nginx
- php7.0-fpm avec les extensions suivantes activée: PDO, GD
- Mysql 5.*

## Utilisation
~~~
Désarchiver le projet sur votre ordinateur 

placer vous sur ce projet 
- cd docker-php7

Exécutez le fickier docker compose
- docker-compose up -d

~~~

Une fois les conteneurs prêts et démarrés, ouvrez l'url http://localhost:8080 dans le navigateur. Si tout s'est bien passé la version de PHP apparaît.
Pour accéder à la base donnée ouvrez l'url http://localhost:8081.

### Structure

~~~
├── app
│   └── public
│       └── index.php
├── database
├── docker-compose.yml
├── fpm
│   ├── Dockerfile
│   └── supervisord.conf
├── nginx
│   ├── Dockerfile
│   └── default.conf
~~~

- `app` :
Contiendra tous le projet php, Nginx pointe sur le dosier `app/public`.
- `database` :
Contient les fichiers SQL avec les requétes à exécuter au démmarage de docker.


