# Coloriage du Jura

Coloriage à plusieurs au pot de peinture : on choisit une couleur, on touche une zone, elle se
remplit, et tout le monde voit les couleurs arriver en direct, avec les curseurs, les pseudos
des personnes connectées et un tchat.

**Liens à partager :**

- Coloriage du Jura : https://jules125447.github.io/coloriage-jura/
- Libre d'être différents : https://jules125447.github.io/coloriage-jura/#libre
- Miss Ariège : https://jules125447.github.io/coloriage-jura/#ariege

On change de dessin en cliquant sur le titre, en haut à gauche. Chaque dessin a son propre
dessin partagé et son propre tchat. Toute personne qui a le lien peut colorier, sans compte.

Pour un salon à part (un dessin commun rien qu'à vous), ajouter `#nom-du-salon` à l'adresse
pour le Jura, ou `#libre.nom-du-salon` pour l'autre dessin (lettres minuscules, chiffres et
tirets), par exemple `https://jules125447.github.io/coloriage-jura/#libre.famille`.

## Comment ça marche

- `index.html` contient toute la page (les trois dessins et leurs masques de traits intégrés).
- Le partage passe par quatre serveurs MQTT publics et gratuits, sans compte :
  `mqtt.eclipseprojects.io` et `public.cloud.shiftr.io` (port 443, rarement bloqué),
  `broker.emqx.io` et `broker.hivemq.com`. Un navigateur branché sur plusieurs serveurs
  relaie les couleurs et le tchat entre eux. Le panneau de droite indique combien de
  serveurs sont joints. Chaque zone coloriée et l'historique du tchat y sont
  gardés ; la couleur la plus récente gagne. Chaque navigateur garde aussi une copie du dessin
  et la renvoie si un serveur l'a oubliée.
- Ces serveurs sont publics : n'écrivez rien de privé dans le tchat.
- `mqtt.min.js` : [MQTT.js](https://github.com/mqttjs/MQTT.js) 5.10.4, licence MIT.

## Mise en ligne

Settings → Pages → Build and deployment → Source : *Deploy from a branch*,
Branch : `main`, dossier `/ (root)` → Save.
