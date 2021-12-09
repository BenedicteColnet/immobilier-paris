# Évolution des prix de l'immobilier à Paris 

**Analyse *rapide* du marché immobilier parisien à partir de la base de données DVF.**

## Késako

Le code ici présent utilise les données de DVF (Demandes de Valeur Foncière) -- qui recense les mutations à titre onéreux advenues les 5 dernières années -- pour visualiser l'évolution des prix de l'immobilier. 

L'analyse proposée se concentre sur la ville de Paris, mais le principe est le même pour d'autres villes.

En effet si l'[application]([https://app.dvf.etalab.gouv.fr](https://app.dvf.etalab.gouv.fr/) ) de visualisation proposée par etalab prend appui sur ces données et propose de visualiser les transactions à la maille de la parcelle cadastrale, cette dernière ne permet pas d'obtenir une vision aggrégée de l'évolution des prix, du nombre de vente, etc.

Les données rassemblée ici sont celles de Paris intramuros, depuis 2016 jusqu'au premier semestre 2021 inclus. Le code est rédigé en `R` avec une première partie de nettoyage des données, puis de visualisation.

Ces données forment une ressource intéressante pour quiconque s'intéresse au marché immobilier, mais aussi pour permettre des applications en cours de statistique / machine learning / économie. N'hésitez pas à compléter les analyses ou reprendre cela pour votre propre compte.

Pour information les fichiers présents dans le dossier `data` sont en date de novembre 2021.

## Disclaimers

J'attire en particulier l'attention de tout lecteur ou utilisateur sur le fait que:
- La présence de nombreux lots rend l'analyse de la surface en mètres carrés compliquée, car la nature des lots n'est pas précisée (garage, cave, pièce attenante ?)
- Aussi, la présence de la surface des biens en loi carrez n'est pas toujours disponible, *les prix sont donc probablement sur-estimés dans les graphiques présentés*.
- De nombreuses valeurs extrèmes sont présentes, que ce soit des prix très élevés, ou bien très bas (en dessous de 1000 euros le mètre carré, ce qui dans Paris intramuros est étrange). N'ayant pas d'information sur l'origine de prix si bas, ces valeurs extrêmes sont filtrées dans l'analyse. 

## Contexte des données

Pour donner un peu plus de contexte, la mise en ligne de ces données fait suite à l'application de l’article 13 de la loi n° 2018-727 du 10 août 2018 pour un État au service d’une société de confiance (ESSOC) et du décret n°2018-1350 du 28 décembre 2018 relatif à la publication sous forme électronique des informations portant sur les valeurs foncières déclarées à l’occasion des mutations immobilières. Ainsi la Direction générale des Finances publiques (DGFiP) a rendu librement accessibles au public, sur le site [data.gouv.fr](http://data.gouv.fr/), les éléments d’information qu’elle détient au sujet des valeurs foncières déclarées à l’occasion des mutations à titre onéreux intervenues au cours des cinq dernières années.

Ainsi, merci à etalab pour la mise en ligne de ces données !

Informations complémentaires:

- [etalab](https://www.etalab.gouv.fr/)
- [DVF](https://cadastre.data.gouv.fr/dvf)

## Commentaire de l'auteure

Comme précisé, ceci est une analyse rapide, faite par curiosité. Je suis preneuse de tout retour, notamment de la part de personnes averties sur la nature de cette base de données.
