# Ma Vertu du Jour — PWA
### influencons.com — Influencons Autrement

---

## 📁 Structure du dossier

```
vertu-pwa/
├── index.html       ← Application principale
├── manifest.json    ← Config PWA (icônes, couleurs, nom)
├── sw.js            ← Service Worker (cache offline + notifications)
├── icons/
│   ├── icon-192.png ← Icône PWA petite
│   └── icon-512.png ← Icône PWA grande
└── README.md        ← Ce fichier
```

---

## 🚀 Déploiement

### Option 1 — Hébergement simple (recommandé pour commencer)
Uploadez tous les fichiers tels quels sur votre hébergeur via FTP ou le gestionnaire de fichiers.
Le site doit être servi en **HTTPS** (obligatoire pour les PWA).

### Option 2 — Netlify (gratuit, ultra simple)
1. Allez sur [netlify.com](https://netlify.com)
2. Faites glisser le dossier `vertu-pwa/` dans l'interface
3. C'est en ligne en 30 secondes ✅

### Option 3 — Vercel (gratuit)
```bash
npm install -g vercel
cd vertu-pwa
vercel
```

### Option 4 — Sous-dossier de influencons.com
Uploadez le dossier dans `/vertu/` sur votre serveur.
Accès via : `https://influencons.com/vertu/`

---

## 📱 Installation comme application (PWA)

### Sur mobile (Android/iOS) :
1. Ouvrez le site dans Chrome ou Safari
2. Appuyez sur le bouton **"Partager"** ou les **3 points** du navigateur
3. Sélectionnez **"Ajouter à l'écran d'accueil"**
4. L'app s'installe comme une vraie application ! ✅

### Sur ordinateur (Chrome) :
1. Ouvrez le site
2. Cliquez sur l'icône d'installation dans la barre d'adresse
3. Cliquez "Installer"

---

## 🔔 Notifications quotidiennes

Les notifications fonctionnent **sans serveur** grâce au JavaScript natif.
- L'utilisateur clique sur la 🔔 cloche en haut à droite
- Il choisit l'heure du rappel
- Le navigateur envoie une notification chaque jour à l'heure choisie
- Fonctionne même avec l'écran éteint sur Android

> **Note :** Sur iOS (iPhone), les notifications PWA nécessitent iOS 16.4+ et que l'app soit ajoutée à l'écran d'accueil.

---

## ✨ Fonctionnalités

- 🎴 **40 vertus chrétiennes** pour les 40 jours du Carême
- 📖 **Verset biblique** associé à chaque vertu
- 🎯 **Défi concret** du jour
- 📊 **Barre de progression** du Carême
- 📱 **Partage** Facebook, WhatsApp, presse-papier
- 🕐 **Historique** des 10 dernières vertus
- 🔔 **Notification quotidienne** programmable
- 📶 **Mode hors-ligne** (fonctionne sans internet après première visite)
- 💜 Design violet et or, responsive mobile

---

## 🛠️ Personnalisation

### Changer les couleurs
Dans `index.html`, modifiez les variables CSS en haut :
```css
:root {
  --violet-deep:  #1E0433;  /* Fond principal */
  --gold:         #E8C84A;  /* Couleur or */
}
```

### Ajouter des vertus
Dans `index.html`, ajoutez un objet au tableau `VERTUS` :
```javascript
{
  nom: "La Nouvelle Vertu",
  def: "Définition de la vertu.",
  verset: "« Le verset biblique. »",
  ref: "Livre X,Y",
  defi: "Le défi du jour à accomplir."
}
```

### Changer les dates du Carême
Modifiez ces deux lignes dans la fonction `updateCaremeProgress()` :
```javascript
const careme2025Start = new Date('2025-03-05'); // Mercredi des Cendres
const careme2025End   = new Date('2025-04-20'); // Pâques
```

---

## 📞 Support
Développé avec ❤️ pour **influencons.com** — Influencons Autrement
