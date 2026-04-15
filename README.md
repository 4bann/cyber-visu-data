# Cyber Threat Dashboard - Data Visualization

> Projet de visualisation de données réalisé dans le cadre du cours **DataViz** à l'ESILV (2025-2026).

![D3.js](https://img.shields.io/badge/D3.js-v7-orange)
![License](https://img.shields.io/badge/License-MIT-blue)

## Description

Ce projet analyse des **incidents de cybersécurité santé** publiés par le **HHS OCR Breach Portal** à travers deux visualisations interactives développées avec D3.js. L'objectif est d'explorer la répartition géographique des incidents, les volumes d'impact et les flux entre types de brèches et niveaux de gravité.

## Visualisations

### 1. Carte choroplèthe - Incidents par État
Une carte interactive des États-Unis permettant de visualiser :
- **Le nombre d'incidents signalés** par État
- **Le volume d'individus affectés** par État
- **La part d'incidents critiques** par État

### 2. Diagramme Sankey - Types de brèche vers impact
Un diagramme de flux montrant la relation entre :
- Le **type de brèche** déclaré au HHS OCR
- Le **niveau d'impact** calculé à partir des individus affectés

## Technologies utilisées

- **D3.js v7** - Bibliothèque de visualisation
- **TopoJSON** - Données géographiques USA
- **d3-sankey** - Plugin pour diagramme Sankey
- **HTML5 / CSS3** - Structure et style

## Structure du projet

```text
dataviz/
├── index.html              # Dashboard principal
├── map-cyber.html          # Carte choroplèthe cyber
├── sankey-cyber.html       # Sankey cyber
├── data/
│   ├── cyber-incidents.csv # Incidents cyber bruts
│   └── cyber-state-kpis.csv# KPI cyber par État
└── README.md               # Documentation
```

## Données

La source utilisée est le **HHS OCR Breach Portal** :

- Portail : https://ocrportal.hhs.gov/ocr/breach/breach_report_hip.jsf
- Vue retenue : **Under Investigation**

### Fichiers de données du projet

| Fichier | Description |
|---------|-------------|
| `cyber-incidents.csv` | Incidents HHS OCR avec État, entité, type de brèche, individus affectés, etc. |
| `cyber-state-kpis.csv` | Agrégats par État : nombre d'incidents, individus affectés, part critique, type dominant |

### Variables principales

- `State` : abréviation de l'État
- `Covered Entity` : entité déclarant la brèche
- `Covered Entity Type` : type d'organisation santé
- `Individuals Affected` : nombre d'individus affectés
- `Type of Breach` : catégorie officielle de l'incident
- `Location of Breached Information` : support ou système compromis

## Installation locale

1. Lancer un serveur local :

```bash
python -m http.server 8000
```

2. Ouvrir dans le navigateur :

```text
http://localhost:8000
```

## Indicateurs présents dans cette version

- **695 incidents** analysés
- **48 États** couverts
- **295 202 684 individus affectés** cumulés
- **Hacking / IT Incident** comme type de brèche dominant

## Auteurs

| Nom | Rôle |
|-----|------|
| **Alban GUERET** | Développement & Visualisations |
| **Roméo CARECCHIO** | Développement & Visualisations |
| **Thushsan Rathnayaka** | Développement & Visualisations |

---

Projet réalisé dans le cadre du cours DataViz - ESILV 2025-2026
