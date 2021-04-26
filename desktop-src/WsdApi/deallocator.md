---
description: Gibt den Typ des Deallocators an, der von einer Stubfunktion verwendet werden soll.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: deallocator-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692ed2e57b3e649c0ee7af171f205c949496f9b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994937"
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

Der Deallocator-Typ sollte in ein Tagpaar eingeschlossen <deallocator></deallocator> werden. Die folgenden Zeichenfolgen sind gültige Deallocator-Werte:

-   Keine
-   WSDFreeLinkedMemory
-   CoTaskMemFree
-   free
-   delete
-   deleteArray
-   Release

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




