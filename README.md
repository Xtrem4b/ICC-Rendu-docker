Pour l'exercice 2.3:

Afin d'éviter les problèmes liés au VPN, je passe pas un subnet. Il faut lancer dans un terminal
cette commande: docker network create --subnet=10.242.0.0/24 subNet


Acceder depuis le terminal au dossier Exercice 2.3 et lancer la commande: docker-compose up.
Parfois il est possible qu'après l'installation il y est un conflit entre wordpress et mysql,
il suffit de relancer docker-compose up en root.

Pour tester il faut ouvrir un navigateur et aller sur l'adresse donnée dans le terminal, le launcher de 
wordpress s'ouvrira puis il suffira de finir l'installation.


Pour l'exercice 3:

taper dans le terminal: docker network create --subnet=10.243.0.0/24 subNet2

Se rendre dans le dossier exercice 3, lancer en root la commande docker-compose up, attendre que tout 
s'installe. Le container contenant le jar s'eteindra automatique à la fin de son installation. Pour
accèder à son application il faut faire dans un terminal:

xhost +
docker run -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=unix$DISPLAY containerTest

Sinon pour acceder au serveur web, il suffit de lancer dans son navigateur localhost.
Pour accèder à phpmyadmin il faut aller sur localhost:8080, à partir de là pour se connecter il faut mettre root en username et root en mot de passe. Pour tester la base de donnée, il suffit de créer
une bdd depuis phpmyadmin puis une table.
