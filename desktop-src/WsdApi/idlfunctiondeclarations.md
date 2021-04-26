---
description: Generiert IDL-Deklarationen für Proxyfunktionen für Porttypvorgänge.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: idlFunctionDeclarations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf4d1648ac6d9c3ac6900826ebe90a64418822b6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994737"
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
| [**async**](async.md)<br/>         | Gibt an, ob asynchrone Vorgänge in den generierten Proxyfunktionen enthalten sind.<br/> <br/>         |
| [**eventArg**](eventarg.md)<br/>   | Gibt an, ob verwandte Ereignisargumente in den generierten Funktionen enthalten sind.<br/> <br/>               |
| [**Ereignisse**](events.md)<br/>       | Gibt an, ob verwandte Ereignisse in den generierten Funktionen enthalten sind.<br/> <br/>                        |
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

Dieses Element generiert Deklarationen von Memberfunktionen, die vorgängen entsprechen, die vom Vertrag aufgerufen werden. Diese Deklarationen sind in einer Für den MIDL-Compiler geeigneten Form und werden im Allgemeinen in IDL-Dateien verwendet.

Beispiel:

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




