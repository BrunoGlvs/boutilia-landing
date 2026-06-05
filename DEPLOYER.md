# Comment déployer ta landing en 10 min

## Étape 1 — Tester en local (1 min)

Ouvre `index.html` dans ton navigateur (double-clic).
→ Tu vois ta landing fonctionner. Le formulaire ne marche pas encore (étape 2).

## Étape 2 — Créer le formulaire Tally (3 min)

1. Va sur [tally.so](https://tally.so) → crée un compte (gratuit, illimité)
2. **Create a new form** → choisis "From scratch"
3. Crée un formulaire avec ces champs :
   - **Email** (Short answer, required)
   - **Nom de ta boutique** (Short answer)
   - **URL Shopify** (Short answer)
   - **CA mensuel approximatif** (Multiple choice : "< 5K€", "5K-25K€", "25K-100K€", "> 100K€")
   - **Ton plus gros défi côté data ?** (Long answer)
4. **Publish** → onglet **Share** → onglet **Embed**
5. Copie l'URL d'embed (format : `https://tally.so/embed/XXXXXX?...`)
6. Dans `index.html`, ligne avec `data-tally-src` → remplace `REMPLACE_PAR_TON_ID_TALLY` par ton ID Tally

## Étape 3 — Déployer en ligne sur GitHub Pages (5 min, gratuit)

### 3a. Crée un repo GitHub
1. [github.com](https://github.com) → New repository
2. Nom : `pilote-landing` (ou ce que tu veux)
3. Public · Sans README
4. Create

### 3b. Push ton code (depuis le dossier landing_pilote)
```bash
cd "H:\Desktop\Projets\BOS-main\Output\landing_pilote"
git init
git add .
git commit -m "Initial landing"
git branch -M main
git remote add origin https://github.com/TON_USERNAME/pilote-landing.git
git push -u origin main
```

### 3c. Active GitHub Pages
1. Dans ton repo GitHub → Settings → Pages
2. Source : `Deploy from a branch`
3. Branch : `main`, folder : `/ (root)`
4. Save

Attends 1-2 min. Ton site est en ligne sur :
**https://TON_USERNAME.github.io/pilote-landing/**

## Étape 4 — Domaine custom (optionnel, 10-15€/an)

Pour avoir `pilote.app` ou `pilote.fr` au lieu de `*.github.io` :
1. Achète un domaine sur [namecheap.com](https://www.namecheap.com) ou [ovh.fr](https://www.ovh.com)
2. Dans GitHub Pages → Custom domain → ajoute ton domaine
3. Configure les DNS chez ton registrar (instructions GitHub te seront données)

Pas urgent pour valider le marché. Le `.github.io` suffit pour les 20 premiers tests.

## Étape 5 — Tester sur mobile

Ouvre ton URL sur ton téléphone. Vérifie que tout est lisible.

## Notes

- Tally te notifiera par email à chaque nouvelle inscription
- Tu peux aussi voir toutes les soumissions dans le dashboard Tally
- Tu peux modifier la landing à tout moment, push GitHub, et le site se met à jour en 1 min

## Quand tu auras 10-20 inscrits, tu pourras dire :

> *"On a 20+ e-commerçants français qui veulent ce produit avant même qu'il existe.
> Maintenant on construit le MVP."*

→ C'est le feu vert pour 6 semaines de dev.
