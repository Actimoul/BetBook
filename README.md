[README.md](https://github.com/user-attachments/files/26570907/README.md)
# 🎲 BetBook

![BetBook](logo.png)

**Le registre officiel des paris entre potes.**

Tracker de paris entre amis avec synchronisation en temps réel. Créez vos paris, désignez le gagnant, suivez les scores — plus aucun pari ne sera oublié.

## 🚀 Démo

👉 **[actimoul.github.io/betbook](https://actimoul.github.io/betbook/)**

## ✨ Fonctionnalités

- 📝 Créer un pari avec description, enjeu/gage et date limite
- 👥 Joueurs prédéfinis (Aurélien, Thomas, Geoffrey, Matthieu, Claude) + ajout libre
- 🏆 Résoudre un pari en un tap — désigne le gagnant
- 🔥 Classement avec ratio W/L et graphe visuel
- 🔍 Filtrer les paris par joueur
- 📜 Historique complet de tous les paris résolus
- 🔄 Synchronisation temps réel entre tous les joueurs (Firebase)
- 📱 Mobile-first, fonctionne aussi sur desktop
- 🌙 Mode sombre

## 📦 Structure

```
betbook/
├── index.html   ← Toute l'application (zéro dépendance build)
├── logo.png     ← Logo BetBook
└── README.md
```

## 🔧 Installation

### 1. Cloner le repo

```bash
git clone https://github.com/actimoul/betbook.git
cd betbook
```

### 2. Configurer Firebase (pour le temps réel)

L'app fonctionne en **mode local** (localStorage) sans Firebase. Pour activer la synchro temps réel entre joueurs :

1. Va sur [console.firebase.google.com](https://console.firebase.google.com)
2. Crée un nouveau projet (ex: `betbook`)
3. Clique sur **</>** (Web) pour ajouter une application
4. Copie les valeurs de `firebaseConfig`
5. Ouvre `index.html` et remplace les `REMPLACE_MOI` en haut du script :

```javascript
const firebaseConfig = {
  apiKey: "AIzaSy...",
  authDomain: "betbook-xxxxx.firebaseapp.com",
  databaseURL: "https://betbook-xxxxx-default-rtdb.europe-west1.firebasedatabase.app",
  projectId: "betbook-xxxxx",
  storageBucket: "betbook-xxxxx.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abcdef123456"
};
```

6. Dans la console Firebase, va dans **Realtime Database** → **Créer une base de données** → **Mode test**
7. C'est prêt !

### 3. Déployer sur GitHub Pages

```bash
git add .
git commit -m "🎲 BetBook v1"
git push origin main
```

Puis dans les **Settings** du repo → **Pages** → Source : `main` branch → Save.

Ton site sera live sur `https://actimoul.github.io/betbook/`

## 🎮 Utilisation

1. Ouvre le lien et entre ton prénom
2. Appuie sur **+** pour créer un pari
3. Quand le résultat est connu, tape sur le nom du gagnant
4. Consulte le **classement** pour voir qui domine

## 🛠 Tech

- Vanilla JS — zéro framework, zéro build
- Firebase Realtime Database — synchro temps réel
- Google Fonts (Anybody + DM Sans)
- Déployable n'importe où (GitHub Pages, Netlify, Vercel...)

## 📄 Licence

Projet privé entre potes. Fait avec 🍺 et des mauvaises décisions.
