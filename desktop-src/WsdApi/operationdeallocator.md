---
description: Gibt den typdezuweisung an, der von einer vorlagenstub-Funktion verwendet werden soll.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: operationenzuordcator-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c214b5dbc3245f63797c55880fe052d5c3ced15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358923"
---
# <a name="operationdeallocator-element"></a>operationenzuordcator-Element

Gibt den typdezuweisung an, der von der Stub-Funktion eines Vorgangs verwendet werden soll.

## <a name="usage"></a>Verbrauch

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a>Attribute



| Attribut                  | type                         | Erforderlich       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **deallokator**<br/> | Zeichen \_ Folge<br/> | Ja<br/> | Der für den Vorgang zu verwendende dezuweiser.<br/> <br/> Die folgenden Zeichen folgen sind gültige Werte.<br/> <br/> <dl><span id="none"></span><span id="NONE"></span><dt>* * * * keine *</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> * * * <dt>* * * * Wsdfreelinkedmemory * *</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> * * <dt>* * * * CoTaskMemFree * * * *</dt> <span id="free"></span> <span id="FREE"></span> <dt>* * * * Free * * * *</dt> <span id="delete"></span> <span id="DELETE"></span> <dt>* * * * Delete * * * *</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> <dt>* * * * deletearray * * * *</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> <dt>* * * * Release * * *</dt> * </dl> |
| **operation**<br/>   | Zeichen \_ Folge<br/> | Ja<br/> | Der Name des Vorgangs.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                               | BESCHREIBUNG                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubdefinitionen**](stubdefinitions.md)<br/> | Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




