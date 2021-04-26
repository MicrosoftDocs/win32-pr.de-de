---
description: Generiert Implementierungen für Proxyfunktionen für Porttypvorgänge.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: proxyFunctionImplementations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9f03834ca59ede41f2f3c3dff00d7dacdd54db
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995757"
---
# <a name="proxyfunctionimplementations-element"></a>proxyFunctionImplementations-Element

Generiert Implementierungen für Proxyfunktionen für Porttypvorgänge.

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
| [**async**](async.md)<br/>           | Gibt an, ob asynchrone Vorgänge in den generierten Proxyfunktionen enthalten sind.<br/> <br/>         |
| [**Ereignisse**](events.md)<br/>         | Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>   | Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierten Funktionen enthalten sind.<br/> <br/> |
| [**Vorgang**](operation.md)<br/>   | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                                        |
| [**Porttype**](porttype.md)<br/>     | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                                       |
| [**proxyClass**](proxyclass.md)<br/> | Gibt den Namen der clientseitigen Proxyklasse an.<br/> <br/>                                               |



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
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




