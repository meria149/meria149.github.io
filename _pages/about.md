---
permalink: /
# title: "title"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Mon nom est Mériadec Finoude. Ce site est créé dans le cadre du cours [IFT4055 : Projet Informatique Honor](https://admission.umontreal.ca/cours-et-horaires/cours/IFT-4055/) du Département d'Informatique et de Recherche Opérationelle (DIRO) de l'Université de Montréal. Ce cours vise à initier l'étudiant à la recherche par le biais d'un projet défini et encadré par un professeur du département.

Titre du projet
======
Amélioration des Recommandations de Produits d'Épicerie : Exploration de l’influence du budget sur les produits

Description du projet
======
Ce projet de recherche vise à améliorer les recommandations de produits d'épicerie en adaptant et en combinant des algorithmes
de recommandation existants pour une meilleure performance. Le projet se basera sur des données pré-traitées provenant d'une grande
épicerie au Canada. Ces données contiennent des achats d’un grand nombre de clients ayant une carte de fidélité. Elles contiennent
aussi des informations riches comme le prix du produit, sa catégorie, etc. Notre hypothèse dans ce travail est que les achats
d’un client est influencé par son niveau budgétaire. Un client ayant un budget restreint va tenter d’acheter des produits moins
chers. Si cette hypothèse s’avère vraie (en vérifiant sur les données), il est alors possible de tenir compte du niveau de budget
du client pour recommander des produits adaptés. Le critère du budget sera ajouté à un algorithme de recommandation existant.
Le projet évaluera selon le succès de l’implémentation de ce critère dans un algorithme, ainsi que son impact sur la qualité de
la recommandation de produits d'épicerie.

Rôle de l'étudiant
======
Le rôle de l'étudiant dans ce projet de recherche englobe diverses responsabilités. Il analysera l'ensemble de données prétraitées
des courses d'épicerie, permettant de vérifier (ou non) l’hypothèse formulée. Il mettra en œuvre des algorithmes de recommandation
en intégrant le critère lié au niveau de budget. L'étudiant effectuera des tests et une évaluation rigoureuse de ces algorithmes,
en documentant sa progression et ses découvertes. 

Superviseur
======
Mon superviseur pour ce projet est le professeur [Jian-Yun Ni](http://rali.iro.umontreal.ca/nie/jian-yun-nie/). Mr. Nie est Professeur titulaire dans le laboratoire de recherche appliquée en linguistique informatique (RALI) de l'Université de Montréal.

Évolution du projet
======

- Semaine 0 ( 18 au 24 Septembre 2023)
------
Cette semaine, j'ai rencontré pour la première fois mon professeur. Ensemble, nous avons discuté de mon profil, de l'objectif du cours, et du projet de recherche sur lequel je pourrais travailler au cours de la session.

- Semaine 1 (25 septembre au 1er octobre 2023)
------
J'ai obtenu accès aux données et clarifié les étapes du projet avec mon superviseur.

- Semaine 3 - 9 (1er ocobre au 7 décembre 2023)
-------
Durant ces semaines, j'ai focusé beaucoup sur la première partie du projet, qui est l'analyse de la corrélation entre le budget et les achats des clients. Notre analyse a d'abord requis d'obtenir des informations additionnelles notamment le poids de chaque produit (pour calculer prix par unité des produit). En effet, il était impossible de comparer les achats des produits sans connaitre le poids de chaque produit (en grammes ou en mL) et pouvoir réellement voir si dans une même catégorie un produit est plus cher qu'un autre par unité.

Nous avons découvert cet [article](https://www.ers.usda.gov/webdocs/publications/40816/32372_aer759.pdf?v=36.2) super intéressant qui semble valider notre hypothèse initiale i.e. que les ménages avec des revenus faibles achètent en moyenne des produits moins chers par unité que l'ensemble des ménages.

Armé de cette hypothèse, nous avons utilisé deux définitions de budgets:
- somme des achats d'un usager durant le mois
- somme des achats d'un usager par panier (visite dans une journée dans le mois)

Une analyse des données avec ces deux définitions n'a pas permis de démontrer une corrélation entre le budget et le prix moyen par unité des produits achetés. En effet, il y a toujours certains produits où l'usager avec un budget faible selon notre définition se retrouve avec un prix moyen par unité plus élevé que l'usager moyen ou même plus élevé que le prix moyen par unité d'un usager avec un budget élevé. 

On dirait que nous ne disposons pas de suffisamment d'informations pour confirmer notre hypothèse avec les données dont nous disposons. En effet, un client peut juste venir prendre un faible nombre de produits (et donc un budget faible selon nos définitions), mais dépenser par unité plus qu'un usager qui vient prendre un nombre élevé de produits.

Nous envisageons de continuer notre analyse de données pour identifier si nous pouvons avoir un profil des clients qui dépensent le moins par unité pour chaque catégorie de produits. Achètent-il par exemple des produits moins bons pour la santé ? L'analyse pourrait alors servir pour d'autres études postérieures ou on regarderait par exemple si il est possoble de recommender à ces usagers des produits moins chers dans la même catégorie mais qui sont meilleurs pour la santé. 

Une fois que nous avons identifié le profil de ces clients, nous allons incorporer ces profils dans un modèle de recommendation existant afin de vérifier si il permet d'améliorer les métriques tels que le Recall et le NDGC.


