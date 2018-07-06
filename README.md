# Idéal Biens SA

## Introduction
Idéal Biens SA est une application de gestion de visites pour une agence immobilière. Elle a été crée grâce à JHipster en guise d'application de démonstration pour le Travail de Bachelor.

## Prérequis
Il faut avoir installer les éléments suivants:
- Java 8
- Node.Js
- Yarn
- Yeoman
- Docker

## Configuration de l'application
- JHipster 4.14.3
- Application monolithique
- Base de données MySQL pour le développement et la production dans un docker
- PhyMyadmin dans un docker
- Angular 5
- JWT authentification
- Maven
- Developper sur IntelliJ
- Kitematic



## Modèle de données
MCD

![](https://github.com/x-xira25-x/JhipsterMonoMySql/blob/master/ModeleDonnees/MCD2.PNG)

MLD
![](https://github.com/x-xira25-x/JhipsterMonoMySql/blob/master/ModeleDonnees/MLD2.PNG)

## Structure du projet
![](https://github.com/x-xira25-x/JhipsterMonoMySql/blob/master/structure.PNG)


## Manuel d'utilisation

 - Avant de générer le projet, il faut installer et configurer les dépendances: Node.js et Yarn
 - Après l'installation de Node, exécuter la commande ci-dessous pour installer les outils de développement
 ``yarn install   ``
 - Cloner le projet
-  Lancer les dockers, il faut qu'ils soient dans le même réseau :

   ``docker-compose -f src/main/docker/mysql.yml up``
 
-  Lancer le client

   ``yarn start``

- Lancer le serveur

   ``./mvnw ``
<ul>
    <li>PhpMyAdmin:</li>
    <ul>
        <li>pseudo: root</li>
        <li>mot de passe : 1234</li>
    </ul>
</ul>

## Installation de PHPMyAdmin
La première chose à faire est d'arreter tous les conteneurs docker. Puis lancer la commande suivante
``docker-compose up -d du https://hub.docker.com/r/phpmyadmin/phpmyadmin/  ``

Il est important que le conteneur docker contenant PHPMyAdmin tourne sur le même réseau que le conteneur contenant la base de données.

Le plus simple est d'installer Kitematic pour lancer les conteneurs docker.

PHPMyAdmin est accessible à l'adresse : http://localhost:9191/

## Contexte
Cette application est destinée pour les agences immobilières. Elle leur permet de mettre en avant des biens à vendre et de ce fait, les clients ont la possibilité de s'inscrire, d'effectuer des recherches et s'inscrire à des visites que proposent les agents immobiliers.

## Utilisateurs de l'application
L'application dispose de 4 types d'utilisateurs:

- Public
- Client : vendeur ou acheteur
- Agent immobilier
- Admnistrateur

#### Public
L'utilisateur en public peut accéder à l'onglet "a vendre" et ainsi voir les biens mis en vente. Il peut également effectuer un filtre par type de bien.

#### Client : vendeur ou acheteur
En s'inscrivant sur l'application, le client peut etre un vendeur et/ou un acheteur. Il peut accéder à l'onglet "a vendre", voir les biens mis en vente et également effectuer un filtre par type de bien. Il a la possibilité de s'inscrire à des visites et dispose d'un onglet "visites" pour voir les visites auxquelles il est inscrit. Il dispose d'un bouton pour se désister d'une visite.


#### Agent immobilier
L'agent immobilier est créé depuis le compte administrateur. Il peut accéder à l'onglet "a vendre" et peut créer, supprimer, modifier les diverses entités suivantes:
- bien
- client
- agent immobilier
- visite

#### Admnistrateur
L'administrateur dispose d'un onglet "administration" qui lui permet de controler divers paramètres de l'application.

### Comptes

<ul>
    <li>Client:</li>
    <ul>
        <li>Login: client </li>
        <li>mot de passe: 1234 </li>
    </ul>
</ul>
<ul>
    <li>Agent immobilier:</li>
    <ul>
        <li>Login: agent</li>
        <li>mot de passe: 1234</li>
    </ul>
</ul>
<ul>
    <li>Administarteur:</li>
    <ul>
        <li>Login: admin</li>
        <li>mot de passe: admin</li>
    </ul>
</ul>

### Remarque

Lors qu'un user est créé depuis un compte administrateur ou agent immobilier son mot de passe est par défaut: 1234






