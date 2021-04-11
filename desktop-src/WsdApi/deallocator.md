---
description: Gibt den Typ der dezuweisung an, der von einer stubfunktion verwendet werden soll.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: enzuordcator-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3604f0efb366c3f88e2e0828c02344ee75606079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215434"
---
# <a name="deallocator-element"></a>enzuordcator-Element

Gibt den Typ der dezuweisung an, der von einer stubfunktion verwendet werden soll.

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
| [**stubdefinitionen**](stubdefinitions.md)<br/> | Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Der dezuordnertyp sollte in ein Tagpaar eingeschlossen werden <deallocator></deallocator> . Die folgenden Zeichen folgen sind gültige Freigabe Werte:

-   none
-   Wsdfreelinkedmemory
-   CoTaskMemFree
-   free
-   delete
-   deletearray
-   Release

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




