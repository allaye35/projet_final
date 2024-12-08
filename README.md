# projet_final
# Projet Hadoop : Analyse des Évaluations de Films

## Description

Ce projet utilise Hadoop MapReduce pour analyser un ensemble de données de films. L'objectif principal est de déterminer le film le mieux noté pour chaque utilisateur à partir des fichiers `movies.csv` et `ratings.csv`. Ensuite, il compte combien d'utilisateurs ont aimé chaque film et les regroupe par nombre d'utilisateurs.

## Fichiers Inclus

- `movies.csv` : Contient les informations sur les films, avec les colonnes `movieId` et `movieName`.
- `ratings.csv` : Contient les évaluations des films, avec les colonnes `userId`, `movieId`, et `rating`.

## Fonctionnalités

1. **Mapper pour les Évaluations (`RatingsMapper`)** : 
   - Lit le fichier `ratings.csv` et émet des paires (userId, movieId,rating).

2. **Mapper pour les Films (`MoviesMapper`)** : 
   - Lit le fichier `movies.csv` et émet des paires (movieId, movieName).

3. **Reducer (`MovieReducer`)** : 
   - Effectue une jointure des données des deux mappers pour obtenir le nom du film le mieux noté par utilisateur.
   - Compte le nombre d'utilisateurs ayant aimé chaque film et émet les résultats.

4. **Sortie** : 
   - Produit des résultats au format `nombre_d_utilisateurs nom_du_film`.

## Installation et Configuration

### Prérequis

- **Docker** : Assurez-vous que Docker et Docker Compose sont installés sur votre machine.
- **Java** : Java 8 ou supérieur est nécessaire pour compiler le projet.
- **Maven** : Utilisé pour gérer les dépendances et compiler le projet.

### Étapes d'Installation

1. **Cloner le dépôt** :
   ```bash
   git clone <url-du-dépôt>
   cd <nom-du-dossier-du-projet>
