# hacknet-xsd

XML schemas for [Hacknet](http://hacknet-os.com/) modding files.

These are valid for patch v5.067 released on 2017-06-04.

## Usage

When used with an IDE, it allows for auto-completion, integrated documentation and quick validation.

### ExtensionInfo.xml

```xml
<HacknetExtension xmlns="http://hacknet-os.com" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  
xsi:schemaLocation="http://hacknet-os.com https://raw.githubusercontent.com/rquinio/hacknet-xsd/master/Nodes.xsd">
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