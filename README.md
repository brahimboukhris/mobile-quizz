# BBQuiz

BBQuiz est une application de quiz mobile développée avec Flutter et Firebase. Elle permet aux utilisateurs de se connecter, de créer des quizzes personnalisés, de jouer à des quizzes publics, de consulter leur profil et leurs statistiques, et de découvrir des contenus de quiz recommandés.

## Description du projet

L'application propose :

- Authentification Firebase (login par email ou username, inscription)
- Création de quizzes avec questions, réponses et score
- Gestion des quizzes en mode brouillon, privé ou public
- Lecture des quizzes publics et sauvegarde des résultats
- Recherche de quizzes et écran d'exploration
- Interface principale avec navigation par onglets (home, mes quizzes, créer, profil)
- Intégration Firestore pour stocker les quizzes, les utilisateurs et les résultats

## Architecture

Le projet utilise les dossiers suivants :

- `lib/` : code Flutter principal
  - `main.dart` : point d'entrée de l'application
  - `screens/` : écrans de l'application
  - `services/` : services Firebase et logique métier
  - `models/` : modèles de données de quiz
  - `theme/` : thème visuel
  - `widgets/` : composants réutilisables
- `android/`, `ios/`, `web/`, `windows/`, `macos/`, `linux/` : plateformes supportées par Flutter
- `pubspec.yaml` : dépendances et ressources du projet

## Fonctionnalités principales

- Écran d'accueil avec navigation vers connexion et inscription
- Connexion par email ou par username
- Inscription et gestion des erreurs de formulaire
- Écran principal avec message de bienvenue et quiz du jour
- Recherche de quizzes
- Affichage des quizzes recommandés
- Création de quiz avec :
  - titre, description, catégorie, difficulté
  - questions à choix multiples
  - sélection du bon choix
  - status `draft`, `private` ou `public`
- Sauvegarde automatique des résultats dans Firestore
- Historique et favoris de quiz

## Installation

### Prérequis

- Flutter installé
- SDK Dart compatible
- Un projet Firebase configuré avec `firebase_options.dart`
- Un simulateur/emulateur ou un appareil réel

### Étapes

1. Clonez le projet :

```bash
git clone https://github.com/brahimboukhris35/Projet-mobile-27-04-26.git
cd Projet-mobile-27-04-26
```

2. Installez les dépendances :

```bash
flutter pub get
```

3. Lancez l'application :

```bash
flutter run
```

> Pour exécuter sur le web : `flutter run -d chrome`

## Configuration Firebase

Le projet s'appuie sur Firebase pour l'authentification et Firestore. Assurez-vous d'avoir configuré les fichiers de configuration Firebase pour votre plateforme :

- `lib/firebase_options.dart`
- `android/app/google-services.json`
- `ios/Runner/GoogleService-Info.plist`

## Remarques

- Le statut `public` exige un minimum de 10 questions pour publier un quiz.
- Les brouillons expirent après 7 jours.
- Le projet dispose d'un thème personnalisé et de composants d'interface réutilisables.

## Auteur

Brahim Boukhris

