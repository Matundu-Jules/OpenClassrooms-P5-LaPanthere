# Kanap - OpenClassrooms P5

Kanap est un projet développé dans le cadre de la formation OpenClassrooms. 

Ce projet vise à créer une plateforme de e-commerce pour la marque de canapés Kanap, permettant de vendre leurs produits en ligne en plus de leur boutique physique. 

Le site comprend une partie front-end en JavaScript pur et une API back-end.

## Scénario

En tant que développeur web dans une agence de développement, vous êtes chargé de rendre dynamique le site e-commerce de Kanap en intégrant les éléments de l'API. 

Le site doit permettre aux utilisateurs de parcourir les produits, de les ajouter au panier et de passer des commandes.

## Technologies utilisées

- **HTML**
- **CSS**
- **JavaScript (pur, sans framework)**
- **Webpack**
- **Babel**
- **API REST**

## Fonctionnalités Principales

- **Page d'accueil** : Affiche dynamiquement tous les articles disponibles à la vente.
- **Page Produit** : Affiche dynamiquement les détails d'un produit sélectionné, avec options de personnalisation et ajout au panier.
- **Page Panier** : Permet de modifier les quantités, supprimer des produits, et passer une commande avec validation des données.
- **Page Confirmation** : Affiche un message de confirmation et l'identifiant de commande.
- **Amélioration de l'Accessibilité** : Mise en œuvre des meilleures pratiques pour assurer que le site soit accessible à tous les utilisateurs.

## Installation

### Prérequis Backend

Vous devez avoir **Node** et **npm** installés localement sur votre machine.

### Installation Backend

1. Clonez ce repository.
2. Depuis le dossier back du projet, installez les dépendances :
```bash
cd back
npm install
```

3. Démarrez le serveur avec :
```bash
node server
```

Le serveur devrait fonctionner sur **localhost** avec le port par défaut *3000*. 

Si le serveur utilise un autre port, cela sera indiqué dans la console lorsque le serveur démarre (e.g. Listening on port *3001*).

### Installation Frontend

1. Depuis le dossier front du projet, installez les dépendances :
```bash
cd ../front
npm install
```
2. Démarrez le serveur local avec :
```bash
npm start
```

## API

L'API back-end est utilisée pour gérer les produits et les commandes. 

Voici les détails des **endpoints** disponibles :

### GET /api/products

- **Description** : Retourne tous les produits disponibles.
- **Réponse** : Tableau d'objets produits avec les champs *colors*, *id*, *name*, *price*, *imageUrl*, *description*, *altTxt*.

### GET /api/products/{product-ID}

- **Description** : Retourne un produit spécifique par son ID.
- **Paramètres** : {**product-ID**} - L'identifiant du produit.
- **Réponse** : Objet produit correspondant à l'ID.

### POST /api/order

- **Description** : Passe une commande.
- **Paramètres** : Objet JSON contenant les informations de contact et un tableau des IDs de produits.
- **Corps de la demande** :
```bash
{
  "contact": {
    "firstName": "string",
    "lastName": "string",
    "address": "string",
    "city": "string",
    "email": "string"
  },
  "products": ["product-ID1", "product-ID2", ...]
}
```
- **Réponse** : Objet contenant les informations de contact, le tableau des produits, et l'identifiant de commande (**orderId**).

## Points Forts

- **Intégration Dynamique** : Unification des travaux front-end et back-end pour créer une expérience utilisateur fluide et interactive.
- **SEO et Accessibilité** : Mise en œuvre des meilleures pratiques pour assurer une meilleure visibilité sur les moteurs de recherche et une accessibilité optimale pour tous les utilisateurs.
- **Code Bien Structuré** : Utilisation de fonctions courtes et réutilisables, avec des commentaires clairs pour chaque fonction.
- **Performance Optimisée** : Amélioration de la vitesse de chargement des pages pour une meilleure performance utilisateur.
- **Tests et Validation** : Planification et réalisation de tests d’acceptation pour garantir la qualité et la fiabilité des fonctionnalités.

## Informations

Ce projet est destiné à démontrer mes compétences en développement web et n'est pas destiné à une utilisation commerciale.
