# Analyse financière sur la toile

## Contexte du projet

L'objectif du projet est de récupérer des données financières sur internet afin de pouvoir les exploiter et réaliser un DashBoard.
Les données seront stockées en base, avant de réaliser de la dataviz.

Pour effectuer le scrapping, notre choix s'est porté sur BeautifulSoup.
Le jeu de données provient du site de la banque en ligne Boursorama, où nous avons récupérer les indices boursiers pour le mois de mars 2021.

[jeu de données](https://github.com/celine29730/Analyse-financi-re-sur-la-toile/blob/main/Jeudonn%C3%A9es.png)

Notre jeu de données comporte le dernier cours du jour, la variation du cours de l'indice, le cours à l'ouverture, le cours le plus haut et le plus bas sur la journée , le volume, le nom de l'indice et la date.

Le jeu de données est transformé en fichier csv et importé sous PHP my admin afin d'être mis en base (création d'une table cours). On crée alors un fichier cours.sql. 
Ce fichier est ensuite copié dans un container MYsql. Le container MYsql ainsi que le container de Grafana pour la visualisation des données sont créés, à l'aide dun fichier docker-compose.yml.

Une fois la table cours.sql intégrée dans le container, il est possible via grafana de se connecter à la base de données et plus particulièremet à la table cours, afin de visualiser les donées.

Nous obtenons le Dashboard suivant réalisé sur Grafana:





