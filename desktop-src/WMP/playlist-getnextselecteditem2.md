---
title: PLAYLIST.getNextSelectedItem2
description: Die getNextSelectedItem2-Methode ruft den Index des nächsten ausgewählten Elements in der Wiedergabeliste nach dem angegebenen Index ab.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- PLAYLIST.getNextSelectedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6d1f98a418da1d8b21345598999f847cbf2142e9ca575bcfdc7047e2f9fd524
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415280"
---
# <a name="playlistgetnextselecteditem2"></a>PLAYLIST.getNextSelectedItem2

Die **getNextSelectedItem2-Methode** ruft den Index des nächsten ausgewählten Elements in der Wiedergabeliste nach dem angegebenen Index ab.

``` syntax
        elementID.getNextSelectedItem2(item)
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

Diese Methode kann mit geschachtelten Wiedergabelisten arbeiten und ersetzt die **getNextSelectedItem-Methode,** was nicht möglich ist. Übergeben Sie 1 im *Elementparameter,* um das erste ausgewählte Element zu finden. Wenn keine weiteren ausgewählten Elemente angezeigt werden, wird -1 zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextSelectedItem**](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





