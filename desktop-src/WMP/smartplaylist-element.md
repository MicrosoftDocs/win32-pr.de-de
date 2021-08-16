---
title: smartPlaylist-Element
description: Das smartPlaylist-Element enthält den dynamisch definierten Teil einer Wiedergabeliste.
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- smartPlaylist-Element Windows Media Player
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a21d685759e9e8b27c881ceaec6595535b3c4b799eb28ecd94dd96a3a571ec99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763470"
---
# <a name="smartplaylist-element"></a>smartPlaylist-Element

Das **smartPlaylist-Element** enthält den dynamisch definierten Teil einer Wiedergabeliste.

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a>Attribute



| Begriff                                                                                                                                   | BESCHREIBUNG                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**Version** (erforderlich) <br/> | Die Dezimalzahl, die die Versionsnummer des Schemas für intelligente Wiedergabelisten darstellt. Legen Sie auf 1.0.0.0 fest.<br/> |



 

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy | Elemente                                                       |
|-----------|----------------------------------------------------------------|
| Parent    | [Seq](seq-element.md)                                         |
| Untergeordnet     | [querySet,](queryset-element.md) [filter](filter-element.md) |



 

## <a name="remarks"></a>Hinweise

Ein **smartPlaylist-Element** enthält in der Regel ein **querySet-Element** und kann auch ein **Filterelement** enthalten.

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
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**argument-Element**](argument-element.md)
</dt> <dt>

[**filter-Element**](filter-element.md)
</dt> <dt>

[**fragment-Element**](fragment-element.md)
</dt> <dt>

[**querySet-Element**](queryset-element.md)
</dt> <dt>

[**seq-Element**](seq-element.md)
</dt> <dt>

[**Windows Referenz zu Medienwiedergabelistenelementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





