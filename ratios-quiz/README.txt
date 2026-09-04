FICHIER RATIOS — quizz infini de révision
==========================================

Le site fonctionne maintenant en local sur ordinateur ET hors-ligne
sur téléphone (métro, salle d'attente, etc. — sans wifi ni réseau).
C'est devenu une "PWA" (Progressive Web App) : une fois ajoutée à
l'écran d'accueil, elle se comporte comme une vraie appli, sans
navigateur visible, et fonctionne même sans connexion.

--------------------------------------------------------------------
SUR ORDINATEUR (comme avant)
--------------------------------------------------------------------
Double-clique sur index.html, ou lance un mini-serveur local :
  python3 -m http.server 8000
puis va sur http://localhost:8000

--------------------------------------------------------------------
SUR TÉLÉPHONE, POUR UN USAGE HORS-LIGNE (métro, admin, etc.)
--------------------------------------------------------------------
Un fichier local ouvert depuis l'app Fichiers ne s'exécute pas
correctement sur iPhone (Safari ne l'ouvre pas comme une vraie page).
La solution : mettre le site en ligne une seule fois (gratuitement,
sans compte), puis l'installer sur ton téléphone — il fonctionnera
ensuite indéfiniment sans connexion.

1) Sur ton ordinateur, ouvre https://app.netlify.com/drop dans un
   navigateur.

2) Fais glisser le DOSSIER complet (celui qui contient index.html,
   manifest.json, service-worker.js, fonts/, icons/) dans la zone de
   dépôt. Aucune inscription n'est nécessaire.

3) Netlify te donne un lien du type https://un-nom-aleatoire.netlify.app
   — ouvre ce lien une fois sur ton téléphone, en Safari, connecté au
   wifi ou aux données mobiles (juste pour cette première ouverture).

4) Dans Safari, appuie sur l'icône de partage (le carré avec la
   flèche vers le haut), puis "Sur l'écran d'accueil". Un icône
   "Ratios" apparaît sur ton téléphone, comme une vraie appli.

5) Ouvre l'appli une fois depuis cet icône (toujours avec du réseau),
   pour laisser le temps au site de tout mettre en cache.

À partir de là, tu peux couper le wifi et les données mobiles :
l'appli s'ouvre et fonctionne entièrement hors-ligne, y compris ta
progression (elle est sauvegardée sur le téléphone).

Remarque : le lien Netlify "non réclamé" peut expirer après un
moment si tu ne crées pas de compte. Ce n'est pas grave : une fois
l'appli ajoutée à l'écran d'accueil et ouverte au moins une fois,
tout est mis en cache sur ton téléphone et continue de fonctionner
même si le lien d'origine disparaît. Si tu veux garder la main pour
la mettre à jour plus tard (ajouter des ratios, etc.), tu peux créer
un compte Netlify gratuit et "réclamer" le site.

--------------------------------------------------------------------
FONCTIONNEMENT DU QUIZZ
--------------------------------------------------------------------
- Chaque question porte sur un ratio et prend une forme parmi trois,
  tirée au hasard : donner sa formule, donner son utilité principale,
  ou retrouver son nom à partir de sa formule.
- 4 réponses sont proposées (une bonne, trois fausses piochées parmi
  les autres ratios, en priorité dans la même catégorie). Clique une
  réponse (ou touches 1-4 au clavier) pour valider.
- La bonne réponse s'affiche en vert. Si tu réponds juste, tu vois un
  résumé concis (formule + définition + utilité). Si tu te trompes,
  une fiche complète "mini-cours — à apprendre" apparaît à la place :
  définition (avec la signification de l'acronyme le cas échéant),
  formule, utilité, un point "à retenir" (piège classique ou
  comparaison avec un ratio proche), et un exemple chiffré — de quoi
  vraiment apprendre le ratio plutôt que juste voir la bonne réponse.
  Puis "suivant →" (ou Entrée/Espace) pour continuer. Le quizz ne
  s'arrête jamais.
- Le tirage des questions est pondéré : les ratios sur lesquels tu te
  trompes reviennent plus souvent, ceux que tu maîtrises s'espacent.
- Le bandeau à gauche (ou en haut sur mobile) filtre par catégorie :
  Rentabilité, Liquidité, Solvabilité, Activité/BFR, Valorisation, DCF.
- Ta progression (poids de chaque ratio + compteurs) est sauvegardée
  sur l'appareil (localStorage), donc elle persiste d'une session à
  l'autre.
- Interface optimisée mobile : catégories en bandeau scrollable,
  réponses empilées en une colonne, zones cliquables agrandies.

Pour ajouter tes propres ratios ou questions, ouvre index.html avec un
éditeur de texte et complète le tableau RATIOS en haut du <script>.
