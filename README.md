# HELP'OPS - Plateforme de Gestion des Incidents

**Projet JAVA – Sockets/RMI 2025-2026**

---

## 📋 Description

HELP'OPS est une plateforme distribuée de gestion des incidents permettant :
- ✅ Authentification des utilisateurs (jeton)
- ✅ Déclaration d'incidents (catégorie, titre, description)
- ✅ Consultation des incidents déclarés

---

## 🛠️ Setup & Workflow Git

### 1️⃣ Cloner le repo
```bash
git clone https://github.com/ballakeita/md-to-confluence-test.git
cd helpOps
```

### 2️⃣ Créer votre branch (NE JAMAIS travailler sur `main`)
```bash
git checkout -b votre-nom
git pull origin main
```

### 3️⃣ Développer & Tester
```bash
# Faire vos modifs
git add .
git commit -m "Description du changement"
```

### 4️⃣ Avant de pusher
```bash
git pull origin main  # Se mettre à jour(Tester avec l'ensemble de l'equipe avant de mettre votre code sur le main)
```

### 5️⃣ Push & Pull Request
```bash
git push origin votre-nom
```
Ensuite, créez une **Pull Request** sur GitHub pour review en équipe avant merge sur `main`.

---

## 📁 Structure

```
helpOps/
├── src/
│   ├── models/     # Entités (User, Incident, AuthToken)
│   ├── services/   # Services (Auth, Incidents)
│   └── client/     # Application client
└── docs/           # Documentation
```

---

##  Échéances

- **V1** : 03/02/2026 (Auth + Incidents)
- **V2** : 16/02/2026 (Assignation agents)
- **V3** : 09/03/2026 (Résolution + Stats)
- **V4** : 17/03/2026 (Supervision temps réel)

