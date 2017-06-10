# hacknet-xsd

XML schemas for [Hacknet](http://hacknet-os.com/) modding files.

These are valid for patch v5.067 released on 2017-06-04.

## Editor support

Basic text editors merely do simple syntax coloring or expanding and collapsing of nodes.
When used with an [XML editor](https://en.wikipedia.org/wiki/Comparison_of_XML_editors), an XML schema allows for:
* XML tag auto-completion
* integrated documentation when hover tags and attributes
* validation from the schema.

| Editor | Auto-completion | Documentation | Validation | Notes
|---|---|---|---|---|
| Notepad++ XML tools plugin | No | No | Yes, but need to copy the .xsd locally, as referencing via http:// doesn't seem to work  | See [http://when-others-then-null.blogspot.fr/2012/12/Validate-XML-against-an-XSD-using-npp.html](article).
| Eclipse | Yes | Yes | Yes | Can validate the whole extension via Right-click/Validate on folders |

## Usage

Add the attributes "xmlns", "xmlns:xsi" and "xsi:schemaLocation" to the root XML tag, in order to specify the XML schema to use for validation.

### ExtensionInfo.xml

```xml
<HacknetExtension xmlns="http://hacknet-os.com" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  
xsi:schemaLocation="http://hacknet-os.com https://raw.githubusercontent.com/rquinio/hacknet-xsd/master/ExtensionInfo.xsd">
```

### Nodes

```xml
<Computer xmlns="http://hacknet-os.com" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:schemaLocation="http://hacknet-os.com https://raw.githubusercontent.com/rquinio/hacknet-xsd/master/Nodes.xsd">
```

### ConditionalActions

```xml
<ConditionalActions xmlns="http://hacknet-os.com" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:schemaLocation="http://hacknet-os.com https://raw.githubusercontent.com/rquinio/hacknet-xsd/master/ConditionalActions.xsd">
```

### Missions

```xml
<mission xmlns="http://hacknet-os.com" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:schemaLocation="http://hacknet-os.com https://raw.githubusercontent.com/rquinio/hacknet-xsd/master/Missions.xsd">
```

### Factions

```xml
<CustomFaction xmlns="http://hacknet-os.com" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:schemaLocation="http://hacknet-os.com https://raw.githubusercontent.com/rquinio/hacknet-xsd/master/Factions.xsd">
```

### People

```xml
<Person xmlns="http://hacknet-os.com" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:schemaLocation="http://hacknet-os.com https://raw.githubusercontent.com/rquinio/hacknet-xsd/master/People.xsd">
```

### Themes

```xml
<CustomTheme xmlns="http://hacknet-os.com" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:schemaLocation="http://hacknet-os.com https://raw.githubusercontent.com/rquinio/hacknet-xsd/master/Themes.xsd">
```

## Limitations

* The order of elements in files (especially <Computer>) is stricter than what the game allows. This is due to XSD 1.0 limitation regarding xs:all. XSD 1.1 would solve that, but it is not widely supported yet.