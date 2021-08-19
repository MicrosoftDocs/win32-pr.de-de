---
description: Gibt den Typdelocator an, der von einer Operations-Stubfunktion verwendet werden soll.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: operationDeallocator-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ce2902bbfac16cb096da334cf3f22a12c68e3720d575fa303b8f3b133c9328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991690"
---
# <a name="operationdeallocator-element"></a>operationDeallocator-Element

Gibt den Typdelocator an, der von der Stubfunktion eines Vorgangs verwendet werden soll.

## <a name="usage"></a>Verbrauch

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a>Attribute



| attribute                  | type                         | Erforderlich       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **deallocator**<br/> | Zeichenfolge \_<br/> | Ja<br/> | Der für den Vorgang zu verwendende Zuordnungsvorgang.<br/> <br/> Die folgenden Zeichenfolgen sind gültige Werte.<br/> <br/> <dl><span id="none"></span><span id="NONE"></span><dt>"none"</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> <dt>"WSDFreeLinkedMemory"</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> <dt>"CoTaskMemFree"</dt> <span id="free"></span> <span id="FREE"></span> <dt>"free"</dt> <span id="delete"></span> <span id="DELETE"></span> <dt>"delete"</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> <dt>"deleteArray"</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> <dt>"Release"</dt> </dl> |
| **operation**<br/>   | Zeichenfolge \_<br/> | Ja<br/> | Der Name des Vorgangs.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                               | Beschreibung                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




