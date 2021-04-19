---
description: Generiert C-Konstante Deklarationen für Porttypen.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: porttypeer-Deklarations Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e202f1451d93b519bd59ea51f591c37a92957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345865"
---
# <a name="porttypedeclarations-element"></a>porttypeer-Deklarations Element

Generiert C-Konstante Deklarationen für Porttypen.

## <a name="usage"></a>Verbrauch

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**codeName**](codename.md)<br/>   | Gibt den Namen an, der für den Porttyp im generierten Code verwendet werden soll. Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.<br/> <br/> |
| [**Betriebs**](operation.md)<br/> | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                                                                                          |
| [**PortType**](porttype.md)<br/>   | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Code-Generator aus.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Auf Porttyp Deklarationen wird von der Anwendung und einem Großteil des generierten Codes verwiesen. Dieses Element wird zum Generieren von Include-Dateien verwendet.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




