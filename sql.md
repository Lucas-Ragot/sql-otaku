# Requete SQL du challenge

## la moyenne d'age des viewers, classée par pays

```SQL
  SELECT viewer_country, ROUND(AVG(viewer_age_group)) as average_age FROM viewing GROUP BY viewer_country;
```

## le nombre d'épisodes regardés, classé par tranche d'âge, et rangé par tranche d'age décroissant

```SQL
  SELECT viewer_age_group AS age, COUNT(*) AS episode FROM viewing GROUP BY viewer_age_group ORDER BY viewer_age_group DESC;
```

## BONUS CACTUS (attention, ça parait simple mais ça pique !) : le nombre de visionnage par an

```SQL
  SELECT extract(YEAR from viewing_date) AS year, COUNT(*) AS view FROM viewing GROUP BY year ORDER BY year;
```
