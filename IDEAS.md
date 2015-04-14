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
      id: 263,
      name: "Zigzaton",
      lvlmin: 4,
      lvlmax: 5,
      see: 0,
      horde: True,
      flee: False,
      cry: False,
    },
  ]
}
```

# Organisation de l'interface du logiciel
