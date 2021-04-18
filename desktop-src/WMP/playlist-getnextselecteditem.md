---
title: Wiedergabeliste. getnextselecteditem
description: Die getnextselecteditem-Methode ruft den Index des nächsten ausgewählten Elements in der Wiedergabeliste nach dem angegebenen Index ab.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- Wiedergabeliste. getnextselecteditem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c5e37ad5109066a11cf28a593ed69f8c86b8b639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368284"
---
# <a name="playlistgetnextselecteditem"></a>Wiedergabeliste. getnextselecteditem

Die **getnextselecteditem** -Methode ruft den Index des nächsten ausgewählten Elements in der Wiedergabeliste nach dem angegebenen Index ab.

``` syntax
        elementID.getNextSelectedItem(item)
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

Wenn keine weiteren ausgewählten Elemente vorhanden sind, gibt diese Methode 1 zurück.

Diese Methode wurde durch **getNextSelectedItem2** ersetzt, der als Unterstützung für die wieder-Wiedergabeliste steht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> <dt>

[**Wiedergabeliste. getNextSelectedItem2**](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





