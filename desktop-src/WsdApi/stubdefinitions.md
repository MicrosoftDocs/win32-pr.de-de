---
description: Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: stubDefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42c60b071c901538122751f6e92cfd7049f7be88
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994687"
---
# <a name="stubdefinitions-element"></a>stubDefinitions-Element

Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.

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
| [**Deallocator**](deallocator.md)<br/>                   | Gibt den Typ des Deallocators an, der von einer Stubfunktion verwendet werden soll.<br/> <br/>                                 |
| [**eventArg**](eventarg.md)<br/>                         | Gibt an, ob verwandte Ereignisargumente in den generierten Funktionen enthalten sind.<br/> <br/>               |
| [**Ereignisse**](events.md)<br/>                             | Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>                       | Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierten Funktionen enthalten sind.<br/> <br/> |
| [**Vorgang**](operation.md)<br/>                       | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                                        |
| [**operationDeallocator**](operationdeallocator.md)<br/> | Gibt den Typ des Deallocators an, der von der Stubfunktion eines Vorgangs verwendet werden soll.<br/> <br/>                    |
| [**Porttype**](porttype.md)<br/>                         | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                                       |
| [**serverClass**](serverclass.md)<br/>                   | Gibt den Namen der hostseitigen Serverklasse an.<br/> <br/>                                                |



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
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




