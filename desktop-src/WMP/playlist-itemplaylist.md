---
title: PLAYLIST.itemPlaylist
description: Das itemPlaylist-Attribut ruft die Wiedergabeliste für das Medienelement ab, das am angegebenen Index im PLAYLIST-Element angezeigt wird.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- PLAYLIST.itemPlaylist Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f2ed3173042d68ec048486189d909be60427df92e9936d4446f8d7a99ef592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571172"
---
# <a name="playlistitemplaylist"></a>PLAYLIST.itemPlaylist

Das **itemPlaylist-Attribut** ruft die Wiedergabeliste für das Medienelement ab, das am angegebenen Index im **PLAYLIST-Element** angezeigt wird.

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein schreibgeschütztes **Wiedergabelistenobjekt.**

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Index*
</dt> <dd>

**Zahl**(**long**), die den Index eines Wiedergabelistenelements enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **itemPlaylist-Eigenschaft** gibt das Wiedergabelistenobjekt zurück, das im **PLAYLIST-Element** erweitert wird. Wenn beispielsweise zwei geschachtelte Wiedergabelisten vorhanden sind, die im **PLAYLIST-Element** nicht erweitert sind und jeweils drei Medienclips enthalten, gibt **itemPlaylist**(1) die übergeordnete Wiedergabeliste zurück, die die beiden geschachtelten Wiedergabelisten enthält. Wenn die zweite Wiedergabeliste erweitert wird, gibt **itemPlaylist**(1) die zweite Wiedergabeliste zurück. Wenn beide Wiedergabelisten erweitert sind, gibt **itemPlaylist**(1) die erste Wiedergabeliste zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> </dl>

 

 





