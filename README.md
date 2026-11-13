# Mini Marché (version GitHub Pages, sans base de données)

Site statique : le catalogue est le fichier `data/produits.json`.

## Mise en ligne

1. Créez un dépôt GitHub (ex. `mini-marche`) et envoyez-y `index.html`, `data/produits.json` et ce README.
2. Dans le dépôt : **Settings → Pages → Build and deployment → Source : Deploy from a branch**, branche `main`, dossier `/ (root)`, puis **Save**.
3. Après une minute, le site est disponible sur `https://VOTRE-NOM.github.io/mini-marche/`.

## Configuration

Dans `index.html`, modifiez en haut du script :

```js
var ADMIN_WA = "22790000000"; // WhatsApp de l'administrateur
```

## Ajouter un produit

1. Le boutiquier remplit l'onglet **Vendre un produit** : un message WhatsApp est envoyé à l'administrateur (avec la photo en pièce jointe).
2. L'administrateur copie le bloc JSON reçu dans la liste `produits` de `data/produits.json` (sur GitHub : ouvrir le fichier → icône crayon → **Commit changes**).
3. Photo : déposez-la dans un dossier `images/` (ex. `images/pagne.jpg`, idéalement < 150 Ko) et renseignez `"image": "images/pagne.jpg"`.
4. Le site se met à jour en 1 à 2 minutes.

## Retirer un produit

Supprimez son bloc dans `data/produits.json` et validez.

## Limites

Sans base de données, les boutiquiers ne peuvent pas publier eux-mêmes en direct : l'administrateur reste le seul à modifier le fichier, ce qui joue aussi le rôle de validation.
