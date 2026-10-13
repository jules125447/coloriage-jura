# Coloriage du Jura

Coloriage à plusieurs au pot de peinture : on choisit une couleur, on touche une zone, elle se
remplit, et tout le monde voit les couleurs arriver en direct, avec les curseurs, les pseudos
des personnes connectées et un tchat.

**Lien à partager :** https://jules125447.github.io/coloriage-jura/

Toute personne qui a le lien peut colorier, sans compte. Pour un dessin séparé, ajouter
`#nom-du-salon` à la fin de l'adresse (lettres minuscules, chiffres et tirets), par exemple
`https://jules125447.github.io/coloriage-jura/#famille`.

## Comment ça marche

- `index.html` contient toute la page (dessin et masque des traits intégrés).
- Le partage passe par deux serveurs MQTT publics et gratuits (`broker.emqx.io` et
  `broker.hivemq.com`), sans compte. Chaque zone coloriée et l'historique du tchat y sont
  gardés ; la couleur la plus récente gagne. Chaque navigateur garde aussi une copie du dessin
  et la renvoie si un serveur l'a oubliée.
- Ces serveurs sont publics : n'écrivez rien de privé dans le tchat.
- `mqtt.min.js` : [MQTT.js](https://github.com/mqttjs/MQTT.js) 5.10.4, licence MIT.

## Mise en ligne

Settings → Pages → Build and deployment → Source : *Deploy from a branch*,
Branch : `main`, dossier `/ (root)` → Save.
