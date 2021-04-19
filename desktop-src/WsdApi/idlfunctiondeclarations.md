---
description: Generiert IDL-Deklarationen für Proxy Funktionen für Porttyp Vorgänge.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: idlfunction-Deklarationen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1afa43676898231f739804185b8bf5d6e2b4faf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358816"
---
# <a name="idlfunctiondeclarations-element"></a>idlfunction-Deklarationen-Element

Generiert IDL-Deklarationen für Proxy Funktionen für Porttyp Vorgänge.

## <a name="usage"></a>Verbrauch

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)<br/>         | Gibt an, ob asynchrone Vorgänge in den generierten Proxy Funktionen enthalten sind.<br/> <br/>         |
| [**EventArg**](eventarg.md)<br/>   | Gibt an, ob Verwandte Ereignis Argumente in den generierten Funktionen enthalten sind.<br/> <br/>               |
| [**Fall**](events.md)<br/>       | Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.<br/> <br/>                        |
| [**faultinfo**](faultinfo.md)<br/> | Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierte Funktionen eingeschlossen werden<br/> <br/> |
| [**Betriebs**](operation.md)<br/> | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                                        |
| [**PortType**](porttype.md)<br/>   | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                                       |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
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

Dieses Element generiert Deklarationen von Element Funktionen, die den Vorgängen entsprechen, die durch den Vertrag aufgerufen werden. Diese Deklarationen sind in einer für die Verwendung durch den Mittel l-Compiler geeigneten Form und werden im Allgemeinen in IDL-Dateien verwendet.

Beispiel:

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




