# helias-constructions

*L'icon ci-dessous indique si le déploiement du site à marché ou non.*

[![helias-constructions](https://circleci.com/gh/Dauliac/helias-constructions.svg?style=svg)](https://helias-constructions.com/)

## Rédaction page principale
Pour la rédaction des différentes zones de textes, il faut écrire dans les guillemets `""`

Pour obtenir du gras: entourer le texte de **deux astériques**: `**En gras**`.

Pour l'*italique* ça sera d'une seule. `*En italique*`

Pour la rédaction de nouveau billet de blog, il faut créer un ficher dans le dossier [`content/monbilletdeblog.md`](./content/) (le `.md` étant simplement l'extention du fichier.)

Il faudra ajouter en début de fichier ce bloc de text en raplacant les différents champs par les informations y correspondant:
```markdown
---
title: "Titre du billet de blog"
date: 2019-12-12T04:28:21+06:00
image: images/blog/ecurie.jpg
description: "Description du billet de blog"
type: "post"
---
```

Le champ `image: ` étant un peu spécial car il correspond au chemin de la miniature du billet de blog.

Libre à vous d'ajouter une belle photo à cet enplaçement ou de réutiliser une photo existante.


La suite est écrite suivant une syntaxe markdown,
