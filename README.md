# Dashboard Covid 
# Tableau de bord sur la Covid
Ouvrir Ubuntu
Créer un dossier mkdir covid
Ouvrir le dossier: covid
Ouvrir VS Code avec la commande "code ."

Créer 1 fichier:
 - fichier docker-compose.yml : Créer les containers et fait les liens entre les containers Docker, Mysql, Grafana ainsi que notre Base de données 
Importer 1 fichier :
- vaccination.sql : il s'agit de notre base de données
 

Voici les 2 graphiques avec leur requêtes:

 SELECT DISTINCT country, MAX(daily_vaccinations) AS daily_vaccinations
            FROM covid_sql
            GROUP BY country
            ORDER BY daily_vaccinations DESC
            LIMIT 10



 SELECT DISTINCT country, MAX(people_fully_vaccinated) AS people_fully_vaccinated
            FROM covid_sql
            GROUP BY country
            ORDER BY people_fully_vaccinated DESC
            LIMIT 10 ;
   
 <img width="452" alt="graph" src="https://user-images.githubusercontent.com/95342914/161985758-62067490-0d19-4471-b4fb-1b02a81b4702.PNG">




SELECT DISTINCT country, MAX(people_fully_vaccinated) AS people_fully_vaccinated
            FROM covid_sql
            GROUP BY country
            ORDER BY people_fully_vaccinated DESC
            LIMIT 10 ;

<img width="766" alt="graph 2" src="https://user-images.githubusercontent.com/95342914/161985744-b93947c5-ec18-4402-a971-f4f4993f23de.PNG">
