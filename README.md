# macOS 2026 - Scientific Edition Simulation

Simulation interactive d'un système macOS 2026 avec thème scientifique, incluant un mini-jeu de labyrinthe quantique.

## Fonctionnalités

### Écran de connexion
- Design moderne avec effets visuels
- Mot de passe : `Shamballa023`
- Thème scientifique avec interface futuriste

### Bureau macOS
- Barre de menu avec horloge en temps réel
- Dock interactif avec animations
- 5 dossiers scientifiques verrouillés :
  - 🧠 Données IA
  - 🔬 Recherches
  - ⚗️ Expériences
  - 🌌 Simulations
  - 📊 Rapports

### Mini-jeu "Quantum Maze"
- 5 niveaux de difficulté croissante
- Joueur : Cube bleu (contrôlable)
- Ennemi : Triangle rouge avec IA de poursuite
- Objectif : Atteindre la cible verte
- Contrôles : Flèches directionnelles ou ZQSD
- Système de vies (3 vies)
- Écran "screamer" à la perte

## Déploiement sur Vercel

### Option 1 : Déploiement via GitHub

1. Créez un nouveau repository sur GitHub
2. Poussez le code :
```bash
git add .
git commit -m "Initial commit: macOS simulation"
git branch -M main
git remote add origin https://github.com/VOTRE-USERNAME/VOTRE-REPO.git
git push -u origin main
```

3. Allez sur [vercel.com](https://vercel.com)
4. Connectez-vous avec GitHub
5. Cliquez sur "Add New Project"
6. Importez votre repository
7. Cliquez sur "Deploy"

### Option 2 : Déploiement direct via Vercel CLI

1. Installez Vercel CLI :
```bash
npm i -g vercel
```

2. Déployez :
```bash
vercel
```

3. Suivez les instructions à l'écran

### Option 3 : Déploiement par glisser-déposer

1. Allez sur [vercel.com](https://vercel.com)
2. Connectez-vous
3. Glissez-déposez le dossier du projet directement sur le dashboard

## Ajout du MP3 Screamer

Pour ajouter votre fichier MP3 screamer :

1. Placez votre fichier MP3 dans le même dossier que `index.html`
2. Dans `index.html`, ligne ~566, remplacez :
```javascript
function showScreamer() {
    closeGame();
    document.getElementById('screamer-popup').style.display = 'flex';
    // Ici vous ajouterez le son MP3 plus tard
}
```

Par :
```javascript
function showScreamer() {
    closeGame();
    document.getElementById('screamer-popup').style.display = 'flex';
    const scream = new Audio('votre-fichier.mp3');
    scream.volume = 1.0; // Volume maximum
    scream.play();
}
```

## Technologies utilisées

- HTML5
- CSS3 (Animations, Gradients, Backdrop Filter)
- JavaScript (Canvas API, Game Loop)
- Design inspiré de macOS Big Sur/Monterey

## Crédits

Simulation créée avec Claude Code
