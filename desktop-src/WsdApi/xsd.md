---
description: Gibt eine XSD-Datei an, die für Vertragsinformationen verarbeitet werden soll.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: XSD-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9628a078129446f51729c92c447f8da5736dab88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865336"
---
# <a name="xsd-element"></a>XSD-Element

Gibt eine XSD-Datei an, die für Vertragsinformationen verarbeitet werden soll.

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
| **path**<br/> | Pfadnamen-Zeichenfolge<br/> | Ja<br/> | Die Datei und der Pfad der XSD-Eingabedatei.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                               | BESCHREIBUNG                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [**TypeUri**](typeuri.md)<br/> | Gibt einen Typ an, der aus einer XSD-Datei aufgenommen werden soll.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
typeUri*
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | BESCHREIBUNG                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdcodegen**](wsdcodegen.md)<br/> | Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Die Dateinamen Zeichenfolge sollte auch Informationen zum kompletten Pfad enthalten.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




