# Medical'ia — Accès aux Soins par l'IA

![Statut](https://img.shields.io/badge/Statut-En%20cours%20de%20développement-orange)
![Type](https://img.shields.io/badge/Type-HealthTech-teal)
![Formation](https://img.shields.io/badge/Formation-ASRC-green)
![École](https://img.shields.io/badge/%C3%89cole-IMIE--Paris-orange)
![Frontend](https://img.shields.io/badge/Frontend-Disponible-brightgreen)

> ⚠️ **Projet en cours de développement** — Le frontend est fonctionnel. Les fonctionnalités IA, la base de données et les API de géolocalisation sont en cours d'intégration.

Projet **Medical'ia** (nom de marque : **Mozes'IA**) — Plateforme d'intelligence artificielle pour faciliter l'accès aux soins dans les zones sous-desservies.

🔗 **Démo frontend** : [carmand237.github.io/medalia-healthtech](https://carmand237.github.io/medalia-healthtech)

---

## Vision

Medical'ia vise à réduire les inégalités d'accès aux soins en proposant une solution IA capable d'orienter les patients vers les structures médicales adaptées, en particulier dans les déserts médicaux et les régions à faible densité de professionnels de santé.

---

## Problématique

- **Déserts médicaux** : millions de personnes sans médecin traitant accessible
- **Délais de prise en charge** : plusieurs semaines / mois pour certaines spécialités
- **Manque d'information** : patients mal orientés, recours aux urgences inadaptés
- **Fracture numérique & géographique** : inégalités d'accès aux plateformes existantes

---

## Frontend — Pages disponibles

| Page | Fichier | Description |
|------|---------|-------------|
| Accueil | `index.html` | Landing page — choix du profil utilisateur |
| Espace Patient | `patient.html` | Chatbot IA, recherche médecin, carte soins |
| Espace Médecin | `medecin.html` | Agenda, gestion patientèle, disponibilités |
| Espace Collectivité | `collectivite.html` | Tableau de bord territorial, indice désert médical |

---

## Architecture technique (cible)

```
┌──────────────────────────────────────────────────────────┐
│                    Couche Présentation                    │
│         Web App (HTML/Tailwind)  ·  Mobile App (PWA)     │
└───────────────────────────┬──────────────────────────────┘
                            │ HTTPS / API REST
┌───────────────────────────▼──────────────────────────────┐
│                    Couche Application  [EN COURS]        │
│   Moteur IA d'orientation  ·  API Ressources de Santé    │
│   Gestion utilisateurs (IAM)  ·  Notifications           │
└───────────────────────────┬──────────────────────────────┘
                            │
┌───────────────────────────▼──────────────────────────────┐
│                    Couche Données  [EN COURS]            │
│   Base de données patients (chiffrée)                    │
│   Dataset structures de santé (~1 306 entrées, 132 cols) │
│   Logs d'accès (traçabilité RGPD)                        │
└──────────────────────────────────────────────────────────┘
```

## Roadmap

| Phase | Contenu | Statut |
|-------|---------|--------|
| Phase 1 — Frontend | Pages index, patient, médecin, collectivité | ✅ Terminé |
| Phase 2 — Backend API | Endpoints REST, authentification, IAM | 🔄 En cours |
| Phase 3 — Moteur IA | Chatbot orientation, NLP, classification | 🔄 En cours |
| Phase 4 — Data | Intégration dataset santé, géolocalisation temps réel | 📅 Prévu |
| Phase 5 — Conformité | Certification HDS, audit RGPD | 📅 Prévu |

---

## Sécurité & Conformité (cible)

| Exigence | Implémentation |
|----------|----------------|
| HDS (Hébergeur Données de Santé) | Hébergement certifié, chiffrement AES-256 |
| RGPD | Consentement explicite, droit à l'oubli, DPO désigné |
| Authentification | MFA obligatoire pour les professionnels de santé |
| Traçabilité | Logs d'accès horodatés, conservation 10 ans |
| Disponibilité | Architecture redondante, RTO < 4h |

---

## Branding

Noms finalistes explorés lors de la phase de conception :
`Viciné` · `Sanori` · `Oraya` · `Curia` → **Medical'ia / Mozes'IA** retenu

---

## Structure du repo

```
medalia-healthtech/
├── README.md
├── index.html          ← Landing page (choix profil)
├── patient.html        ← Espace patient
├── medecin.html        ← Espace médecin
├── collectivite.html   ← Espace collectivité
├── docs/
│   ├── cahier-des-charges.md
│   ├── architecture-si.md
│   └── conformite-hds-rgpd.md
├── data/
│   └── dataset-structures-sante/
└── design/
    └── branding/
```

---

## Auteur
**Armand CHUIGWA** — ASRC RNCP39611 Niveau 6 — IMIE Paris 2025-2026
