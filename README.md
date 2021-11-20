Modèles linéaires (généralisés) appliuqués à la biométrie humaine
================

<!--- do not edit readme.md ---->

## Avant-propos

Cette séance d’exercices est suceptible d’être adaptée. N’hésitez pas à
vérifier le lien suivant afin de voir si des modifications n’ont pas été
apportées dans les consignes :
<https://github.com/BioDataScience-Course/B03Gb_human>

## Contexte

Dans le cadre du cours de **science des données biologique I**, vous
avez été amené à collecter des données sur la biométrie humaine. Un an
plus tard, il vous est demandé de ré-analyser ces données à l’aide de
modèle(s) linéaires(s) (généralisés).

Étant donné que vous avez été des scientifiques consciencieux, vous avez
collecté vos données en y associant des métadonnées.

Les données ont été collectées via un document GoogleSheet à l’adresse
suivante :
<https://docs.google.com/spreadsheets/d/1GJAGWjwNBtEGqQXqFcNxkrwcw-5n-gqwmiGAzxUZrxg/edit?usp=sharing>

Les métadonnées associées aux données ont été recensées dans un document
GoogleDoc :
<https://docs.google.com/spreadsheets/d/1j55bB9YEAVbS4eRE-i6L-NEYhHXua-dxs-aQr_qko7k/edit?usp=sharing>

Les données sont téléchargeables au fomat CSV via :
<https://docs.google.com/spreadsheets/d/e/2PACX-1vSfY7b0ICF64uv9vIYi8Jg38Rw3pKvLHC5TW0XOZYVQ4ce2dTmXGM5Cm8J922MsYm_fk75DKOK2wC4b/pub?output=csv>

## Consignes

Ce projet est un projet à réaliser par **binôme** et **libre**. Il doit
être **terminé pour la fin du module 3**. Sur base d’une question de
recherche que vous choisissez, effectuez des analyses qui nécessitent
des modèles linéaires (généralisés) pour y répondre.

### Script R

Dans un script R nommé `biometry.R` :

-   Importez vos données

``` r
biometry <- readr::read_csv("https://docs.google.com/spreadsheets/d/e/2PACX-1vSfY7b0ICF64uv9vIYi8Jg38Rw3pKvLHC5TW0XOZYVQ4ce2dTmXGM5Cm8J922MsYm_fk75DKOK2wC4b/pub?output=csv", locale = readr::locale(decimal_mark = ","))
```

-   Ajoutez les labels à vos variables. (vous pouvez utiliser par
    exemple la fonction `labelise()`).

-   Réalisez une sauvegarde locale de votre jeu de données (vous pouvez
    par exemple employer la fonction `write$rds()`)

### human_notes

Dans le fichier `human_notes.Rmd` dans `docs`, réalisez au moins trois
modèles linéaires (généralisés) en lien avec votre thématique. Réalisez
des analyses complètes (n’oubliez donc pas l’analyse des résidus).

### human_report

Ce fichier est un template au format R Markdown, un peu plus élaboré.
Vous pouvez y réaliser des citations de références bibliographiques, de
tableaux et de figure comme vous avez appris à la faire dans le
précédent projet. Sélectionnez votre modèle linéaire le plus adéquat et
consignez-le dans un document structuré au format R Markdown. Utilisez
le template (`human_report.Rmd`) mis à votre disposition dans le dossier
`docs`. Ce document doit contenir :

-   une courte introduction sur la question de recherche que vous vous
    posez.
-   une section analyse avec la description des données et la
    réalisation du modèle linéaire. Chaque tableau et graphique doit
    avoir une légende claire et précise comme montré dans l’exemple.
    Tout comme dans les revues scientifiques, les tableaux et graphiques
    doivent être cité dans le texte.
-   une section discussion et conclusions
