---
title: Wiedergabeliste. setselectedstate
description: Die setselectedstate-Methode gibt an, dass das indizierte Element in der Wiedergabeliste ausgewählt ist.
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- Wiedergabeliste. setselectedstate Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a7bb545330710ae4fe2c39eae4556207061203
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360448"
---
# <a name="playlistsetselectedstate"></a>Wiedergabeliste. setselectedstate

Die **setselectedstate** -Methode gibt an, dass das indizierte Element in der Wiedergabeliste ausgewählt ist.

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Position*
</dt> <dd>

**Zahl** (**Long**), die den Index eines Elements in der Wiedergabeliste angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Sie können alle Elemente auf den ausgewählten Zustand festlegen, indem Sie im *Item* -Parameter den Wert 1 angeben.

Diese Methode wurde durch **setSelectedState2** ersetzt, der als Unterstützung für die wieder-Wiedergabeliste steht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> <dt>

[**Wiedergabeliste. setSelectedState2**](playlist-setselectedstate2.md)
</dt> </dl>

 

 





