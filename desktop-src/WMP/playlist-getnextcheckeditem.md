---
title: PLAYLIST.getNextCheckedItem
description: Die getNextCheckedItem-Methode ruft den Index des nächsten überprüften Elements in der Wiedergabeliste nach dem angegebenen Index ab.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- PLAYLIST.getNextCheckedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54b6e598737d1aac09754b15c037c27a435deb5fff34c729aa48c51019e12982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571450"
---
# <a name="playlistgetnextcheckeditem"></a>PLAYLIST.getNextCheckedItem

Die **getNextCheckedItem-Methode** ruft den Index des nächsten überprüften Elements in der Wiedergabeliste nach dem angegebenen Index ab.

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Artikel*
</dt> <dd>

**Number** (**long**) gibt den Index des Elements an, nach dem gesucht werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**long**) zurück.

## <a name="remarks"></a>Hinweise

Wenn keine weiteren überprüften Elemente vorhanden sind, gibt diese Methode 1 zurück.

Diese Methode wurde durch **getNextCheckedItem2** ersetzt, das geschachtelte Wiedergabelisten unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextCheckedItem2**](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





