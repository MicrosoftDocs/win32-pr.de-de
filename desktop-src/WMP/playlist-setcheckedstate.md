---
title: Wiedergabeliste. setcheckedstate
description: Die setcheckedstate-Methode gibt an, dass das indizierte Element in der Wiedergabeliste überprüft wird.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- Wiedergabeliste. setcheckedstate Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a8c86459dcf590b1ff1e884a8aa671dc1bba78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369935"
---
# <a name="playlistsetcheckedstate"></a>Wiedergabeliste. setcheckedstate

Die **setcheckedstate** -Methode gibt an, dass das indizierte Element in der Wiedergabeliste überprüft wird.

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Position*
</dt> <dd>

**Number** (**Long**), der den Index des zu überprüfenden Wiedergabelisten Elements angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen** Wert zurück.

## <a name="remarks"></a>Bemerkungen

Sie können alle Elemente in den aktivierten Zustand setzen, indem Sie im *Item* -Parameter den Wert 1 angeben.

Diese Methode wurde durch **setCheckedState2** ersetzt, der als Unterstützung für die wieder-Wiedergabeliste steht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> <dt>

[**Wiedergabeliste. setCheckedState2**](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





