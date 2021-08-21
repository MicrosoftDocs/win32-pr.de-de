---
title: PLAYLIST.setCheckedState2
description: Die setCheckedState2-Methode legt den aktivierten Zustand des Elements mit dem angegebenen Index im PLAYLIST-Element fest.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- PLAYLIST.setCheckedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6b95cb332c5f5a9d86e6f49484b27c1ab5802f28b18195f610395a1c732e369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336219"
---
# <a name="playlistsetcheckedstate2"></a>PLAYLIST.setCheckedState2

Die **setCheckedState2-Methode** legt den aktivierten Zustand des Elements mit dem angegebenen Index im **PLAYLIST-Element** fest.

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Artikel*
</dt> <dd>

**Zahl** (**long**), die den Index des Wiedergabelistenelements angibt, das überprüft oder deaktiviert werden soll.

</dd> <dt>

<span id="checked"></span><span id="CHECKED"></span>*Überprüft*
</dt> <dd>

**Boolescher Wert,** der angibt, ob das angegebene Element überprüft (true) oder deaktiviert (FALSE) werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen zurück.**

## <a name="remarks"></a>Hinweise

Diese Methode kann mit geschachtelten Wiedergabelisten arbeiten und ersetzt die **setCheckedState-Methode,** was nicht möglich ist. Sie können alle Elemente auf den angeforderten Zustand festlegen, indem Sie im *Elementparameter* 1 angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setCheckedState**](playlist-setcheckedstate.md)
</dt> </dl>

 

 





