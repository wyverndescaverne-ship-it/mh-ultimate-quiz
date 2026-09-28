# 🎮 MONSTER HUNTER ULTIMATE QUIZ

**Application Windows complète de quiz inspirée de l'univers Monster Hunter**

- ✅ **200 questions uniques et vérifiées** (FR/EN)
- ✅ **Interface AAA** (animations, sons, effets visuels)
- ✅ **Système de score, combo, timer, statistiques**
- ✅ **Multilingue** (Français/Anglais)
- ✅ **Mode survie, classique, rapide, par catégorie, par jeu**
- ✅ **Système de succès (achievements)**
- ✅ **Audio personnalisable** (musique, SFX, voix)
- ✅ **Responsive** (PC, tablette, mobile)

---

## 📥 **TÉLÉCHARGEMENT & INSTALLATION (POUR LES DÉBUTANTS)**

### **🔹 Méthode 1 : Télécharger le ZIP (recommandé)**
1. **Téléchargez le projet** :
   → [Télécharger le ZIP complet](https://github.com/wyverndescaverne-ship-it/mh-ultimate-quiz/archive/refs/heads/main.zip)
2. **Décompressez le ZIP** dans un dossier (ex: `C:\mh-quiz`).
3. **Passez à l'étape 2** ci-dessous.

---

### **🔹 Méthode 2 : Cloner avec Git (si vous avez Git installé)**
1. Ouvrez **l'Invite de commandes (CMD)**.
2. Tapez :
   ```bash
   git clone https://github.com/wyverndescaverne-ship-it/mh-ultimate-quiz.git
   cd mh-ultimate-quiz
   ```

---

## 🛠️ **ÉTAPE 2 : INSTALLER LES OUTILS NÉCESSAIRES**

### **🔹 Installer Node.js (OBLIGATOIRE)**
1. **Téléchargez Node.js** :
   → [https://nodejs.org/fr/download/](https://nodejs.org/fr/download/)
   → **Choisissez la version LTS** (recommandée).
2. **Installez Node.js** :
   - Cochez **"Automatically install necessary tools"**.
   - Cliquez sur **Next** à chaque étape.
3. **Vérifiez l'installation** :
   - Ouvrez **l'Invite de commandes (CMD)**.
   - Tapez :
     ```bash
     node -v
     npm -v
     ```
   - **✅ Si vous voyez des numéros de version (ex: `v18.17.0` et `9.6.7`), c'est bon !**

---

## 🚀 **ÉTAPE 3 : CONSTRUIRE L'APPLICATION (GÉNÉRER LE .EXE)**

1. **Ouvrez l'Invite de commandes (CMD)** dans le dossier du projet :
   - Appuyez sur **`Win + R`**, tapez **`cmd`**, puis **Entrée**.
   - Dans la fenêtre noire, tapez :
     ```bash
     cd C:\mh-ultimate-quiz
     ```
     *(Remplacez `C:\mh-ultimate-quiz` par le chemin où vous avez décompressé le ZIP.)*

2. **Installez les dépendances** :
   ```bash
   npm install
   ```
   *(Cela peut prendre 2-3 minutes. Attendez que ça se termine.)*

3. **Construisez l'application** :
   ```bash
   npm run build
   ```
   *(Cela génère les fichiers nécessaires.)*

4. **Générez l'exécutable (.exe)** :
   ```bash
   npm run package
   ```
   *(Cela crée un dossier `dist` contenant `MonsterHunterQuiz.exe`.)*

---

## 🎮 **ÉTAPE 4 : LANCER LE QUIZ !**

1. Allez dans le dossier **`dist`** (à l'intérieur de `mh-ultimate-quiz`).
2. **Double-cliquez sur `MonsterHunterQuiz.exe`**.
3. **Profitez du quiz !**

---

## 📁 **STRUCTURE DU PROJET**
```
mh-ultimate-quiz/
├── src/                  # Code source
│   ├── components/       # Composants React
│   ├── pages/            # Pages de l'application
│   ├── data/             # Données (questions, jeux, catégories)
│   │   ├── questions.json # 200 questions vérifiées
│   │   ├── games.json    # Liste des jeux Monster Hunter
│   │   └── categories.json # Catégories de questions
│   ├── hooks/            # Hooks personnalisés
│   ├── services/         # Services (audio, statistiques)
│   ├── utils/            # Fonctions utilitaires
│   ├── types/            # Types TypeScript
│   ├── i18n/             # Traductions (FR/EN)
│   └── styles/           # Styles CSS
├── public/               # Assets statiques
│   ├── audio/            # Sons (SFX, musique)
│   └── images/           # Images (fond, icônes)
├── package.json          # Configuration du projet
├── vite.config.ts        # Configuration de Vite
└── README.md             # Ce fichier
```

---

## 🔍 **APERÇU DES 200 QUESTIONS**

### **Exemple de question (format JSON)**
```json
{
  "id": 1,
  "game": "Monster Hunter: World",
  "category": "Monstres",
  "difficulty": "facile",
  "question": {
    "fr": "Quel monstre est connu comme le 'Roi des Cieux' ?",
    "en": "Which monster is known as the 'King of the Skies'?"
  },
  "answers": [
    { "id": "A", "fr": "Rathalos", "en": "Rathalos" },
    { "id": "B", "fr": "Nargacuga", "en": "Nargacuga" },
    { "id": "C", "fr": "Zinogre", "en": "Zinogre" },
    { "id": "D", "fr": "Diablos", "en": "Diablos" }
  ],
  "correctAnswer": "A",
  "explanation": {
    "fr": "Rathalos est surnommé le 'Roi des Cieux' en raison de sa domination aérienne.",
    "en": "Rathalos is nicknamed the 'King of the Skies' due to its aerial dominance."
  },
  "sources": [
    {
      "name": "Capcom - Monster Hunter: World Official Guide",
      "url": "https://game.capcom.com/manual/mhw/fr/",
      "type": "official",
      "verified": true
    }
  ]
}
```

### **Catégories disponibles**
- 🐉 **Monstres** (Noms, caractéristiques, faiblesses)
- ⚔️ **Armes** (Types, mouvements, mécaniques)
- 🛡️ **Armures** (Compétences, sets, bonus)
- 🧪 **Objets** (Potions, pièges, consommables)
- 🎮 **Gameplay** (Mécaniques, astuces, stratégies)
- 📜 **Lore** (Histoire, personnages, lieux)
- 🏆 **Personnages** (PNJ, chasseurs légendaires)

### **Niveaux de difficulté**
- 🟢 **Facile** (Questions générales)
- 🟡 **Normal** (Connaissance du gameplay)
- 🟠 **Difficile** (Détails précis)
- 🔴 **Expert** (Mécaniques avancées, trivia)

---

## 🎯 **FONCTIONNALITÉS**

### **Modes de jeu**
| Mode | Description |
|------|-------------|
| **Classique** | 200 questions aléatoires |
| **Rapide** | 10 questions chronométrées |
| **20 Questions** | 20 questions aléatoires |
| **Par Jeu** | Questions d'un jeu spécifique |
| **Par Catégorie** | Questions d'une catégorie spécifique |
| **Expert** | Uniquement des questions difficiles |
| **Survie** | Une erreur = élimination |

### **Système de score**
- ✅ **+100 points** par bonne réponse
- ⚡ **Bonus de rapidité** (jusqu'à +100 points)
- 🔥 **Combo** (x2, x3, x4, x5)
- ❌ **0 point** pour une mauvaise réponse ou temps écoulé

### **Timer**
- ⏳ **5 secondes** par question
- ⚠️ **Effet sonore à 3 secondes**
- ❌ **Son d'expiration à 0 seconde**
- 🎨 **Animation visuelle** (cercle, barre de progression)

### **Statistiques**
- 📊 **Parties jouées**
- ✅ **Bonnes/mauvaises réponses**
- 📈 **Pourcentage de réussite**
- 🏆 **Meilleur score**
- 🔥 **Meilleur combo**
- ⏱️ **Temps moyen de réponse**
- 📉 **Questions les plus difficiles**

### **Succès (Achievements)**
| Succès | Description |
|--------|-------------|
| 🏆 **Première chasse** | Répondre correctement à 1 question |
| 🏆 **Chasseur confirmé** | 50 bonnes réponses |
| 🏆 **Maître chasseur** | 100 bonnes réponses |
| 🏆 **Bibliothèque vivante** | Répondre à 200 questions |
| 🏆 **Sans faute** | Terminer une partie sans erreur |
| 🏆 **Foudre** | Répondre très rapidement à 5 questions |
| 🏆 **Expert** | Réussir 20 questions difficiles |

---

## 🎨 **INTERFACE & DESIGN**

### **Menu Principal**
- 🎮 **JOUER** (Lancer un quiz)
- 🎯 **MODES DE JEU** (Choisir un mode)
- 🎮 **CHOISIR UN JEU** (Filtrer par jeu)
- 📊 **STATISTIQUES** (Voir vos performances)
- 🏆 **SUCCÈS** (Voir vos récompenses)
- ⚙️ **OPTIONS** (Paramètres audio, langue)
- 📜 **CRÉDITS** (Informations sur le projet)
- ❌ **QUITTER** (Quitter l'application)

### **Écran du Quiz**
```
━━━━━━━━━━━━━━━━━━━━━━
       MONSTER HUNTER QUIZ
━━━━━━━━━━━━━━━━━━━━━━

Jeu : Monster Hunter: World
Question 42 / 200

« Quel monstre est le roi des cieux ? »

          ⏳ 5

    [ A ] Rathalos
    [ B ] Nargacuga
    [ C ] Zinogre
    [ D ] Diablos

━━━━━━━━━━━━━━━━━━━━━━
Score : 8450 | Combo : x7
━━━━━━━━━━━━━━━━━━━━━━
```

### **Design Inspiré de Monster Hunter**
- 🪵 **Textures bois** (arrière-plan, panneaux)
- ⚔️ **Éléments métalliques** (bordures, boutons)
- 📜 **Parchemins** (pour les questions et explications)
- 🔥 **Effets de feu/particules** (animations)
- 🎨 **Couleurs chaudes** (oranges, bruns, noirs)

---

## 🔊 **SYSTÈME AUDIO**

### **Musique & Effets Sonores**
- 🎵 **Musique de fond** (ambiance guilde)
- 🔊 **SFX** (clics, sélections, transitions)
- 🗣️ **Voix** (confirmations, erreurs)

### **Paramètres Audio (dans OPTIONS)**
| Paramètre | Description |
|-----------|-------------|
| **Volume général** | 0-100% |
| **Musique** | 0-100% |
| **Effets sonores** | 0-100% |
| **Voix** | 0-100% |
| **Mute** | ON/OFF |

---

## 🌍 **LANGUES**

### **Bilingue FR/EN**
- 🇫🇷 **Français** (traductions officielles Capcom)
- 🇬🇧 **English** (official Capcom terms)
- 🔄 **Changement instantané** (bouton FR/EN dans l'interface)

---

## 🐛 **DÉPANNAGE**

### **Problème : `node` ou `npm` non reconnu**
❌ **Erreur** :
```
'node' is not recognized as an internal or external command...
```
✅ **Solution** :
1. **Réinstallez Node.js** en cochant **"Add to PATH"**.
2. **Redémarrez votre PC**.
3. **Réessayez** dans une nouvelle fenêtre CMD.

---

### **Problème : `npm install` échoue**
❌ **Erreur** :
```
ERRORE: Failed to parse JSON
```
✅ **Solution** :
1. **Supprimez le dossier `node_modules`** (s'il existe).
2. **Supprimez `package-lock.json`**.
3. **Relancez** :
   ```bash
   npm install
   ```

---

### **Problème : `npm run package` échoue**
❌ **Erreur** :
```
Failed to load URL: win32 x64
```
✅ **Solution** :
1. **Installez `electron-builder` manuellement** :
   ```bash
   npm install electron-builder --save-dev
   ```
2. **Relancez** :
   ```bash
   npm run package
   ```

---

### **Problème : L'application ne s'ouvre pas**
❌ **Erreur** :
```
Nothing happens when I click the .exe
```
✅ **Solution** :
1. **Vérifiez que `dist/win-unpacked` existe**.
2. **Essayez de lancer `MonsterHunterQuiz.exe` depuis l'Invite de commandes** :
   ```bash
   cd dist
   MonsterHunterQuiz.exe
   ```
3. **Si ça ne marche toujours pas**, installez **Electron** globalement :
   ```bash
   npm install -g electron
   ```

---

## 📜 **LICENCE & CRÉDITS**

### **Licence**
- **Code** : MIT (libre utilisation, modification, distribution)
- **Assets** :
  - Sons : **Libres de droits** (ou créés pour le projet)
  - Images : **Libres de droits** (ou créées pour le projet)
  - **❌ AUCUN asset officiel Capcom** n'est utilisé (pour éviter les problèmes de copyright).

### **Crédits**
- **Développement** : [wyverndescaverne-ship-it](https://github.com/wyverndescaverne-ship-it)
- **Inspiration** : Univers de **Monster Hunter** (Capcom)
- **Données** : Basé sur les **manuels officiels Capcom** et **wikis communautaires vérifiés**.

---

## 🤝 **CONTRIBUER**

### **Comment aider ?**
1. **Signaler un bug** : Ouvrez une **Issue** sur GitHub.
2. **Proposer une amélioration** : Ouvrez une **Pull Request**.
3. **Ajouter des questions** :
   - Vérifiez qu'elles sont **uniques** et **sourcées**.
   - Respectez le **format JSON** dans `data/questions.json`.

---

## 📞 **CONTACT**

- **GitHub** : [wyverndescaverne-ship-it/mh-ultimate-quiz](https://github.com/wyverndescaverne-ship-it/mh-ultimate-quiz)
- **Problèmes techniques** : Ouvrez une **Issue** sur le dépôt.

---

**✨ Bon quiz, chasseur !** 🎮🔥