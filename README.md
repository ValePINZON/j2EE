# j2EE

salut, essaie ce type de mapping, cela aide a fetch la bonne colonne de table, tiens moi au courant

@ManyToMany(cascade = CascadeType.ALL)
@JoinTable(name = "business_vendor",
        joinColumns = @JoinColumn(name = "business_id"**, referencedColumnName = "enter business Id name"**),
        inverseJoinColumns = @JoinColumn(name = "vendor_id", **referencedColumnName = "enter vendor Id name"** ))
@JSON(include = false)
protected List<Vendor> vendors;

**OR** 

@ManyToMany(cascade = CascadeType.ALL)
@JoinTable(name = "business_vendor",
        joinColumns = @JoinColumn(**name = "tablename_idname"**),
        inverseJoinColumns = @JoinColumn(**name = "tablename_idname"**))
@JSON(include = false)
protected List<Vendor> vendors;
