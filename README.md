Exercices pratiques libres sur le Module 3 Modèle linéaire : La
biométrie humaine
================

<!--- do not edit readme.md ---->

# Avant-propos

Cette séance d’exercices est en cours de développement. N’hésitez pas à
vérifier le lien suivant afin de voir si des modifications n’ont pas été
apportées dans les consignes :
<https://github.com/BioDataScience-Course/B03Gb_human>

## Contexte

Dans le cadre du cours de **science des données biologique I**, vous
avez été amené à collecter des données sur la biométrie humaine. Un an
plus tard, il vous est demandé de ré-analyser ces données à l’aide des
outils en lien avec le modèle linéaire.

Etant donnée que vous avez été des scientifiques consciencieux, vous
avez collecté vos données en y associant des métadonnées.

Les données ont été collectées via un document googlesheet dont l’url
est le suivant :

  - <https://docs.google.com/spreadsheets/d/1GJAGWjwNBtEGqQXqFcNxkrwcw-5n-gqwmiGAzxUZrxg/edit?usp=sharing>

Les métadonnées associées aux données ont été recensées dans un document
googledoc dont l’url est le suivant :

  - <https://docs.google.com/spreadsheets/d/1j55bB9YEAVbS4eRE-i6L-NEYhHXua-dxs-aQr_qko7k/edit?usp=sharing>

Les données sont téléchargeables au fomat csv via l’url suivant :

  - <https://docs.google.com/spreadsheets/d/e/2PACX-1vSfY7b0ICF64uv9vIYi8Jg38Rw3pKvLHC5TW0XOZYVQ4ce2dTmXGM5Cm8J922MsYm_fk75DKOK2wC4b/pub?output=csv>

# Objectif

Ce projet est un projet **individuel**, **court** et **libre** qui doit
être **terminé pour la fin du module 3**.

# Consignes

Sur base d’une question de recherche que vous choisissez.

## Script R

Dans un script R nommé `biometry.R` :

  - Importez vos données

<!-- end list -->

``` r
biometry <- readr::read_csv("https://docs.google.com/spreadsheets/d/1UfpZvx1_nd7d10vIMAfGVZ1vWyIuzeiKxPL0jfkNSQM/export?format=csv", locale = readr::locale(decimal_mark = ","))
```

  - Ajoutez les labels à vos variables. (vous pouvez utiliser par
    exemple la fonction `labelise()`).

  - Réalisez une sauvegarde locale de votre jeu de données (vous pouvez
    apr exemple employer la fonction `write()`)

## human\_notes

Dans le fichier `human_notes.Rmd`, réalisez au moins 3 modèles linéaires
en lien avec votre thématique. Réalisez des analyses complètes
(N’oubliez donc pas l’analyse des résidus)

## human\_report

Ce fichier est un template au format R Markdown, un peu plus élaboré. Il
est facilement possible de faire des citations des auteurs, des tableaux
et des graphiques dans le texte.

Dans le template Rmd :

  - Sélectionnez votre modèle linéaire le plus adéquat et consignez cle
    dans un document structuré au format R Markdorwn. Utilisez le
    template (`human_report.Rmd`) mis à votre disposition dans le
    dossier `docs`. Ce document doit contenir :
    
      - une courte introduction sur la question de recherche que vous
        vous posez.
      - une section analyse avec la description des données et la
        réalisation du modèle linéaire. Chaque tableau et graphique
        doit avoir une légende claire et précise comme montré dans
        l’exemple. Tout comme dans les revues scientifiques, les
        tableaux et graphiques doivent être cité dans le texte.
      - une section discussion et conclusion
