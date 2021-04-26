---
description: Gibt eine XSD-Datei an, die für Vertragsinformationen zu verarbeiten ist.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: xsd-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851ce31230ff88ea2465040c33dc131e0902392c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994547"
---
# <a name="xsd-element"></a>xsd-Element

Gibt eine XSD-Datei an, die für Vertragsinformationen zu verarbeiten ist.

## <a name="usage"></a>Verbrauch

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a>Attribute



| Attribut           | type                       | Erforderlich       | BESCHREIBUNG                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| **path**<br/> | pathname string<br/> | Ja<br/> | Datei und Pfad der XSD-Eingabedatei.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                               | BESCHREIBUNG                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [**typeUri**](typeuri.md)<br/> | Gibt einen Typ an, der aus einer XSD-Datei enthalten sein soll.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
typeUri*
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | BESCHREIBUNG                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Das Stammelement einer XML-Skriptdatei des WSDAPI-Codegenerators.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Die Dateinamenzeichenfolge sollte auch vollständige Pfadinformationen enthalten.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




