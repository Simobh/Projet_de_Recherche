# Comparaison des Algorithmes d'Optimisation sur la Suite BBOB (COCO)

Ce projet vise à comparer les performances de trois algorithmes d’optimisation sans dérivée — **BFGS**, **GLOBAL**, et **RANDOMSEARCH-5** — sur plusieurs fonctions tests de la suite **BBOB** (Black-Box Optimization Benchmarking), en utilisant les données brutes générées par la plateforme **COCO**.

## Objectifs

- Évaluer le comportement des algorithmes selon la nature des problèmes.
- Mesurer la déviation à l’optimum sur différents runs.
- Comparer les résultats par **fonction**, **dimension** et **algorithme**.
- Visualiser la convergence et la robustesse des approches.

## Méthodologie

Les fonctions tests utilisées sont :
- `f1` (Sphere), `f6` (Attractive Sector), `f10` (Ellipsoidal), `f15` (Rosenbrock), `f20` (Schaffer F7)

Les dimensions testées sont :
- **2** et **10**

Pour chaque combinaison **algorithme – fonction – dimension**, nous avons :
1. Analysé **un seul run**
2. Agrégé **tous les runs**
3. Calculé les **moyennes**, **écarts-types**, et **bornes min/max**
4. Comparé les performances dans la section "Comparaison des algorithmes"

## Structure du dépôt

La structure du projet a été conçue de manière claire et hiérarchisée. À la racine du dossier **projet_recherche**, trois sous-dossiers principaux correspondent aux algorithmes étudiés : **BFGS/**, **GLOBAL/** et **RANDOMSEARCH-5/**. Chacun de ces répertoires contient un sous-dossier **data/** qui regroupe les fichiers de données brutes (.tdat) extraits de la plateforme COCO, spécifiques à l’algorithme concerné. Les fichiers notebooks Jupyter (.ipynb) y sont nommés selon la convention **algo_fonction_dimension** et permettent d’analyser les performances de chaque algorithme sur chaque combinaison fonction/dimension.

En parallèle, un dossier **comparaison_des_algorithmes_COCO/** regroupe les notebooks dédiés à la comparaison directe des trois algorithmes sur chaque problème. Chaque notebook dans ce dossier (ex. `f1_dim2.ipynb`) intègre les résultats de tous les algorithmes pour une fonction et une dimension donnée, permettant une analyse transversale et comparative.


## Reproduction des résultats

1. Exécuter les notebooks dans chaque dossier `BFGS/`, `GLOBAL/`, `RANDOMSEARCH-5/` pour générer :
   - les courbes d’un seul run
   - les courbes de tous les runs
   - les courbes agrégées (moyenne, écart-type, min/max)

2. Comparer les résultats avec les notebooks du dossier :
   ```
   comparaison_des_algorithmes_COCO/
   ```

## Technologies utilisées

- **Python**
- **Google Collab**
- **Matplotlib / Pandas**
- **COCO platform (Benchmark suite)**

## Auteurs

- **SAADI Rayane**
- **JALDI Oussama**
- **BAHLOUL Mohammed**

Projet réalisé dans le cadre du module initiation à la recherche – Ecole d'ingenieurs du Littoral Cote d'Opale - Année universitaire 2024–2025
