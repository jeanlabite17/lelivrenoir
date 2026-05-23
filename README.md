# Le Livre Noir

Annuaire de profils — site statique HTML/CSS/JS, hébergé sur GitHub Pages.

## Structure des fichiers

```
lelivrenoir/
├── index.html      ← page principale (listing + profil)
├── admin.html      ← panneau pour générer le code d'un profil
├── data.js         ← tous les profils (à modifier)
└── images/
    ├── sofia.jpg
    └── ...
```

---

## Ajouter un profil

**Option 1 — Via le panneau admin (recommandé)**
1. Ouvre `admin.html` dans ton navigateur
2. Remplis le formulaire
3. Copie le code généré
4. Colle-le dans `data.js` dans le tableau `PROFILES`, avant le `]` final (séparé par une virgule)
5. Place la photo dans `images/`
6. Push sur GitHub

**Option 2 — Directement dans data.js**
Copie un bloc existant et modifie les valeurs.

---

## Mettre en ligne sur GitHub Pages

1. Crée un repo GitHub (ex: `lelivrenoir`)
2. Upload tous les fichiers
3. Va dans **Settings → Pages**
4. Source : **Deploy from a branch → main → / (root)**
5. Ton site est en ligne sur `https://tonpseudo.github.io/lelivrenoir/`

### Avec un nom de domaine personnalisé
1. Dans Settings → Pages → Custom domain : entre ton domaine (ex: `lelivrenoir.com`)
2. Chez ton registrar (où t'as acheté le domaine), ajoute ces DNS :
   - Type A → `185.199.108.153`
   - Type A → `185.199.109.153`
   - Type A → `185.199.110.153`
   - Type A → `185.199.111.153`
   - Type CNAME → `www` → `tonpseudo.github.io`

---

## SEO — ce qui est intégré

- `<title>` dynamique par profil (Prénom Nom — Le Livre Noir)
- `<meta description>` générée automatiquement
- Schema.org `Person` en JSON-LD (lu en priorité par Google)
- Open Graph (partage sur réseaux sociaux)
- URLs propres avec ancres `#prenom-nom`
- Navigation navigateur (bouton retour fonctionne)
