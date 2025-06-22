# Multiprise Connectée - Application Mobile

Application mobile cross-platform (iOS/Android) pour le contrôle à distance d'une multiprise intelligente.

# Application Ionic pour Multiprise Intelligente

Ceci est le code source de l'application mobile pour contrôler une multiprise connectée DIY.

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
