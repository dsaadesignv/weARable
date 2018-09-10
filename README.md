# weARable

## Planning
- Lundi 10 - 10h—17h - KV (+ JB 13-14h)
- Jeudi 13 - 09h—17h - KV @ urbanLab
- Lundi 17 - 09h—17h - KV

## Demande
Concevoir une collection de bijoux et accessoires de mode augmentés.

## Ressources
### Ressources techniques
- VR / WebVR : https://aframe.io/
- AR : https://aframe.io  + AR.js = https://aframe.io/blog/arjs/
- Générateur de _markers_ personnalisés : https://jeromeetienne.github.io/AR.js/three.js/examples/marker-training/examples/generator.html
- Gestion des modèles 3D : https://aframe.io/docs/0.8.0/introduction/models.html
- Blender : https://www.blender.org/
- Export glTF pour Blender : https://github.com/KhronosGroup/glTF-Blender-Exporter ou https://blackthread.io/gltf-converter/

### Références
- Le travail de N O R M A L S : http://mixtur.es/apparel/ + http://normalfutu.re/apparel/a-p-p-a-r-e-l-v-1-0-application/ + http://mixtur.es/category/apparel/?aa=5
![](https://pbs.twimg.com/media/CqBXlvGWAAAIs8J.jpg:large)
- Un article à propos de l'exposition _Extended Bodies_ à la Tate : https://www.tate.org.uk/context-comment/articles/extending-bodies
![](https://www.tate.org.uk/sites/default/files/images/extending-bodies-2.jpg)
- http://barthess.nl/lucyandbart.html
- http://www.curvelive.com/Magazine/Archives/eighteen/A-blushing-dress-and-an-excitable-body-suit
- https://n-e-r-v-o-u-s.com/

## Starter-kit
Ici, vous trouverez plusieurs scripts d'exemple pour démarrer vos projets. Pour tester ces exemples sur votre machine (perso ou au pôle), il faut **configurer un serveur local considéré comme sécurisé**.

_Note : la procédure suivante est valable pour macOS et (à quelques ajustements près) pour Linux._

### Installation
_Note : [Git](https://git-scm.com/downloads) et [Google Chrome](https://www.google.com/chrome/) doivent être installés sur la machine._

1. Ouvrir le Terminal
2. Créer un dossier dans les documents (par exemple) en tapant dans le Terminal **`cd ~/Documents && mkdir dsaa-wearable && cd dsaa-wearable`** puis en appuyant sur **`Entrée`**
3. Maintenant, vous êtes dans votre dossier `dsaa-wearable` fraîchement créé. On va cloner tous les fichiers de ce repo pour que vous ayiez une version locale sur votre machine, que vous pourrez éditer à souhait.
4. Taper dans le Terminal : **`git clone https://github.com/dsaadesignv/weARable.git`** et valider
5. Une fois le téléchargement terminé, vous pouvez constater que vous avez désormais un dossier `weARable` dans votre dossier `dsaa-wearable`, et que vous trouverez tous les fichiers de ce repo dans `weARable`
6. Maintenant, on va installer un outil, [pyhttps](https://github.com/talhasch/pyhttps), permettant de simuler un serveur local sécurisé. Pourquoi ? Pour accéder à la webcam de l'ordinateur ou d'un mobile, il faut désormais avoir un serveur sécurisé par un certificat de sécurité. _pyhttps_ simule un certificat à peu près valide, et permet d'outrepasser cette restriction pour avoir accès au flux de la webcam.
7. Taper dans le Terminal : **`git clone https://github.com/talhasch/pyhttps && cd pyhttps`** et valider
8. Une fois le téléchargement terminé, on va installer l'outil. Taper dans le Terminal : **`sudo python setup.py install`** et valider
9. On va vous demander votre mot de passe administrateur : si vous êtes sur votre machine perso, entrez votre mot de passe qui permet d'ouvrir votre session ; si vous êtes sur une machine du pôle, demandez à JB. Taper le mot de passe puis valider
10. Ça y est, vous avez configuré l'environnement de travail 👍

### Lancer un script
1. Ouvrir le Terminal
2. Se rendre dans le dossier des starter-kits : **`cd ~/Documents/dsaa-wearable/weARable/sk-arjs`** (ou `cd ~/../Shared/DSAA/weARable/sk-arjs` pour ceux qui sont sur une machine du pôle que Kévin a configuré lundi dernier) puis valider
3. Taper dans le Terminal : **`pyhttps`** puis valider
4. La dernière ligne affichée dans le Terminal contiendra le lien vers vos scripts : `https://localhost:4443`. Ouvrir cette URL dans Google Chrome.
5. Voilà, vous avez accès au premier starter-kit 👍
6. Pour afficher les autres starter-kits, ajouter à la fin de l'URL le nom du fichier HTML. Par exemple : `https://localhost:4443/index.html`, `https://localhost:4443/multiple-markers.html`, `https://localhost:4443/model.html`, etc.

### Modifier un script
1. Ouvrir Atom ou tout autre éditeur de code
2. Ouvrir le fichier HTML qui vous intéresse, et qui se trouve dans `~/Documents/dsaa-wearable/weARable/sk-arjs` (ou `~/../Shared/DSAA/weARable/sk-arjs` : vous y trouverez par exemple `index.html` ou `multiple-markers.html` ou `model.html`, etc.
3. Modifier le code à souhait
4. Bien penser à enregistrer (`Cmd + S`)
5. Une fois le code enregistré, retourner dans Google Chrome et recharger l'onglet de la page (`Cmd + R` ou le bouton `Actualiser`)
6. Tadaam 🎉

### Problèmes courants


**Les repos de Github ne se téléchargent pas, et restent bloqués à "Cloning…"** 

👉 Il ne faut pas se mettre sur le réseau du lycée, donc il faut passer par une 4G le temps du téléchargement. Désactiver le proxy du réseau en restant sur le réseau ne suffit pas. De même, si vous passez par une 4G, pensez à désactiver le proxy le temps du téléchargement.

**Je ne peux pas afficher la page sur le réseau du lycée**

👉 Il faut ajouter une exception au proxy : 
1. Ouvrir les Préférences Système
2. Ouvrir `Réseau`
3. Dans la colonne de gauche, cliquer sur le premier moyen de connexion de la liste
4. Vers le bas droit de la fenêtre, cliquer sur "Avancé…"
5. Dans l'onglet "Proxy", trouver le grand champ de texte en bas de la fenêtre
6. Par défaut, il contient deux exceptions séparées par une virgule : `localhost/, xxx/xxx/xxx`
7. Ajouter `, https://localhost:4443` à la suite, pour avoir quelque chose ressemblant à `localhost/, xxx/xxx/xxx, https://localhost:4443`
8. Bien penser à cliquer sur "OK" puis "Appliquer"
9. Recharger la page dans Google Chrome
10. 🎉

**Mon modèle 3D et/ou mes textures ne s'affichent pas**

👉 Vérifiez que l'URL de votre page commence bien par https://localhost:4443 et non pas par `file://`




