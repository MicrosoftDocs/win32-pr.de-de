---
description: Gibt den Typ des Deallocators an, der von einer Stubfunktion verwendet werden soll.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: deallocator-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e9a27f768d0c9d854d13bd58c0c797234a0526c4abb95a0c5f4fb553466a6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991750"
---
# <a name="deallocator-element"></a>deallocator-Element

Gibt den Typ des Deallocators an, der von einer Stubfunktion verwendet werden soll.

## <a name="usage"></a>Verbrauch

``` syntax
<deallocator/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                               | BESCHREIBUNG                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Der Deallocatortyp sollte in ein Tagpaar eingeschlossen <deallocator></deallocator> werden. Die folgenden Zeichenfolgen sind gültige Deallocator-Werte:

-   Keine
-   WSDFreeLinkedMemory
-   CoTaskMemFree
-   frei
-   delete
-   deleteArray
-   Freigabe

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




