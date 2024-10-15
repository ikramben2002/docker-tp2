## Introduction

Ce projet consiste à créer un environnement Docker pour déployer une application web utilisant PHP, NGINX, et une base de données SQL. L'objectif est de suivre plusieurs étapes pour configurer les conteneurs nécessaires et d'utiliser Git pour le versionnement.

## Prérequis

- Docker installé sur votre machine
- Connaissances de base en utilisation de la ligne de commande
- Un navigateur web

## Étapes du projet

### Étape 0 - Initialisation

1. **Stopper et supprimer tous les conteneurs existants :**
   
docker stop $(docker ps -aq)
docker rm $(docker ps -aq)

### Étape 1 - Configuration de base
Créer 2 conteneurs :
HTTP : Un conteneur avec un serveur HTTP qui écoute sur le port 8080.
SCRIPT : Un conteneur avec un interpréteur PHP et le protocole FPM pour NGINX.
Créer index.php :
Ce fichier doit exécuter la fonction php_info() et se trouver dans /app.

### Étape 2 - Ajout d'une base de données
Créer 3 conteneurs :
HTTP, SCRIPT, et DATA (pour la base de données SQL).
Créer test_bdd.php :
Ce fichier doit exécuter au moins 2 requêtes CRUD.

### Étape 3 - Intégration de WordPress
Remplacer les pages PHP par WordPress :
Installer WordPress dans le conteneur SCRIPT.

### Étape 4 - Utilisation de Docker Compose
Convertir la configuration en Docker Compose :
Créer un fichier docker-compose.yml 

### Instructions d'installation et d'exécution

Pour chaque étape :
cd etape<numero-etape>
chmod +x ./setup.sh
./setup.sh
