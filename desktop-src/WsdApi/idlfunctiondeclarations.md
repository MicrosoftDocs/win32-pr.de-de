---
description: Generiert IDL-Deklarationen für Proxyfunktionen für Porttypvorgänge.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: idlFunctionDeclarations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f4bc12f0269e79142a4e55ad0cdc252b88b01959f6d18a6d4a4b5a8e72cde6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311732"
---
# <a name="idlfunctiondeclarations-element"></a>idlFunctionDeclarations-Element

Generiert IDL-Deklarationen für Proxyfunktionen für Porttypvorgänge.

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
| [**Asynchrone**](async.md)<br/>         | Gibt an, ob asynchrone Vorgänge in den generierten Proxyfunktionen enthalten sind.<br/> <br/>         |
| [**eventArg**](eventarg.md)<br/>   | Gibt an, ob verwandte Ereignisargumente in den generierten Funktionen enthalten sind.<br/> <br/>               |
| [**Ereignisse**](events.md)<br/>       | Gibt an, ob verknüpfte Ereignisse in den generierten Funktionen enthalten sind.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/> | Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierten Funktionen enthalten sind.<br/> <br/> |
| [**Vorgang**](operation.md)<br/> | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                                        |
| [**Porttype**](porttype.md)<br/>   | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                                       |



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
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Element generiert Deklarationen von Memberfunktionen, die den vom Vertrag aufgerufenen Vorgängen entsprechen. Diese Deklarationen sind in einer Form enthalten, die für die Verwendung durch den MIDL-Compiler geeignet ist und in der Regel in IDL-Dateien verwendet werden.

Beispiel:

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




