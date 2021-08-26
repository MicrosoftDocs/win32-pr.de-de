---
description: Gibt eine XSD-Datei an, die für Vertragsinformationen zu verarbeiten ist.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: xsd-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f790375c34a4d5afc3dc345691c8e26e5f95cebe0bbde283e2986e838cce554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995090"
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



| attribute           | type                       | Erforderlich       | BESCHREIBUNG                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| **path**<br/> | pathname string<br/> | Ja<br/> | Datei und Pfad der XSD-Eingabedatei.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                               | Beschreibung                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [**typeUri**](typeuri.md)<br/> | Gibt einen Typ an, der aus einer XSD-Datei enthalten sein soll.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
typeUri*
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | Beschreibung                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Das Stammelement einer XML-Skriptdatei des WSDAPI-Codegenerators.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Die Dateinamenzeichenfolge sollte auch vollständige Pfadinformationen enthalten.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




