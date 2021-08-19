---
title: PLAYLIST.setCheckedState
description: Die setCheckedState-Methode gibt an, dass das indizierte Element in der Wiedergabeliste überprüft wird.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- PLAYLIST.setCheckedState Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93e143f738197524e1555f18aedf84aa606626de645a98149c65507b71291cde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336247"
---
# <a name="playlistsetcheckedstate"></a>PLAYLIST.setCheckedState

Die **setCheckedState-Methode** gibt an, dass das indizierte Element in der Wiedergabeliste überprüft wird.

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Artikel*
</dt> <dd>

**Zahl** (**long**), die den Index des zu überprüfenden Wiedergabelistenelements angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen zurück.**

## <a name="remarks"></a>Hinweise

Sie können alle Elemente auf den überprüften Zustand festlegen, indem Sie im *Elementparameter* 1 angeben.

Diese Methode wurde durch **setCheckedState2** ersetzt, das geschachtelte Wiedergabelisten unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setCheckedState2**](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





