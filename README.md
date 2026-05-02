ce repo contient les etapes de l installation et de l utilisation de burp suite 

Ce fichier contient les étapes d'installation ET d'utilisation de Burp Suite:

## 🎯 Objectif

Cette application permet de comprendre :
- L'interception et l'analyse des requêtes HTTP avec Burp Suite
- Les injections SQL dans les formulaires de connexion
- La manipulation des paramètres avec Burp Suite
- La gestion des sessions et des cookies

## 🚀 Installation

### Prérequis
- Node.js installé

### Configuration

git clone https://github.com/aishide/Burp_suit_test_website.git
cd Burp_suit_test_website
npm install
npm start

Le serveur démarre sur http://localhost:3000

### Vulnérabilités intégrées
Vulnérabilité     	                Description
Injection SQL	                      Contournement de l'authentification
Absence de limite	                  Attaques par force brute possibles
Communication non sécurisée	        Pas de HTTPS, identifiants en clair
Absence de validation	              Entrées utilisateur non filtrées


### Test avec Burp Suite
Configuration

Configurer le proxy Burp Suite (127.0.0.1:8080)
Configurer le navigateur sur le proxy Burp
Activer l'interception

### Scénarios de test
Connexion normale

Nom d'utilisateur : admin
Mot de passe : admin123

### Injection SQL

Nom d'utilisateur : admin' --
Mot de passe : n'importe quoi

### Manipulation des paramètres

Intercepter la requête de connexion
Modifier les paramètres
Transmettre la requête modifiée

### Éléments à observer dans Burp

Requête brute (Raw)
Paramètres dans le corps POST
En-têtes HTTP
Réponse du serveur

### Structure
text
Burp_suit_test_website/
├── server.js
├── package.json
├── public/
│   ├── index.html
│   ├── dashboard.html
│   └── style.css
└── README.md

### Avertissement
Cette application est volontairement vulnérable. Ne pas déployer en production ou sur Internet.
