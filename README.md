		CONTENER DOCKER AVEC :
		
	PHP 7.3
	DB MySQL
	PHP MyAdmin
	MailDev

# article pour suivre le tuto 
https://yoandev.co/un-environnement-de-d%C3%A9veloppement-symfony-5-avec-docker-et-docker-compose/

# Principales commande 

 - $ docker-compose build
    -> lance le build des conteneurs du projet 


 - $ docker-compose up -d
    -> ouvrir le conteneurs

 - $ docker exec www_docker_symfony composer create-project symfony/website-skeleton project
    ->nouveau projet symmfony

dans le dossier projet 
 - $ cd project
 
 - $ ls -l
    -> on remarque le propriétaire est root

 - projst$ sudo chown -R $USER ./
    -> changer le propriétaire des fichier (root -> yt)


## parameter la base de donner dans le ficher .env

 - DATABASE_URL=mysql://root:@db_docker_symfony:3306/db_test?serverVersion=5.7

et puis se connecter dans le shell du docker 

 - $ docker exec -it www_docker_symfony bash
    ->shel conteneur 
 - /var/www# cd project
 - /var/www/project# php bin/console doctrine:database:create
     ->symfo db create
 =Created database \`db_name\` for connection named default


## parameter mail dev dans le fichier .env


