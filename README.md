# Plan de Feu

Application web pour électricien plateau (technicien lumière / gaffer) :
préparer une implantation lumière — importer un patch DMX, placer les
projecteurs et des caméras sur un plan de scène ou de salle.

## Usage

- Ouvrir `index.html` dans Safari (idéalement via l'URL GitHub Pages une
  fois publiée), puis "Sur l'écran d'accueil" pour l'installer comme une
  app iPad.
- Fonctionne **100% hors-ligne** après le premier chargement : pas de
  compte, pas de synchronisation, tout reste dans le navigateur.

## Fonctionnalités

- Import CSV du patch, avec correspondance manuelle des colonnes
  (adresse / nom / type), mémorisée d'une session à l'autre
- Import d'une image de fond (plan de salle)
- Placement des projecteurs (liés à une entrée du patch) et des caméras
  par tap sur le plan, déplacement au doigt, rotation via une poignée
  dédiée
- Zoom et déplacement (pan) du plan
- Sauvegarde automatique locale, export/import du projet en `.json`
  (fond d'image inclus)
- Recherche/filtre dans la liste du patch

## Développement

Fichier unique `index.html`, JavaScript natif (vanilla), sans framework
ni dépendance externe (CDN, fonts, libs) — tout le CSS/JS est inline
dans ce fichier. C'est volontaire : une seule ressource à mettre en
cache pour que l'app reste utilisable hors-ligne, sans risque de rupture
si un CDN est injoignable.

## Déploiement

Le repo est publié via **GitHub Pages** directement depuis la branche
`main` (racine du repo). Toute modification poussée sur `main` met à
jour l'app en ligne.
