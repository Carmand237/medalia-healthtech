# Medical'ia — Accès aux Soins par l'IA

![Statut](https://img.shields.io/badge/Statut-En%20cours-yellow)
![Type](https://img.shields.io/badge/Type-HealthTech-teal)
![Formation](https://img.shields.io/badge/Formation-ASRC-green)
![École](https://img.shields.io/badge/%C3%89cole-IMIE--Paris-orange)

Projet **Medical'ia** — Plateforme d'intelligence artificielle pour faciliter l'accès aux soins dans les zones sous-desservies.

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

## Solution

Plateforme intelligente combinant :
- **Moteur d'orientation IA** : analyse des symptômes et orientation vers le professionnel adapté
- **Géolocalisation des ressources de santé** : carte interactive des structures disponibles (urgences, spécialistes, généralistes, téléconsultation)
- **Gestion de données de santé sécurisée** : conformité HDS (Hébergeur de Données de Santé) et RGPD

---

## Architecture technique (cible)

```
┌──────────────────────────────────────────────────────────┐
│                    Couche Présentation                    │
│         Web App (React)  ·  Mobile App (PWA)             │
└───────────────────────────┬──────────────────────────────┘
                            │ HTTPS / API REST
┌───────────────────────────▼──────────────────────────────┐
│                    Couche Application                     │
│   Moteur IA d'orientation  ·  API Ressources de Santé    │
│   Gestion utilisateurs (IAM)  ·  Notifications           │
└───────────────────────────┬──────────────────────────────┘
                            │
┌───────────────────────────▼──────────────────────────────┐
│                    Couche Données                         │
│   Base de données patients (chiffrée)                    │
│   Dataset structures de santé (~1 306 entrées, 132 cols) │
│   Logs d'accès (traçabilité RGPD)                        │
└──────────────────────────────────────────────────────────┘
```

## Sécurité & Conformité

| Exigence | Implémentation |
|----------|----------------|
| HDS (Hébergeur Données de Santé) | Hébergement certifié, chiffrement AES-256 |
| RGPD | Consentement explicite, droit à l'oubli, DPO désigné |
| Authentification | MFA obligatoire pour les professionnels de santé |
| Traçabilité | Logs d'accès horodatés, conservation 10 ans |
| Disponibilité | Architecture redondante, RTO < 4h |

---

## Dataset

Exploitation d'un dataset de structures de santé françaises :
- **~1 306 entrées** sur les urgences et spécialités
- **132 colonnes** : localisation, spécialités disponibles, horaires, capacités
- Source : données publiques Santé Publique France / data.gouv.fr

---

## Branding

Noms finalistes explorés lors de la phase de conception :
`Viciné` · `Sanori` · `Oraya` · `Curia` → **Medical'ia** retenu

---

## Équipe & Rôles

| Rôle | Responsabilité |
|------|----------------|
| Architecture SI & Sécurité | Infrastructure, conformité HDS/RGPD, IAM |
| Développement IA | Moteur d'orientation, traitement du langage naturel |
| Data Engineering | Pipeline de données, dataset structures de santé |
| UX/UI | Interface patient, accessibilité, parcours utilisateur |
| Communication | Branding, réseaux sociaux, partenariats médicaux |

---

## Structure du repo

```
medalia-healthtech/
├── README.md
├── docs/
│   ├── cahier-des-charges.md   ← Spécifications fonctionnelles
│   ├── architecture-si.md      ← Architecture technique cible
│   └── conformite-hds-rgpd.md  ← Analyse de conformité
├── data/
│   └── dataset-structures-sante/  ← Exploration du dataset
├── design/
│   └── branding/               ← Charte graphique, logos
└── schemas/                    ← Diagrammes d'architecture
```

---

## Auteur
**Armand CHUIGWA** — ASRC RNCP39611 Niveau 6 — IMIE Paris 2025-2026
