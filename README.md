# JuriFormulaires — Projet prêt à déployer

Ce dossier contient le prototype (le même code que l'artifact que tu vois dans Claude), mais organisé comme un vrai projet web que Vercel ou Netlify peut construire et publier automatiquement.

Je n'ai pas pu faire un test d'installation complet (`npm install`) dans mon environnement de travail, car il n'a pas accès à Internet — mais la syntaxe du code a été vérifiée, et cette structure est le modèle standard utilisé partout dans l'industrie pour ce genre de projet (React + Vite + Tailwind). Vercel et Netlify vont l'installer et le construire automatiquement sur leurs propres serveurs (qui ont accès à Internet), donc le vrai test se fera à ce moment — c'est normal et attendu.

## Étape 1 — Créer un compte GitHub (si tu n'en as pas déjà un)

GitHub est l'endroit où le code du projet va être rangé — Vercel s'y connecte directement pour publier automatiquement chaque mise à jour.

👉 https://github.com/signup

## Étape 2 — Créer un nouveau dépôt (« repository »)

1. Une fois connecté, va à : https://github.com/new
2. Nom du dépôt : `juriformulaires` (ou ce que tu préfères)
3. Laisse-le en **Private** pour l'instant (le code n'a pas à être public)
4. Clique **Create repository**
5. Sur la page qui suit, clique **uploading an existing file** et glisse-déposes TOUS les fichiers et dossiers de ce dossier-ci (garde la structure des dossiers `src/` telle quelle)
6. Clique **Commit changes**

## Étape 3 — Créer un compte Vercel

👉 https://vercel.com/signup

Choisis **Continue with GitHub** — ça relie automatiquement les deux comptes, ce qui simplifie tout le reste.

## Étape 4 — Importer le projet dans Vercel

1. Une fois connecté à Vercel : https://vercel.com/new
2. Trouve le dépôt `juriformulaires` que tu viens de créer et clique **Import**
3. Vercel détecte automatiquement qu'il s'agit d'un projet Vite — ne change rien aux réglages proposés
4. Clique **Deploy**
5. Après une minute ou deux, Vercel te donne un lien du genre `juriformulaires.vercel.app` où l'application est déjà en ligne

## Étape 5 — Brancher ton nom de domaine (juriformulaires.com)

1. Dans le projet Vercel, va dans **Settings → Domains**
2. Tape `juriformulaires.com` et clique **Add**
3. Vercel va t'afficher une ou deux valeurs précises à copier (un enregistrement de type A ou CNAME) — copie-les
4. Va dans ton compte GoDaddy → gestion DNS du domaine `juriformulaires.com`
5. Colle les valeurs exactement comme Vercel te les montre
6. Ça peut prendre de quelques minutes à quelques heures avant que ça se propage

**Attention à un détail important :** si ton site GoDaddy actuel (celui avec la page « Legal Forms Made Easy ») reste sur `juriformulaires.com`, il faut choisir lequel des deux garde le domaine principal — l'app pourrait plutôt vivre sur une adresse comme `app.juriformulaires.com` pendant que la page d'accueil reste sur `juriformulaires.com`. Dis-moi ce que tu préfères et je peux ajuster les instructions.

## Ce que tu n'as PAS besoin de faire

- Pas besoin d'installer Node.js ou quoi que ce soit sur ton ordinateur pour publier — tout se passe sur les serveurs de GitHub et Vercel
- Pas besoin de toucher au code — il est déjà prêt

## Si tu veux prévisualiser sur ton ordinateur avant de publier (optionnel)

Ceci nécessite d'installer Node.js (https://nodejs.org, choisir la version LTS) une seule fois, puis dans ce dossier :

```
npm install
npm run dev
```

Un lien local (http://localhost:5173) s'ouvrira avec l'application.

## Rappel important

Comme discuté, ce prototype n'a pas encore de sauvegarde de données ni de système de comptes — c'est normal à ce stade. Le publier avec un domaine officiel le rend visible publiquement ; si tu ne veux pas encore que n'importe qui tombe dessus par hasard, Vercel permet de mettre un mot de passe simple sur le site (Settings → Deployment Protection) le temps des entrevues et de la validation.
