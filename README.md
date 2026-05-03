# Détection et prédiction d'anomalies dans le domaine industriel
Projet final du cours *STT 3795 Fondements théoriques en science des données*  

## Contexte
Dans le domaine manufacturier de haute précision, une pièce non conforme 
entraîne des retards critiques dans la chaîne d'approvisionnement et peut 
avoir des conséquences graves sur la sécurité. Ce projet propose un pipeline 
séquentiel pour anticiper les défaillances machines à partir de données de 
capteurs de production.

## Objectif principal
Quantifier l'impact du débruitage spatial (DBSCAN) sur les performances 
prédictives d'un classificateur SVM, dans un contexte de données industrielles 
avec un fort déséquilibre de classes (environ 3.4% de défaillances).


## Données
**AI4I 2020 Predictive Maintenance Dataset** — UCI Machine Learning Repository  
- 10 000 observations, 6 variables explicatives  
- Variable cible : "Machine failure" (binaire, 0 : bon, 1 : mauvais)  
- Défi : fort déséquilibre de classes (environ 3.39% de défaillances)


## Résultats

| Métrique | SVM Brut | SVM Propre |
|----------|----------|------------|
| F1-score | 0.5465   | 0.5000     |
| AUC-ROC  | 0.9304   | 0.9298     |

Le débruitage par DBSCAN n'a pas amélioré les performances du SVM. 
Les défaillances, dispersées en périphérie du nuage dense, sont 
géométriquement similaires au bruit spatial.
DBSCAN ne fait pas de différence entre les deux.

## Technologies
- Python 3.11
- scikit-learn, pandas, numpy, matplotlib, seaborn


## Auteurs

Yves Sery
