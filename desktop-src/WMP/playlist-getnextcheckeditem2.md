---
title: Wiedergabeliste. getNextCheckedItem2
description: Die getNextCheckedItem2-Methode ruft den Index des nächsten aktivierten Elements in der Wiedergabeliste nach dem angegebenen Index ab.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- Wiedergabeliste. getNextCheckedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368285"
---
# <a name="playlistgetnextcheckeditem2"></a>Wiedergabeliste. getNextCheckedItem2

Die **getNextCheckedItem2** -Methode ruft den Index des nächsten aktivierten Elements in der Wiedergabeliste nach dem angegebenen Index ab.

``` syntax
        elementID.getNextCheckedItem2(item)
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

Diese Methode kann mit schsted-Wiedergabelisten arbeiten und ersetzt die **getnextcheckeditem** -Methode, die nicht. Übergeben Sie 1 in den *Element* Parameter, um das erste aktivierte Element zu suchen. Wenn keine weiteren aktivierten Elemente vorhanden sind, gibt diese Methode 1 zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> <dt>

[**Wiedergabeliste. getnextcheckeditem**](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





