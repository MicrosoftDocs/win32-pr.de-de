---
description: Generiert Implementierungs Deklarationen für Proxy Funktionen für Porttyp Vorgänge.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: functiondeklarationen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82aca30f94fc8fcec80701a74b56e83ab674c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216168"
---
# <a name="functiondeclarations-element"></a>functiondeklarationen-Element

Generiert Implementierungs Deklarationen für Proxy Funktionen für Porttyp Vorgänge.

## <a name="usage"></a>Verbrauch

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)<br/>         | Gibt an, ob asynchrone Vorgänge in den generierten Proxy Funktionen enthalten sind.<br/> <br/>         |
| [**Fall**](events.md)<br/>       | Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.<br/> <br/>                        |
| [**faultinfo**](faultinfo.md)<br/> | Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierte Funktionen eingeschlossen werden<br/> <br/> |
| [**Betriebs**](operation.md)<br/> | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                                        |
| [**PortType**](porttype.md)<br/>   | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                                       |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Code-Generator aus.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Element generiert Deklarationen von Element Funktionen, die den Vorgängen entsprechen, die durch den Vertrag aufgerufen werden. Diese Deklarationen sind in einer für die Verwendung durch einen C++-Compiler geeigneten Form und werden im Allgemeinen in cpp-Dateien verwendet.

Beispiel:

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




