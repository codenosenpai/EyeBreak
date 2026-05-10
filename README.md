# 👀 EyeBreak

> **Coder comme un ninja, enseigner comme un sensei.**
> *Un projet [Code no Senpaï](https://github.com/codenosenpai)*

Application desktop de rappels de pauses oculaires — inspirée de Stretchly, construite avec Electron.
Fonctionne sur **Windows**, **macOS** et **Linux**.

---

## ✨ Fonctionnalités

- 🕐 **Mini-pauses** configurables (défaut : 20 sec toutes les 20 min)
- 🌿 **Grandes pauses** configurables (défaut : 5 min toutes les heures)
- 🖥️ Écran de pause **plein écran**, toujours au premier plan
- 🔔 **Son d'alerte** doux (désactivable)
- ⚙️ **Paramètres** accessibles depuis l'icône barre des tâches
- 🚀 **Démarrage automatique** avec le PC
- 🥷 Footer **Code no Senpaï** intégré

---

## 📦 Installation rapide

### Prérequis

- [Node.js](https://nodejs.org) v18 ou supérieur
- npm (inclus avec Node.js)

### Lancer en développement

```bash
# 1. Cloner le repo
git clone https://github.com/codenosenpai/eyebreak.git
cd eyebreak

# 2. Installer les dépendances
npm install

# 3. Lancer l'application
npm start
```

L'icône EyeBreak apparaît dans votre barre des tâches. C'est tout !

---

## 🏗️ Créer un installeur

```bash
# Windows (.exe)
npm run build-win

# macOS (.dmg)
npm run build-mac

# Linux (.AppImage)
npm run build-linux
```

Les fichiers sont générés dans le dossier `dist/`.

---

## 🗂️ Structure du projet

```
eyebreak/
├── src/
│   ├── main.js          # Point d'entrée Electron
│   ├── timer.js         # Logique des minuteurs
│   └── tray.js          # Icône & menu système
├── windows/
│   ├── break.html       # Écran de pause (plein écran)
│   └── settings.html    # Fenêtre de paramètres
├── assets/
│   ├── icon.png         # Icône app (256×256 min)
│   └── img/
│       └── logo-senpai.png
└── package.json
```

---

## ⚙️ Configuration

Clic droit sur l'icône → **Paramètres**

| Paramètre | Défaut | Description |
|---|---|---|
| Intervalle mini-pause | 20 min | Fréquence des pauses courtes |
| Durée mini-pause | 20 sec | Durée de la pause courte |
| Intervalle grande pause | 60 min | Fréquence des grandes pauses |
| Durée grande pause | 5 min | Durée de la grande pause |
| Son d'alerte | Activé | Bip doux au déclenchement |
| Démarrage auto | Activé | Lance EyeBreak au démarrage du PC |

Les paramètres sont sauvegardés automatiquement et les minuteurs redémarrent sans quitter l'app.

---

## 🧠 Pourquoi faire des pauses ?

La **règle 20-20-20** est recommandée par les ophtalmologistes :

> Toutes les **20 minutes**, fixe un point à **6 mètres** pendant **20 secondes**.

Cela détend les muscles ciliaires de l'œil, réduit la fatigue visuelle, les maux de tête, et la sécheresse oculaire.

---

## 🛠️ Stack technique

| Composant | Technologie |
|---|---|
| Runtime desktop | Electron v28+ |
| Langage | JavaScript (Node.js) |
| Persistance | electron-store |
| Build | electron-builder |
| UI | HTML5 + CSS3 vanille |

---

## 🤝 Contribuer

Les contributions sont les bienvenues !

```bash
# Fork + clone
git checkout -b feature/ma-fonctionnalite
git commit -m "feat: ajout de ma fonctionnalité"
git push origin feature/ma-fonctionnalite
# → Ouvrir une Pull Request
```

**Conventions de commit :**
`feat:` `fix:` `docs:` `chore:` `refactor:`

---

## 📋 Roadmap

- [x] Mini-pauses et grandes pauses
- [x] Écran plein écran avec anneau de progression
- [x] System tray + menu contextuel
- [x] Démarrage automatique
- [x] Son d'alerte configurable
- [ ] Mode "Ne pas déranger" (détection plein écran)
- [ ] Statistiques de pauses
- [ ] Thèmes visuels
- [ ] Exercices oculaires animés
- [ ] Synchronisation cloud (v2)

---

## 📄 Licence

MIT — libre d'utilisation, de modification et de distribution.

---

<div align="center">

<img src="assets/img/logo-senpai.png" alt="Logo Code no Senpaï" height="48" />

<hr width="50%" />

Projet conçu par **Code no Senpaï**
*Coder comme un ninja, enseigner comme un sensei.*

</div>
