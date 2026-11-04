# Gobelin Portail — page piège (exercice pédagogique)

Page de sensibilisation à l'hameçonnage réalisée dans le cadre d'un exercice
« Social & Cyber Sécurité » (EFREI). L'entreprise **Hyperbole Interactive**, le
studio **Gobelin Hurlant** et toutes les personnes mentionnées sont **fictifs**
(domaine `.example`).

> **Le formulaire est 100 % inerte** : à la soumission, les champs sont vidés
> sans qu'aucune valeur ne soit lue, et la page affiche un écran « en travaux ».
> Rien n'est lu, envoyé, ni stocké. Aucune donnée n'est collectée.

## Mettre en ligne sur GitHub Pages

### Option 1 — sans ligne de commande (le plus simple)
1. Sur github.com, crée un dépôt **public** nommé `gobelin-portail`.
2. **Add file → Upload files** → dépose `index.html` (et ce `README.md`) → **Commit changes**.
3. Onglet **Settings → Pages** → *Source* : branche `main`, dossier `/ (root)` → **Save**.
4. Attends ~1 minute : l'URL s'affiche, au format
   `https://<ton-compte>.github.io/gobelin-portail/`.
5. **Vérifie-la en navigation privée** pour confirmer qu'elle est publique.

### Option 2 — en ligne de commande
    git init
    git add index.html README.md
    git commit -m "Page piege - exercice pedagogique (inerte)"
    git branch -M main
    git remote add origin https://github.com/<ton-compte>/gobelin-portail.git
    git push -u origin main
Puis active **Settings → Pages** (branche `main`, dossier racine).

## Ensuite
Reporte l'URL obtenue partout où elle est attendue :
- le **lien au survol** du mail de phishing,
- le **SMS** (smishing),
- le **QR code** de la page piège,
- le **PDF de rendu** (`SocialCyberSecu_<n°équipe>_EFREI.pdf`).
