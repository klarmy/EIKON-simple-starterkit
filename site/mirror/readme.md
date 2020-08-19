


# mirror/

Contient le site à proprement parler. Les dossiers et fichiers présents à ce degré d'arborescence sont essentiellement issus de HTML5 Boilerplate, excepté le dossier /scss.

## /css

Ce dossier comporte les feuilles de style en exploitation sur le site.
Dans le cas d'un projet basé sur SCSS, il convient qu'il soit **initialement vide** afin que le compilateur y crée les fichiers.

## /fonts

Ce dossier rassemble les fontes web du projet, au format WOFF et WOFF2.

## /img

Ce dossier comporte les images et ressources graphiques.
Afin de les distinguer, préfixes et suffixes renseigneront sur l'image :
   * préfixe- : caractérise le type d'image (icone, photo, background, etc)
   * nom- : identifie explicitement l'image
   * suffixe1 : caractérise le type de device auquel cette image se destine
   * suffixe2 : caractérise la résolution (@1x, @2x)
   * extension

P.ex. : icon-user_profil-desktop@2x.png

## /js

Ce dossier contient les scripts et frameworks utiles dans le langage JavaScript.
   * /vendor : rassemble les scripts tierce-partie (modernizer)
   * plugins.js : collecte les plugins, afin de limiter les requêtes http
   * main.js : scripts du site à proprement parler

## /scss

Ce dossier rassemble toutes les ressources destinées à produire le ou les fichiers css, grâce à un compilateur SCSS.

## icônes

Les fichiers suivants sont destinés à produire des représentations iconiques du site sur iOS et Windows 9+. A conserver dans leurs dimensions initiales.
   * icon.png
   * favicon.ico (ou favicon.png)
   * tile-wide.png
   * tile.png

Le fichier browserconfig.xml associe les fichiers correspondants à Internet Explorer et à Edge.

## .htaccess

Ce fichier configure le service Apache pour ce projet.

## humans.txt

Ce fichier recense les acteurs, collaborateurs, outils, ressources et autres composantes du projet.
Utile si l'on ne peut pas signer une réalisation web.

## robots.txt

Ce fichier est un protocole d'exclusion des robots, à savoir les web crawlers liés aux moteurs de recherche, proposant une politique de référencement des ressource du site.
Une documentation complète est présente sur http://robots-txt.com.

---

## Autres dossiers possibles

```
+-- assets/ contient les vidéos et l'audio  
|  +-- video/  
|  +-- audio/  
+-- **press/ pour le matériel destiné à la presse et à la communication  
+-- **fr/ si le site propose son contenu en plus d'une langue, dans ce cas ajouter les dossiers correspondants aux autres langues  
+-- ...
```