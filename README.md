# Simulateur de cadenas

Le propriétaire d'un cadenas à chiffres ne change jamais le code. Chaque jour, il l'ouvre puis le referme en tournant les roues, toujours un peu de la même façon. En relevant simplement les chiffres affichés quand le cadenas est fermé, peut-on retrouver le code ?

Ce simulateur montre que oui.

**En ligne :** https://nicomeynet.github.io/cadenas-simulator/

## Ce que montre la page

- **Le cadenas** affiche les chiffres du jour, une fois refermé.
- **Codes les plus probables :** tous les codes classés selon leur probabilité d'être le bon, calculée à partir des seuls relevés. Après « Dévoiler le code », le vrai code est surligné en vert.
- **Évolution jour après jour :** pour chaque roue, les chiffres qu'on voit sortir (en bleu) et la probabilité que chaque chiffre soit le bon (en vert), avec une courbe de confiance.
- **Coulisses :** l'habitude réelle du propriétaire (sens de rotation, nombre de crans, tours complets, gestes inhabituels). Elle est tirée au hasard à chaque nouveau code, et l'observateur ne la connaît pas.

## Comment le code est deviné

Pour chaque habitude possible (vers le haut, vers le bas ou dans les deux sens, avec n'importe quelle plage de crans), le simulateur cherche le code qui explique le mieux les relevés. Il suppose seulement que l'habitude est la même sur toutes les roues et que les petits tours sont plus courants que les grands.

Les rares jours où le propriétaire retombe sur le bon chiffre (tour complet, oubli) laissent un petit pic juste à côté des chiffres fréquents. C'est ce pic qui permet de trancher entre des codes décalés qui expliqueraient sinon aussi bien les relevés.

## Utilisation

Tout tient dans un seul fichier, `index.html`, sans dépendance : il suffit de l'ouvrir dans un navigateur. La page existe en français et en anglais (bouton FR / EN en haut, ou `?lang=en` dans l'adresse).

## In English

A combination lock's owner never changes the code, but scrambles the wheels the same way every time they close it. This page shows that the code can be worked out from the digits seen on the closed lock, day after day, without knowing anything about the owner's habit. Switch to English with the FR / EN button, or open https://nicomeynet.github.io/cadenas-simulator/?lang=en

© 2026 Nicolas Meynet
