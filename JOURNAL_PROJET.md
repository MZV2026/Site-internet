# Journal de bord — VAUBAN Espace Technologie

**Dépôt :** MZV2026/Site-internet  
**Portail :** https://mzv2026.github.io/Site-internet/  
**Branche de travail :** `feature/vaublocks-catalogue-integration`

Ce journal suit l'ensemble du site : portail, Systèmes intelligents et connectés, VAUBLOCKS, Mes activités, Robotique et projets, Maquette Designer et Tutoriels.

## 28 novembre 2026 — Mise en place du suivi global

- Lecture de la page d'accueil actuelle du dépôt.
- Constat : l'accueil présente déjà les rubriques, mais VAUBLOCKS, Mes activités, Robotique et projets et Maquette Designer sont encore indiqués comme à venir ou non raccordés.
- Création d'une branche de développement séparée : `feature/vaublocks-catalogue-integration`.
- Décision de tenir un suivi global du site, et non un suivi limité à VAUBLOCKS.
- Création de `suivi-projet.html` comme tableau de bord de l'avancement.
- Les pages et contenus internes des autres rubriques restent à auditer : leur état détaillé n'est pas encore établi.

## État initial des chantiers

- **Portail d'accueil :** prototype existant ; raccordements, contrôles et finitions à réaliser.
- **Systèmes intelligents et connectés :** contenu à inventorier et auditer.
- **VAUBLOCKS :** prototype et cahier des charges existants ; conception des composants et blocs avancée ; catalogue exact, fiches JSON, configurateur, génération de code et tests à poursuivre.
- **Mes activités :** organisation et contenu à définir.
- **Robotique et projets :** projets et ressources à inventorier puis organiser.
- **Maquette Designer :** projet prévu, conception et développement à réaliser.
- **Tutoriels :** ressources à inventorier, classer et publier.

## Règles de mise à jour

1. Ajouter une entrée datée à chaque séance de travail significative.
2. Noter les fichiers créés ou modifiés et les décisions prises.
3. Ne passer une tâche à « terminée » qu'après vérification.
4. Distinguer les éléments documentés, déduits et testés sur le matériel.
5. Actualiser en même temps le tableau de bord HTML et ce journal.


## 28 novembre 2026 — Identité visuelle et première prise en main de VAUBLOCKS

- L'enseignant a testé la page publiée VAUBLOCKS : les blocs sont déplaçables et paramétrables.
- Demande de réintégrer le logo VAUBLOCKS défini dans les travaux précédents et d'utiliser le bleu caractéristique de Grove pour les blocs correspondants.
- Ajout d'un logo vectoriel dans l'en-tête de VAUBLOCKS et application d'une couleur bleue dédiée aux catégories « Capteurs Grove » et « DEL Grove », ainsi qu'aux blocs du capteur et de la DEL.
- PR #5 fusionnée dans `main` : https://github.com/MZV2026/Site-internet/pull/5
- Fichiers modifiés : `vaublocks/index.html`, ajout de `vaublocks/vaublocks-logo.svg`.
- État : modification intégrée dans GitHub. La disponibilité de la version publiée après déploiement Pages reste à vérifier dans le navigateur.
- Limites inchangées : prototype restreint au capteur de luminosité et à la DEL Grove ; génération du code encore à tester/corriger ; aucune simulation ni téléversement physique.


## 28 novembre 2026 — Restauration du logo et clarification du parcours VAUBLOCKS

- L'enseignant a retrouvé et transmis le logo original VauBlocks en PNG.
- Création de la branche `feature/vaublocks-logo-parcours` à partir de `main` (commit de départ `425c15f`).
- Intégration proposée du PNG original dans l'en-tête, en remplacement du SVG simplifié ; adaptation responsive prévue.
- Réorganisation de l'interface dans l'ordre pédagogique validé : 1) affectation des entrées/sorties, 2) programmation Blockly, 3) test sur la carte.
- Ajout de repères visuels pour les deux modes décidés : LIVE (direct USB) et UPLOAD (compilation/téléversement). Les commandes restent désactivées car les fonctions ne sont pas développées.
- Correction d'un défaut identifié dans le générateur : le contenu du bloc « Au démarrage de la carte » était calculé mais non inséré dans la fonction `setup()`.
- Décision d'étudier Web Serial et un firmware de communication pour le mode LIVE ; aucune installation logicielle obligatoire n'est retenue à ce stade pour les navigateurs compatibles.
- Aucun test réel sur carte n'a été effectué dans cette étape. Le mode direct, la compilation et le téléversement restent à développer et valider.


## 28 novembre 2026 — Ajustements visuels VAUBLOCKS

- Réduction de 15 % de la largeur maximale du logo dans l'en-tête (560 px à 476 px) et de sa hauteur maximale (190 px à 162 px), sans modifier ses proportions.
- Correction de l'alignement des champs d'affectation : les deux colonnes utilisent la même grille, les libellés disposent d'une hauteur homogène et les sélecteurs sont alignés.
- Fichier modifié : `vaublocks/index.html`.
- Tableau de bord actualisé : `suivi-projet.html`.
- Modifications proposées dans la branche `fix/vaublocks-logo-port-alignment` et une PR dédiée ; aucun changement sur `main`.
- Vérifications effectuées sur le contenu HTML/CSS et les deux champs. Le rendu dans un navigateur, l'affichage mobile et le déploiement GitHub Pages restent à vérifier.
