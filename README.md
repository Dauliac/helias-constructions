# helias-constructions
[lien du site: https://helias-constructions.com](http://helias-constructions.com/)

*L'icon ci-dessous indique si le déploiement du site à marché ou non.*

[![helias-constructions](https://circleci.com/gh/Dauliac/helias-constructions.svg?style=svg)](https://helias-constructions.com/)

## Structure du projet
On distingue 2 entités distincte pour définir le site web:
- La page d'accueil soit [https://helias-constructions.com/](https://helias-constructions.com/)
- Les billets de blogs présent dans la section: "Nos derniers ouvrages" par exemple: [https://helias-constructions.com/notre-ecurie/](https://helias-constructions.com/notre-ecurie/).

Ces 2 entités sont configurés dans 2 dossier distinct:
- `data/homepage.yml` pour la page d'accueil.
- `content/mon-billet.md` pour les billets de blog.


La page d'acceuil suit une syntaxe
## Rédaction
Les fichiers s'écrient dans un language appelé le markdown, il est très simple à prendre en main et permet de faire de la mise en forme sans efforts !

Pour la rédaction des différentes zones de textes, il faut écrire dans les guillemets `""`

Pour obtenir du gras: entourer le texte de **deux astériques**: `**En gras**`.

Pour l'*italique* ça sera d'une seule. `*En italique*`

Il existe également des editeurs markdown, qui affichent le rendu en temps réél, voici par exemple [typora](https://typora.io/#download)
Il vous suffira de l'installer, d'écrire dessus, puis de copier coller le contenu sur votre fichier de billet de blog sur github.

## Nouveau billet de blog
Pour la rédaction de nouveau billet de blog, il faut créer un ficher dans le dossier [`content/monbilletdeblog.md`](./content/) (le `.md` pour markdown étant simplement l'extention du fichier.)

Pour ce faire, il faut appuyer sur le bouton: `creating file` ou en cliquant sur [ce lien](https://github.com/Dauliac/helias-constructions/new/master).

N'oubliez pas de spécifier le chemin/nom du fichier, par exemple:  `content/construction-piscine.md`

**Note**: évitez les caractères spéciaux/espaces dans les noms de fichiers !

### En tete du billet
Il faut un petit bout de "code" en début de fichier qui ne sera pas affiché sur le site affin de préciser le Titre de l'article, la date, le chemin de la miniature (dans le dossier `public/images/blog/`)
Il faudra ajouter en début de fichier ce bloc de texte en remplaçant les différents champs par les informations y correspondant:
```markdown
---
title: "Titre du billet de blog"
date: 2019-12-13
image: images/blog/ecurie.jpg
description: "Description du billet de blog"
type: "post"
---
```

Le champ `image: ` étant un peu spécial, car il correspond au chemin du fichier de la miniature du billet de blog dans [`public/images/blog`](./public/images/blog/)

**Note**: Ce champ est obligatoire pour

Libre à vous d'ajouter une belle photo à cet emplaçement, ou de réutiliser une photo existante dans `public/images/blog/ma-piscine.png` par exemple

**Astuce:** Vous pouvez ajouter une ligne `draft: true` pour préciser que le billet que vous écrivez pour sauvegarder votre travail sur github mais pour ne pas le publier sur internet:

```markdown
---
title: "Titre du billet de blog"
date: 2019-12-13
image: images/blog/ecurie.jpg
description: "Description du billet de blog"
type: "post"
draft: true
---
```

### le contenu du billet de blog
La suite est écrite suivant notre fameuse syntaxe markdown, voici un petit exemple (n'hésitez pas à le copier coller dans [typora](https://typora.io/#download) pour voir le rendu, vous ne vérez cependant pas les rendus d'images):

```makdown
# Construction d'une piscine

Voici un parfait exemple d'aménagement extérieur que nous sommes capables de produire.

[description de l 'image](ma-piscine.png)

## Titre 2
BLABLABLA

###  Sous titre 3
Ceci est un exemple:
- exemple 1
- exemple 2
- exemple 3

## Titre 3

Fin de l'article

```

## Déployer le site
Le site se construit automatiquement à chaque commit et vient se mettre à jour tout seul.
Si le déploiement marche, ce badge présent plus haut doit être vert: [![helias-constructions](https://circleci.com/gh/Dauliac/helias-constructions.svg?style=svg)](https://helias-constructions.com/)

L'avantage de cette méthode est qu'elle limite les actions de mise à jour, ou de sécurisation du site.

