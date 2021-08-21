---
title: PLAYLIST.getNextCheckedItem2
description: Die getNextCheckedItem2-Methode ruft den Index des nächsten überprüften Elements in der Wiedergabeliste nach dem angegebenen Index ab.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- PLAYLIST.getNextCheckedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9bd39ba95aff88bccfa43885f8c15fba6bb0beef20d51dd3ca4cf6f36bda05b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118834867"
---
# <a name="playlistgetnextcheckeditem2"></a>PLAYLIST.getNextCheckedItem2

Die **getNextCheckedItem2-Methode** ruft den Index des nächsten überprüften Elements in der Wiedergabeliste nach dem angegebenen Index ab.

``` syntax
        elementID.getNextCheckedItem2(item)
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

Diese Methode kann mit geschachtelten Wiedergabelisten funktionieren und ersetzt die **getNextCheckedItem-Methode,** was nicht möglich ist. Übergeben Sie 1 im *Elementparameter,* um das erste überprüfte Element zu finden. Wenn keine weiteren überprüften Elemente enthalten sind, gibt diese Methode 1 zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextCheckedItem**](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





