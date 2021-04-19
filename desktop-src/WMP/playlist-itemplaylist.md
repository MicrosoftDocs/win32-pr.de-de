---
title: Wiedergabeliste. itemwiedergabe Liste
description: Das itemwiedergabe-Attribut ruft die Wiedergabeliste für das Medien Element ab, das am angegebenen Index im Wiedergabelisten Element angezeigt wird.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- Wiedergabeliste. itemwiedergabe Fenster Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359783"
---
# <a name="playlistitemplaylist"></a>Wiedergabeliste. itemwiedergabe Liste

Das **itemwiedergabe** -Attribut ruft die Wiedergabeliste für das Medien Element ab, das am angegebenen Index im **Wiedergabe** Listenelement angezeigt wird.

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein Schreib geschütztes **Wiedergabe** Listen Objekt.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Sin*
</dt> <dd>

**Zahl**(**Long**), die den Index eines Wiedergabelisten Elements enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **itemwiedergabe** -Eigenschaft gibt das Wiedergabelisten Objekt zurück, das im **Wiedergabe** Listenelement erweitert wird. Wenn z. b. zwei nicht im **Wiedergabe** Listenelement enthaltene, nicht erweiterte Wiedergabelisten vorhanden sind und jeweils drei Medienclips enthalten, gibt **itemwiedergabe**(1) die übergeordnete Wiedergabeliste zurück, die die beiden in der Liste enthaltenen Wiedergabelisten enthält. Wenn die zweite Wiedergabeliste erweitert ist, gibt **itemwiedergabe**(1) die zweite Wiedergabeliste zurück. Wenn beide Wiedergabelisten erweitert werden, gibt **itemwiedergabe**(1) die erste Wiedergabeliste zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> </dl>

 

 





