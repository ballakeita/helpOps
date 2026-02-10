# HELP'OPS - Plateforme de Gestion des Incidents

**Projet JAVA – Sockets/RMI 2025-2026**  
MCPR - Modèles et Concepts du Parallélisme et de la Répartition

---

## 📋 Description

HELP'OPS est une plateforme distribuée permettant la gestion des incidents et des interventions au sein d'une organisation. Elle assure le signalement des problèmes, leur prise en charge, leur suivi et leur résolution.

### Version 1 : Fondations Fonctionnelles

La version 1 établit les bases de la plateforme avec trois fonctionnalités principales :

✅ **Authentification des utilisateurs**
- Connexion avec identifiant et code/mot de passe
- Délivrance d'un jeton d'authentification
- Vérification du jeton pour accès aux services

✅ **Déclaration d'incident**
- Création d'incident par utilisateur authentifié
- Champs requis : catégorie, titre, description
- Identifiant unique généré automatiquement
- État initial : OPEN

✅ **Consultation des incidents**
- Liste des incidents déclarés par l'utilisateur
- Affichage du détail : ID, état, informations, date de création

---

## 🏗️ Architecture

### Services

- **AuthenticationService** : Gestion de l'authentification et jetons
- **IncidentService** : Gestion du cycle de vie des incidents
- **ClientApplication** : Interface utilisateur

### Technologies

- **Langage** : Java
- **Communication distribuée** : Sockets / RMI
- **Persistance** : À définir

---

## 📁 Structure du Projet

```
helpOps/
├── README.md
├── .gitignore
│
├── src/
│   ├── models/          # Entités (User, Incident, AuthToken, ...)
│   ├── services/        # Logique métier (Authentication, Incidents)
│   └── client/          # Application client
│
└── docs/                # Documentation (UML, rapports, spécifications)
```

---

## 🚀 Démarrage

### Prérequis
- Java 11+
- Maven (optionnel)

### Compilation
```bash
javac -d bin src/**/*.java
```

### Exécution
```bash
# Lancer le serveur d'authentification
java -cp bin services.AuthenticationService

# Lancer le serveur d'incidents
java -cp bin services.IncidentService

# Lancer le client
java -cp bin client.ClientApplication
```

---

## 📊 Modèle de Données Minimal

### User
- `id` : String (identifiant unique)
- `password` : String (code confidentiel)

### Incident
- `id` : String (identifiant unique généré)
- `userId` : String (référence utilisateur)
- `category` : String
- `title` : String
- `description` : String
- `state` : IncidentState (OPEN)
- `createdDate` : LocalDateTime

### AuthToken
- `token` : String (jeton d'authentification)
- `userId` : String
- `expirationDate` : LocalDateTime

---

## 📅 Échéances

- **Version 1** : 03/02/2026 ✓ (Authentification + Incidents)
- **Version 2** : 16/02/2026 (Assignation aux agents)
- **Version 3** : 09/03/2026 (Résolution + Statistiques)
- **Version 4** : 17/03/2026 (Supervision temps réel)

---

## 👥 Équipe

Projet de groupe de 4 étudiants

---

## 📝 Livrables Attendus

- [x] Conception UML
- [x] Interfaces de service
- [ ] Implémentation services
- [ ] Application client
- [ ] Rapport technique
- [ ] Code commenté

---

## 📖 Notes

*Plateforme en développement incrémental. Les versions suivantes ajouteront la prise en charge par agents, la résolution d'incidents, les statistiques et la supervision temps réel.*

