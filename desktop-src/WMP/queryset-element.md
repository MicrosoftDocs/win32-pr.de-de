---
title: Queryset-Element
description: Das Queryset-Element enthält Elemente, die definieren, welche Medienelemente aus der Bibliothek ausgewählt werden.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- Queryset-Element, Windows-Media Player
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4971c2a7f601132640d7654a95dd288f1740a467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356023"
---
# <a name="queryset-element"></a>Queryset-Element

Das **Queryset** -Element enthält Elemente, die definieren, welche Medienelemente aus der Bibliothek ausgewählt werden.

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente                                   |
|-----------|--------------------------------------------|
| Parent    | [smartwiedergabe](smartplaylist-element.md) |
| Untergeordnet     | [sourceFilter](sourcefilter-element.md)   |



 

## <a name="remarks"></a>Bemerkungen

Das **Queryset** -Element gibt an, welche Medienelemente aus der Bibliothek ausgewählt werden sollen, ohne Berücksichtigung der Größe des Resultsets. Das **Filter** -Element hingegen schränkt die Größe des Resultsets ein.

## <a name="examples"></a>Beispiele


```
<querySet>
    <sourceFilter 
        type = "smartFilterObject" 
        id = "{4202947A-A563-4B05-A754-A1B4B5989849}"
        name = "Windows Media Local Music Library Filter">
            <fragment name = "Genre">
                <argument name = "Condition">Equals</argument>
                <argument name = "Value">Rock</argument>
            </fragment>
            <fragment name = "Artist">
                <argument name = "Condition">Does Not Equal</argument>
                <argument name = "Value">Brenda Diaz</argument>
            </fragment>
    </sourceFilter>
</querySet>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Argument-Element**](argument-element.md)
</dt> <dt>

[**Filter-Element**](filter-element.md)
</dt> <dt>

[**Fragment-Element**](fragment-element.md)
</dt> <dt>

[**smartwiedergabe-Element**](smartplaylist-element.md)
</dt> <dt>

[**SourceFilter-Element**](sourcefilter-element.md)
</dt> <dt>

[**Referenz zu Windows Media-Wiedergabelisten Elementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





