---
description: Gibt den Typ des Zuordnungsdelocators an, der von einer Stubfunktion verwendet werden soll.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: deallocator-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2617ce92dcd0c2763f77b0bc6f0fb5c1beea1c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881059"
---
# <a name="deallocator-element"></a>deallocator-Element

Gibt den Typ des Zuordnungsdelocators an, der von einer Stubfunktion verwendet werden soll.

## <a name="usage"></a>Verwendung

``` syntax
<deallocator/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                               | Beschreibung                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Der Zuordnungstyp sollte in ein Paar von &lt; &gt; </deallocator> Zuordnungstags eingeschlossen werden. Die folgenden Zeichenfolgen sind gültige Zuordnungswerte:

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



 

 




