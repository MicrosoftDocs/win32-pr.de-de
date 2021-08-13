---
title: PLAYLIST.getNextSelectedItem
description: Die getNextSelectedItem-Methode ruft den Index des nächsten ausgewählten Elements in der Wiedergabeliste nach dem angegebenen Index ab.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- PLAYLIST.getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 872dd31694384dfa35d7ce98c2f26756ede14539f4e788cbb6f699d17ca78a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467750"
---
# <a name="playlistgetnextselecteditem"></a>PLAYLIST.getNextSelectedItem

Die **getNextSelectedItem-Methode** ruft den Index des nächsten ausgewählten Elements in der Wiedergabeliste nach dem angegebenen Index ab.

``` syntax
        elementID.getNextSelectedItem(item)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Artikel*
</dt> <dd>

**Zahl** (**long**), die den Index des Elements angibt, nach dem gesucht werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** **(long) zurück.**

## <a name="remarks"></a>Hinweise

Wenn keine weiteren ausgewählten Elemente angezeigt werden, gibt diese Methode 1 zurück.

Diese Methode wurde durch **getNextSelectedItem2** ersetzt, das geschachtelte Wiedergabelisten unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextSelectedItem2**](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





