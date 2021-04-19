---
description: Generiert Deklarationen für Stub-Funktionen für Porttyp Vorgänge.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: Stub-Deklarations Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ceaa8871928031edff90db0491483cfd06bdcc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363812"
---
# <a name="stubdeclarations-element"></a>Stub-Deklarations Element

Generiert Deklarationen für Stub-Funktionen für Porttyp Vorgänge.

## <a name="usage"></a>Verbrauch

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**events**](events.md)<br/>       | Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.<br/> <br/> |
| [**Betriebs**](operation.md)<br/> | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                 |
| [**PortType**](porttype.md)<br/>   | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Code-Generator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




