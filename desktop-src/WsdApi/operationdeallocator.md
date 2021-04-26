---
description: Gibt den Typdelocator an, der von einer Stubfunktion für Vorgänge verwendet werden soll.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: operationDeallocator-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3ae0d9f1d37a478ceca0895806ade6a011747e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994287"
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



| Attribut                  | type                         | Erforderlich       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Deallocator**<br/> | \_Zeichenfolge<br/> | Ja<br/> | Der für den Vorgang zu verwendende Deallocator.<br/> <br/> Die folgenden Zeichenfolgen sind gültige Werte.<br/> <br/> <dl><span id="none"></span><span id="NONE"></span><dt>"None"</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> <dt>"WSDFreeLinkedMemory".</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> <dt>"CoTaskMemFree".</dt> <span id="free"></span> <span id="FREE"></span> <dt>"Free"</dt> <span id="delete"></span> <span id="DELETE"></span> <dt>"delete"</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> <dt>"deleteArray"</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> <dt>"Release"</dt> </dl> |
| **operation**<br/>   | \_Zeichenfolge<br/> | Ja<br/> | Der Name des Vorgangs.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                               | BESCHREIBUNG                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




