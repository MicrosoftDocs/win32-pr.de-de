---
title: smartwiedergabe-Element
description: Das smartwiedergabe-Element enthält den dynamisch definierten Teil einer Wiedergabeliste.
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- smartwiedergabe-Element, Windows Media Player
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 511294af2de4343cb7f63db4312d530aadf57da6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371489"
---
# <a name="smartplaylist-element"></a>smartwiedergabe-Element

Das **smartwiedergabe** -Element enthält den dynamisch definierten Teil einer Wiedergabeliste.

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a>Attribute



| Begriff                                                                                                                                   | BESCHREIBUNG                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**Version** (erforderlich) <br/> | Die Dezimalzahl, die die Versionsnummer des intelligenten Wiedergabelisten Schemas darstellt. Legen Sie auf 1.0.0.0 fest.<br/> |



 

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente                                                       |
|-----------|----------------------------------------------------------------|
| Parent    | [Seq](seq-element.md)                                         |
| Untergeordnet     | [Queryset](queryset-element.md), [Filter](filter-element.md) |



 

## <a name="remarks"></a>Bemerkungen

Ein **smartwiedergabe** -Element enthält in der Regel ein **Queryset** -Element und kann auch ein **Filter** Element enthalten.

## <a name="examples"></a>Beispiele


```
<smartPlaylist version = "1.0.0.0">
    <querySet>
        <sourceFilter 
            type = "smartFilterObject"
            id = "12345678-1234-3333-abCD-123ABCdefGHI"
            name = "Music in my library">
                <fragment name = "Genre">
                    <argument name = "condition">Is</argument>
                    <argument name = "value">Rock</argument>
                </fragment>
                <fragment name = "Album Artist">
                    <argument name = "condition">Is Not</argument>
                    <argument name = "value">Brenda Diaz</argument>
                </fragment>
        </sourceFilter>
    </querySet>
    <filter>
    </filter>
</smartPlaylist>
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

[**Queryset-Element**](queryset-element.md)
</dt> <dt>

[**ENQ-Element**](seq-element.md)
</dt> <dt>

[**Referenz zu Windows Media-Wiedergabelisten Elementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





