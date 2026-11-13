# CleanSkeen — maquette complète pour le thème FullStack

Ce dossier contient uniquement des **fichiers à ajouter** à votre thème (rien de votre thème d'origine n'est modifié, sauf `templates/index.json`, qui remplace la home).

## Installation (15 minutes)

1. **Dupliquez votre thème** : Boutique en ligne → Thèmes → ⋯ → Dupliquer. Travaillez uniquement sur la copie.
2. Sur la copie : ⋯ → **Modifier le code**.
3. Ajoutez les fichiers, dans les mêmes dossiers :
   - `assets/` : `cs-base.css`, `cs-products.js`
   - `snippets/` : `cs-stars.liquid`, `cs-arrow.liquid`
   - `sections/` : les 12 fichiers `cs-*.liquid`
   - `templates/` : `product.cleanskeen-v2.json` (nouveau) et `index.json` (**remplace** votre home actuelle)
4. **Home** : ouvrez l'éditeur de thème, page d'accueil. Les sections apparaissent avec les textes de la maquette.
5. **Fiche produit** : Produits → Le masque LED → colonne « Modèle de thème » → choisissez `cleanskeen-v2`. Ouvrez-la ensuite dans l'éditeur.

## Ce que vous devez renseigner dans l'éditeur

**Images** (la maquette est un PDF aplati, je n'ai pas pu en extraire les photos) :
- Home : photo du hero, photo du masque sur fond blanc (longueurs d'onde), 6 paires avant/après, photo « toutes les peaux ».
- Fiche produit : 3 paires avant/après, photo du contenu de la boîte.
- Les cartes produit prennent automatiquement la photo principale de chaque produit.

**Produits** : la home et le bas de la fiche pointent vers `masque-led-visage`, `masque-anti-age` et `stylo-de-soins-anti-cernes` (adresses relevées sur votre site). Si l'une a changé, rechoisissez le produit dans le bloc concerné.

**Couleurs** : toutes les couleurs sont en haut de `assets/cs-base.css` (variables `--cs-*`). Les couleurs des 7 longueurs d'onde se changent dans l'éditeur.

## À vérifier avant de publier (contenu)

- **Longueurs d'onde (nm)** : seul le rouge (630 à 660 nm) vient de la maquette. Les six autres sont vides : renseignez-les d'après la fiche du fabricant.
- **Descriptions des 7 couleurs** : rédigées par moi (la maquette n'en donnait qu'une), volontairement prudentes. À relire.
- **« Ce qu'il traite »** : j'ai adouci trois formulations de la maquette (« réduction des bactéries responsables des éruptions » → « aide à apaiser l'aspect… », « atténuation visible de l'hyperpigmentation » → « aide à atténuer l'apparence… »).
- **Section « Avis d'experts »** : présente mais **désactivée**. Les citations de dermatologues doivent être exactes et sourcées (champ « Lien vers la source »). Activez-la seulement une fois vérifiées.
- **Chiffres** : « 4 000+ clientes » et le prix barré 139,98 € viennent de la maquette. Assurez-vous qu'ils sont justifiables.
- **Photos avant/après** : n'utilisez que des photos de clientes ayant donné leur accord.

## Pages ajoutées dans cette 2ᵉ livraison

Fichiers en plus : `assets/cs-pages.css`, `snippets/cs-icon.liquid`, 14 sections `cs-*` (annonce, pied de page, collection, comparatif, par objectif, réassurance, colonnes de texte, haut de page, image + texte, déclaration + chiffres, cartes, appel à l'action, journal, lettre d'information, article).

**Modèles alternatifs** (à assigner dans l'admin, rien n'est écrasé) :
- `collection.cleanskeen` : Produits → Collections → votre collection → « Modèle de thème ». Les filtres du haut sont des liens vers vos collections (à adapter dans l'éditeur). Les badges « Best-seller » / « Nouveau » s'affichent si le produit a le tag `best-seller` / `nouveau`.
- `page.notre-histoire` : correspond à la page 4 de la maquette (titre « La science derrière la beauté », menu « Notre histoire »). Pages → « Notre histoire » → Modèle de thème. Ajoutez la photo du haut et celle « Notre approche ». La maquette n'a pas de page « La science » distincte : si vous gardez ce lien dans le menu, réutilisez ce modèle ou votre page existante.
- `blog.cleanskeen` : Boutique en ligne → Blogs → modèle du blog. Le 1er article est mis à la une, les filtres viennent des tags des articles, le temps de lecture est calculé (≈ 200 mots/min).
- `article.cleanskeen` : même endroit, modèle des articles. Le sommaire se construit tout seul à partir des titres de niveau 2 (H2) de l'article. L'image de couverture est celle de l'article.

**Header et footer** — `sections/header-group.json` et `sections/footer-group.json` **remplacent** ceux de votre thème (sauvegardez-les avant, ou faites-le sur la copie du thème) :
- Header : le bandeau d'annonce du thème est remplacé par `CS · Bandeau d'annonce` (4 messages fixes sur ordinateur, défilants sur mobile). Votre header du thème est conservé tel quel (logo, menu, panier, recherche) avec son fond rose existant. **Les deux bandeaux défilants (marquee) sous le header ne sont plus dans le groupe** : ajoutez-les à nouveau si vous les voulez.
- Footer : remplacé par `CS · Pied de page` (lettre d'information, 3 colonnes de liens saisies en « Libellé | /adresse », barre légale, moyens de paiement activés dans votre boutique). **Le bloc de 4 réassurances noires du thème en haut du footer n'est plus là.** Le grand « CLEANSKEEN » est du texte ; vous pouvez mettre votre logo (image) à la place.
- Les liens par défaut (Notre histoire, Avis clientes, FAQ, Suivi…) sont des adresses supposées : corrigez-les.

**Pas de fond crème pour le header** : cela demande d'ajouter un jeu de couleurs dans Paramètres du thème → Couleurs (je n'ai pas touché à `settings_data.json`). Créez un jeu « crème » (#faf6f1 / texte #140e0d) et sélectionnez-le dans la section Header.

**À renseigner** : photos (collection : aucune, elles viennent des produits ; objectifs : 4 photos ; science : 2), liens des filtres et des cartes « objectif », textes de l'article (CTA), liens de la lettre d'information (inscription = abonnés e-mail Shopify avec le tag `newsletter`).

## Pages secondaires (3ᵉ livraison)

Deux modèles supplémentaires hors maquette, à assigner dans Pages → la page → Modèle de thème : `page.faq` et `page.avis` (créez ces pages si elles n'existent pas, avec les adresses `/pages/notre-histoire`, `/pages/faq`, `/pages/avis` utilisées dans le footer).

- **FAQ** : 7 questions reprenant uniquement ce qui figure dans la maquette (livraison 8 à 11 jours ouvrés, 30 jours, paiements, service client lundi au samedi 8 h à 20 h). Vérifiez-les ; la question sur les contre-indications est volontairement prudente.
- **Avis clientes** : reprend les avis et photos avant/après de la home. N'utilisez que de vrais avis et des photos de clientes consentantes.
- La page Contact et le suivi de commande restent ceux de votre thème (`page.contact` existe déjà).

## Correspondance avec la maquette (PDF)

- **Pages 1 + 2 = home** (`templates/index.json`) : hero, bandeau, cartes, longueurs d'onde, résultats, chronologie, peaux, avis, experts (page 1), puis « Tous nos soins LED », « Quel soin choisir ? », « Quel est votre objectif ? », réassurance et « Bon à savoir » (page 2). Les filtres cliquables de la page 2 n'existent que sur le modèle collection ; sur la home, les 3 produits sont affichés sans filtres. La section Experts est maintenant activée : vérifiez que chaque citation est exacte et sourcée.
- **Page 3 = fiche produit** : modèle `cleanskeen-v2` du masque LED.
- **Page 4 = Notre histoire** : modèle `page.notre-histoire`.
- **Pages 5 + 6 = Le journal** : modèles `blog.cleanskeen` (liste) et `article.cleanskeen` (article, avec « À lire aussi »). Dans le dossier `contenu-a-copier/` : le texte complet de l'article de la maquette (HTML à coller dans l'article) et la liste des 7 articles du journal (titres, tags, extraits).

## Option : fond crème du header (dossier `optionnel-fond-creme/`)

Contient `config/settings_data.json` (votre fichier avec un jeu de couleurs « crème » ajouté) et `sections/header-group.json` (header utilisant ce jeu). **Attention : `settings_data.json` contient tous vos réglages de thème au moment de l'export.** Ne l'installez que sur la copie du thème, et si vous avez changé des réglages depuis, ne l'utilisez pas : créez plutôt le jeu à la main (Paramètres du thème → Couleurs → ajouter un jeu : fond #faf6f1, texte #140e0d, boutons #140e0d) puis choisissez-le dans la section Header. Si vous installez seulement le `header-group.json` crème sans le jeu de couleurs, le header reprend la couleur par défaut.

## Non inclus

Les pages dont je n'ai ni maquette ni contenu (mentions légales, CGV, suivi de commande).

## Comment ça a été vérifié

Contrôle Theme Check de Shopify (0 alerte sur ces fichiers), conformité des modèles aux schémas des sections, rendu local desktop et mobile (collection, science, journal, article, header, footer compris). **Je n'ai pas pu tester dans une vraie boutique Shopify** : testez sur la copie du thème (panier, tiroir panier, variantes) avant de publier.
