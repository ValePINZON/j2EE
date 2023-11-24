# j2EE

salut, essaie ce type de mapping, cela aide a fetch la bonne colonne de table, tiens moi au courant. si le "referencedColumnName" n'est pas spécifié, hibernate cherche a réconcilier la colonne depuis le nom de la colonne de la table "associea" donc "codem" et comme la colonne équivalente ne porte pas le même nom dans la table "monument", il n'y arrive pas.

@ManyToMany(cascade = CascadeType.ALL)
@JoinTable(name = "associea",
        joinColumns = @JoinColumn(name = "celebrite"**, referencedColumnName = "celebriteID"**),
        inverseJoinColumns = @JoinColumn(name = "codem", **referencedColumnName = "hashcode"** ))
@JSON(include = false)
protected List<monument> monumentsVisite;

