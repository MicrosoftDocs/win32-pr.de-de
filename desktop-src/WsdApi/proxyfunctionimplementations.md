---
description: Generiert Implementierungen für Proxy Funktionen für Porttyp Vorgänge.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: proxyfunctionimplementierungen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a27e217cfa3d0a9efd204a1b18c7b2f0ca16f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867344"
---
# <a name="proxyfunctionimplementations-element"></a>proxyfunctionimplementierungen-Element

Generiert Implementierungen für Proxy Funktionen für Porttyp Vorgänge.

## <a name="usage"></a>Verbrauch

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                     | BESCHREIBUNG                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)<br/>           | Gibt an, ob asynchrone Vorgänge in den generierten Proxy Funktionen enthalten sind.<br/> <br/>         |
| [**Fall**](events.md)<br/>         | Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.<br/> <br/>                        |
| [**faultinfo**](faultinfo.md)<br/>   | Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierte Funktionen eingeschlossen werden<br/> <br/> |
| [**Betriebs**](operation.md)<br/>   | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                                        |
| [**PortType**](porttype.md)<br/>     | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                                       |
| [**proxyClass**](proxyclass.md)<br/> | Gibt den Namen der Client seitigen Proxy Klasse an.<br/> <br/>                                               |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  events?, 
  async?, 
  faultInfo?
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



 

 




