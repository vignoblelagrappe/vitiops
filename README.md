# VitiOps — Vignoble La Grappe

App de suivi des heures, tâches, traitements phytosanitaires, observations
et kilométrage pour le vignoble. Fonctionne entièrement dans le navigateur —
aucune donnée n'est envoyée à un serveur, tout reste sur l'appareil
(stockage local IndexedDB). La sauvegarde/partage entre appareils se fait
manuellement via export/import JSON (menu **Données**).

## Mettre le site en ligne (GitHub Pages)

1. Crée un nouveau dépôt GitHub (public), par ex. `vitiops`.
2. Dépose-y les fichiers de ce dossier tels quels, à la racine :
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - le dossier `icons/` (avec les 5 fichiers PNG)
3. Dans le dépôt : **Settings → Pages → Source : Deploy from a branch**,
   choisis la branche `main` et le dossier `/root`. Enregistre.
4. GitHub te donne une adresse du genre
   `https://<ton-nom-utilisateur>.github.io/vitiops/` — c'est ton app en ligne.

## Installer l'icône sur ton téléphone (iPhone)

1. Ouvre l'adresse ci-dessus dans **Safari** (important : Safari, pas Chrome,
   pour l'installation sur iPhone).
2. Touche le bouton de partage (carré avec la flèche).
3. Choisis **Sur l'écran d'accueil**.
4. L'icône « VitiOps » (grappe La Grappe) apparaît sur ton écran d'accueil,
   et l'app s'ouvre en plein écran comme une vraie app, sans barre d'adresse.

## Mettre à jour l'app plus tard

Quand une nouvelle version est prête, remplace simplement `index.html`
(et `sw.js` si modifié) dans le dépôt GitHub. Les données déjà saisies sur
le téléphone restent intactes (elles vivent dans IndexedDB, séparément du
code de l'app) — pense quand même à faire un export JSON avant toute mise
à jour majeure, par précaution.

## Sauvegarde des données

Dans le menu **Données** de l'app :
- **Exporter la sauvegarde (JSON)** — à faire régulièrement, à conserver
  sur iCloud Drive ou un autre espace de stockage.
- **Importer** — pour restaurer une sauvegarde ou transférer les données
  vers un autre appareil.
