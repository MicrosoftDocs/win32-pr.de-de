---
description: Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: stubdefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6676cfc6cf55aa9c9961bd614506500d847def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347620"
---
# <a name="stubdefinitions-element"></a>stubdefinitions-Element

Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.

## <a name="usage"></a>Verbrauch

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                         | BESCHREIBUNG                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**deallokator**](deallocator.md)<br/>                   | Gibt den Typ der dezuweisung an, der von einer stubfunktion verwendet werden soll.<br/> <br/>                                 |
| [**EventArg**](eventarg.md)<br/>                         | Gibt an, ob Verwandte Ereignis Argumente in den generierten Funktionen enthalten sind.<br/> <br/>               |
| [**Fall**](events.md)<br/>                             | Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.<br/> <br/>                        |
| [**faultinfo**](faultinfo.md)<br/>                       | Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierte Funktionen eingeschlossen werden<br/> <br/> |
| [**Betriebs**](operation.md)<br/>                       | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                                        |
| [**operationentzuordcator**](operationdeallocator.md)<br/> | Gibt den Typ der dezuweisung an, der von der Stub-Funktion eines Vorgangs verwendet werden soll.<br/> <br/>                    |
| [**PortType**](porttype.md)<br/>                         | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                                       |
| [**Server Class**](serverclass.md)<br/>                   | Gibt den Namen der Host seitigen Serverklasse an.<br/> <br/>                                                |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
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
| Kann leer bleiben                        | Nein            |



 

 




