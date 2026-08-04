# PILOT — Gestion de Projet Industriel

Outil de pilotage de projet en un seul fichier HTML autonome (aucun serveur, aucune dépendance à installer). Optimisé pour un usage sur iPhone et iPad, avec prise en charge de l'ajout à l'écran d'accueil.

## Déploiement sur GitHub Pages (5 minutes)

1. **Créer le repo**
   Sur GitHub, cliquer sur *New repository*. Nom libre (ex: `pilot`). Public ou privé selon ton offre GitHub.

2. **Ajouter les fichiers**
   Mettre `index.html` (et ce `README.md`) à la racine du repo, puis commit/push.
   *Le fichier doit s'appeler exactement `index.html` pour être servi automatiquement à la racine du site.*

3. **Activer GitHub Pages**
   Dans le repo : `Settings` → `Pages` (menu de gauche) → sous *Build and deployment*, choisir :
   - Source : `Deploy from a branch`
   - Branch : `main` / dossier `/ (root)`
   Cliquer sur `Save`.

4. **Récupérer l'URL**
   Après 1–2 minutes, l'URL apparaît en haut de la page Pages, du type :
   `https://ton-pseudo.github.io/pilot/`
   (GitHub Pages est servi en HTTPS automatiquement — nécessaire pour que le mode "ajout à l'écran d'accueil" fonctionne correctement sur iOS.)

5. **Ajouter à l'écran d'accueil (iPhone/iPad)**
   Ouvrir l'URL dans Safari → bouton *Partager* → *Sur l'écran d'accueil*. L'icône et le nom "PILOT" apparaissent automatiquement, et l'app s'ouvre ensuite en plein écran sans barre Safari.

## À savoir sur les données

Les données du projet sont stockées **localement dans le navigateur** (`localStorage`), pas sur un serveur :

- Chaque appareil/navigateur a ses propres données, indépendantes des autres.
- Safari classique et l'app ajoutée à l'écran d'accueil ont des stockages **séparés** au départ : si tu utilises d'abord Safari puis ajoutes l'app à l'écran d'accueil, la version "app" partira de zéro. Ensuite, elle conserve bien ses données d'une session à l'autre.
- Pour faire passer les données d'un appareil à l'autre (ex: iPhone → iPad), utiliser les boutons **Export** (télécharge un fichier `.json`) et **Importer** (recharge ce fichier) présents dans la barre latérale.
- Penser à exporter régulièrement en JSON pour avoir une sauvegarde, au cas où le navigateur efface son stockage local (nettoyage manuel, réinstallation, etc.).

## Mettre à jour l'outil plus tard

Remplacer `index.html` par une nouvelle version et pousser un commit — GitHub Pages se met à jour automatiquement en quelques dizaines de secondes. Les données des utilisateurs (dans `localStorage`) ne sont pas affectées par une mise à jour du fichier.
