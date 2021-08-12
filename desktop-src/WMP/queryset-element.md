---
title: querySet-Element
description: Das querySet-Element enthält Elemente, die definieren, welche Medienelemente aus der Bibliothek ausgewählt werden.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- querySet-Element Windows Media Player
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb157bb30c2e728b7840fe7021a2a4fcacc317b10eb6778b5702d7d2277c4a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570613"
---
# <a name="queryset-element"></a>querySet-Element

Das **querySet-Element** enthält Elemente, die definieren, welche Medienelemente aus der Bibliothek ausgewählt werden.

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy | Elemente                                   |
|-----------|--------------------------------------------|
| Parent    | [smartPlaylist](smartplaylist-element.md) |
| Untergeordnet     | [Sourcefilter](sourcefilter-element.md)   |



 

## <a name="remarks"></a>Hinweise

Das **querySet-Element** gibt an, welche Medienelemente aus der Bibliothek ausgewählt werden sollen, ohne die Größe des Ergebnisses zu betrachten. Das **Filterelement** schränkt hingegen die Größe des Resultsets ein.

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
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**argument-Element**](argument-element.md)
</dt> <dt>

[**filter-Element**](filter-element.md)
</dt> <dt>

[**fragment-Element**](fragment-element.md)
</dt> <dt>

[**smartPlaylist-Element**](smartplaylist-element.md)
</dt> <dt>

[**sourceFilter-Element**](sourcefilter-element.md)
</dt> <dt>

[**Windows Medienwiedergabelisten-Elementreferenz**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





