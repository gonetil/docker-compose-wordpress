# Docker-compose file for a typical Wordpress project

Includes Docker containers for Apache2, MySQL, PHP-FPM and PhpMyAdmin.
Versions for php, apache2 and mysql are parametrized in .env file

Database initialization can be done by putting SQL files inside docker-compose/mysql directory.
Additional php extensions can be installed by editing docker-compose/php/Dockerfile file.


## Usage
Both docker and docker-compose must be installed first.

```bash
mkdir wp_project
git pull https://github.com/gonetil/docker-compose-wordpress.git wp_project
cd wp_project
docker-compose build
```
If you have a pre-existing wordpress project, make sure to copy all WP files into wordpress subdirectory and MySQL dump into docker-compose/mysql .

If you are starting a fresh new wordpress proyect, lets download the latest Wordpress version:
```bash
wget https://wordpress.org/latest.tar.gz
tar -xzf latest.tar.gz
```

When configuring Wordpress, make sure you use all parameters in .env file for MySQL connection (**use "mysql" for database host**)



