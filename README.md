# Multiprise Connectée - Application Mobile

Application mobile cross-platform (iOS/Android) pour le contrôle à distance d'une multiprise intelligente.

# Application Ionic pour Multiprise Intelligente

Ceci est le code source de l'application mobile pour contrôler une multiprise connectée DIY.

## Vue d'ensemble
Application mobile cross-platform développée avec Ionic 7 et Angular 17 pour contrôler des multiprises intelligentes connectées. 
L'application permet de :

* Contrôler individuellement chaque prise à distance
* Monitorer la consommation énergétique en temps réel
* Programmer des horaires automatiques
* Créer des scénarios personnalisés
* Recevoir des alertes de sécurité
* Analyser les données de consommation

## Architecture Technique - Stack Technologique

* Frontend: Ionic 7 + Angular 17
* Backend: Node.js + Express (API REST)
* Base de données: PostgreSQL + InfluxDB (time series)
* Temps réel: WebSocket + MQTT
* Mobile: Capacitor pour iOS/Android
* Cloud: AWS/GCP pour synchronisation

## Fonctionnalités Principales

- Interface responsive et intuitive
- Mode hors ligne avec synchronisation
- Notifications push natives
- Graphiques de consommation interactifs
- Authentification sécurisée (JWT)
- Contrôle vocal (Google/Alexa)
- Export de données (PDF/CSV)

## Architecture
- **Framework Applicatif**: Ionic avec Angular
- **Protocole de Communication**: MQTT
- **Broker par défaut**: `broker.hivemq.com`

## Structure des Topics MQTT

- Commande d'une prise (PUBLISH par l'app): `multiprise/relais/{ID}/commande` (Payload: `ON` ou `OFF`)
- État d'une prise (SUBSCRIBE par l'app): `multiprise/relais/{ID}/etat` (Payload: `ON` ou `OFF`)

## Comment lancer
1. `npm install`
2. `ionic serve`
