# /scss

Les fichiers SCSS sont regroupés dans ce dossier, selon une organisation dite **SMACSS**.  
Tout fichier .scss est compilé avec ses dépendances (@import), pour ne générer, in fine, qu'un seul fichier CSS.

Aucune nouvelle connaissance CSS n'est requise, seules sont touchées l'approche syntaxique et la logique de codage.

Un fichier scss est compilé en son équivalent css.

Un partial, **préfixé "_"**, est intégré à un fichier qui y recourt (@import, par exemple main.scss). Il n'est pas compilé en son équivalent css.

L'ordre d'appel des fichiers est décisif. P.ex. les variables et mixins doivent être déclarés en amont de leur emploi.

Pour aller plus loin, se référer à la documentation SMACSS https://smacss.com, qui fait référence en la matière.  
Tester les syntaxes SCSS (compilées à la volée) sur http://www.sassmeister.com et http://codepen.io.

## main.scss

Ce fichier est l'élément fondateur, qui génèrera la feuille de style correspondante (css/main.css). Peut aussi s'appeler styles.css, screen.css, etc

## _base.scss

Ce partial contient la redéfinition des éléments HTML et des sélecteurs de base.

## _layout.scss

Ce partial regroupe les déclarations propres aux segments du site (.l-header, .l-main, .l-footer…), **préfixés .l-**.

Le champ d'action de layout est limité à définir le comportement des régions de contenu et les règles de composition générales.  
Lire http://www.nicoespeon.com/fr/2013/05/tombez-pour-smacss/ pour plus de détail sur le sujet.

## _module.scss

Ce partial regroupe les modules intégrés aux régions du layout, **préfixés .[nomdumodule]-** (p.ex. : .newsletter, .newsletter-header, .newsletter-form).  
Tous les modules peuvent être définis dans ce partial, ou, pour plus de lisibilité et de modularité, faire l'objet de partials spécifiques groupés dans /module.

Les modules sont réutilisables. Pensez à leur attribuer des **noms logiques**, et à les spécialiser selon leur contexte.
[//]: # (Lire http://maintainablecss.com pour aller plus loin.)

## _shame.scss

Dans la pratique, certains bouts de code ne sont pas immédiatement classables. Ils trouveront leur place **temporaire** dans ce partial.

## _state.scss

Ce partial (non créé et facultatif) regroupe les états des objets du site, **préfixés .is- ou .has-**.

Ces classes sont particulièrement utiles pour décrire les états des objets du site, et y accéder par le biais de JavaScript.

## _theme.scss

Ce partial (non créé et facultatif) regroupe les déclarations liées à l'apparence des éléments du site (fontes, couleurs, arrière-plans).

Délicat à exploiter, car il requiert un degré élevé d'abstraction du code.

## _variables.scss

Ce partial contient les variables SCSS du site, permettant d'unifier les couleurs, fonts, tailles et autres valeurs répétitives.

Attention à ne pas confondre variable SCSS https://sass-lang.com/documentation/variables et variable CSS https://developer.mozilla.org/fr/docs/Web/CSS/Using_CSS_custom_properties

## print.scss

Ce fichier regroupe les styles propres à l'impression.  
Proposés par HTML5 Boilerplate, ils peuvent être intégralement remaniés pour satisfaire des besoins spécifiques d'impression.

## /tools

Ce dossier contient :
   
   * _helper-classes.scss : les classes fournies par HTML5 Boilerplate utiles pour le layout (hidden, screen reader, invisible, clearfix) ;
   * les mixins personnalisés (à ajouter par vos soins)

## /vendor

Ce dossier contient les feuilles de style et scripts tiers (_normalize.scss, _sanitize.scss) ajoutés au site.

Idéal pour y stocker les _gridding systems_ et autres _frameworks CSS_.