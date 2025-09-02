# 📖 Quran Data Repository

Ce dossier contient une **base de données locale du Coran** organisée par sourate.  
Il a été construit en utilisant l’API de [quran.com](https://quran.com) / [Quran Foundation](https://quran.foundation), puis sauvegardé en fichiers JSON et audio.

---

## 📂 Structure du dossier

```
quran/
├── 1-al-fatihah/
│   ├── infos.json          # Métadonnées de la sourate (nom, numéro, versets, etc.)
│   ├── verses.json         # Versets complets avec traduction(s)
│   ├── tajweed.json        # Texte du Coran avec les règles de tajwīd (balises <tajweed>)
│   ├── audio/
│   │   ├── reciterName-id-single.json   # Audio de la sourate complète pour un réciteur
│   │   ├── reciterName-id-verses.json   # Audio verset par verset pour un réciteur
│   │   └── ... (autres récitateurs)
│   └── ...
├── 2-al-baqarah/
│   ├── infos.json
│   ├── verses.json
│   ├── tajweed.json
│   ├── audio/
│   │   ├── ...
│   └── ...
└── ...
```

---

## 📑 Contenu des fichiers

- **`infos.json`** → métadonnées de la sourate (nom arabe, nom simple, nombre de versets, etc.).  
- **`verses.json`** → tous les versets avec texte arabe, traduction, et éventuellement mot à mot.  
- **`tajweed.json`** → texte arabe enrichi avec les règles de tajwīd (via balises HTML).  
- **`audio/`** → enregistrements audio :
  - `*-single.json` → fichier JSON contenant l’URL d’un enregistrement complet de la sourate pour un réciteur.
  - `*-verses.json` → fichiers JSON listant l’URL de chaque verset audio pour un réciteur.

---

## 🎯 Objectif

Ce dépôt permet de :
- Sauvegarder les données textuelles et audio du Coran en local.  
- Éviter les appels répétés à l’API distante.  
- Fournir une base pour développer une application (lecture, apprentissage, tajwīd, etc.).  

---

## ⚠️ Remarques

- Les fichiers audio référencés pointent vers les ressources de Quran.com (ils ne sont pas stockés localement ici).  
- Le contenu textuel (versets, tajwīd) provient de l’API officielle de Quran.com / Quran Foundation.  
- Ce projet est destiné à un usage éducatif et de recherche.  

