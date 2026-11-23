# HediLingua

Application PWA personnelle : préparation TOEIC et allemand débutant vers professionnel.

## Démarrage

### Sur ordinateur
1. Installer **Visual Studio Code**.
2. Ouvrir le dossier `HediLingua` dans VS Code.
3. Installer l'extension **Live Server** et lancer `index.html` avec **Open with Live Server**. On peut aussi lancer `python -m http.server 8000` depuis le dossier et ouvrir `http://localhost:8000`.
4. Modifier les fichiers CSS, HTML et JavaScript ; actualiser la page.

### Publication gratuite sur GitHub Pages
1. Créer un compte GitHub et un dépôt **public** nommé `HediLingua`.
2. Envoyer **le contenu du dossier** `HediLingua` à la racine du dépôt (`index.html`, `css`, `js`, etc.).
3. Dans **Settings > Pages**, choisir **Deploy from a branch**, puis `main` et `/ (root)`.
4. Attendre la publication, puis ouvrir `https://VOTRE-PSEUDO.github.io/HediLingua/`.
5. Sur iPhone : ouvrir cette adresse dans **Safari**, toucher **Partager** puis **Sur l'écran d'accueil**.

> L'icône et le mode hors ligne nécessitent une origine HTTPS (GitHub Pages le fournit) ou localhost. Ouvrir directement `index.html` en `file://` ne permet pas de tester correctement la PWA.

## Personnaliser
- `css/style.css` : couleurs (`--bg`, `--paper`, `--navy`), polices et mise en page.
- `icons/icon.svg` : logo HL bleu marine.
- `js/data.js` : banque initiale de questions et fiches.
- Dans **Paramètres**, modifier le programme, ajouter/supprimer des QCM et des fiches.
- Dans **Mes fiches**, modifier le contenu des leçons.
- **Exporter mes données** régulièrement : la sauvegarde JSON conserve tes modifications et ta progression.

## Important
- Les questions sont **originales et non officielles**, inspirées des compétences évaluées au TOEIC ; les tests ne donnent **pas** une estimation officielle du score TOEIC.
- La partie Listening utilise la synthèse vocale disponible sur l'appareil ; les voix peuvent varier.
- L'application stocke ses données avec `localStorage` dans le navigateur, sans synchronisation automatique. Effacer les données du navigateur peut effacer les progrès. Exporter régulièrement.
- La durée affichée est celle réellement passée dans le quiz, arrondie à la minute ; il ne s'agit pas d'un programme guidé de 30 minutes entièrement rempli. Le nombre initial de questions est volontairement limité.
- La fonction **IA n'est pas encore intégrée**. Ne jamais mettre de clé API secrète dans les fichiers JavaScript publics ou dans GitHub Pages. Pour l'ajouter, prévoir un serveur ou une fonction cloud sécurisée.
- Les fichiers du dépôt GitHub Pages sont publics : ne pas y publier de données personnelles ni de clés secrètes.

## Structure
```
index.html
css/style.css
js/data.js
js/app.js
icons/icon.svg
icons/icon-192.png
icons/icon-512.png
manifest.webmanifest
service-worker.js
README.md
```
