# Généralités du logiciel

Il devra être :
* multi-langues
* multi-versions
* multi-plateformes

# Organisation de la base de données

Elle doit tenir compte du fait que :
* le logiciel doit pouvoir gérer plusieurs langues
* le logiciel doit pouvoir gérer les différentes versions du jeu

De plus, pour un affichage plus agréable, il devra être possible de :
* n'afficher que les Grottes, que les Routes ou que les Villes
* en fonction de l'option choisie, afficher la liste des grottes, ou la liste des routes, ou la liste des villes
* pour chaque grotte, ou route, ou ville, afficher la liste des Pokémons que l'on peut y rencontrer

La technologie utilisée pour créer la base de données sera du JSON.

## Hiérarchie des fichiers

/db/
  index.json
  caves/
    index.json
  cities/
    index.json
  roads/
    index.json
    101.json
    102.json

## Fiche pour un Pokémon

Pour chaque fiche d'une zone, il y aura la liste des Pokémons que l'on peut y rencontrer. Pour chaque Pokémon on pourra savoir :
* son numéro d'entrée dans le Pokédex complet
* son nom
* son niveau minimum dans la zone
* son niveau maximum dans la zone
* le nombre de fois où on l'a rencontré (0 par défaut)
* si on peut le croiser par Horde
* si c'est un fuyard (Téléporte, Fuite) ou un crieur (Hurlement/Cyclone)

Exemple pour Zigzaton (route 104) :
```json
{
  [
    {
      "id": 263,
      "name": "Zigzaton",
      "lvlmin": 4,
      "lvlmax": 5,
      "see": 0,
      "horde": "True",
      "flee": "False",
      "cry": "False"
    }
  ]
}
```

# Organisation de l'interface du logiciel

Une grand fenêtre divisée en 4 parties :
* une barre de menu en haut, à l'horizontal
* une barre d'état en bas, à l'horizontal
* une partie de menu de sélection à gauche, à la verticale
* une grande partie d'affichage des données à droite, à la verticale 

## Barre de menu

## Barre d'état

## Menu de sélection

Permet de sélectionner le type de lieu (cave, ville ou route) puis le nom du lieu.

## Affichage des données

Permet d'avoir le visuel des données sur les pokémon en fonction du lieu.

Chaque fiche est affichée l'une sous l'autre.

Pour chaque fiche on doit pouvoir :
* incrémenter de 1 pour chaque rencontre
* si c'est une rencontre par horde, incrémenter de 5 pour chaque horde rencontrée
* proposer également d'additionner au nombre actuel un nombre compté à l'aide d'un compteur
* pouvoir réinitialiser le nombre en un clic. Demander confirmation avant de réinitialiser le nombre.
