---
title: Wiedergabeliste. getnextcheckeditem
description: Die getnextcheckeditem-Methode ruft den Index des nächsten aktivierten Elements in der Wiedergabeliste nach dem angegebenen Index ab.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- Wiedergabeliste. getnextcheckeditem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373608"
---
# <a name="playlistgetnextcheckeditem"></a>Wiedergabeliste. getnextcheckeditem

Die **getnextcheckeditem** -Methode ruft den Index des nächsten aktivierten Elements in der Wiedergabeliste nach dem angegebenen Index ab.

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Position*
</dt> <dd>

**Zahl** (**Long**), die den Index des Elements angibt, nach dem gesucht werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**Long**) zurück.

## <a name="remarks"></a>Bemerkungen

Wenn keine weiteren aktivierten Elemente vorhanden sind, gibt diese Methode 1 zurück.

Diese Methode wurde durch **getNextCheckedItem2** ersetzt, der als Unterstützung für die wieder-Wiedergabeliste steht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> <dt>

[**Wiedergabeliste. getNextCheckedItem2**](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





