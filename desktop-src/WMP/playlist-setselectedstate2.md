---
title: PLAYLIST.setSelectedState2
description: Die setSelectedState2-Methode legt den ausgewählten Zustand des Elements mit dem angegebenen Index im PLAYLIST-Element fest.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- PLAYLIST.setSelectedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f952d00486fe2419ab48592c7624299ef466c5dfa2b96d53fefb308fc537488
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335812"
---
# <a name="playlistsetselectedstate2"></a>PLAYLIST.setSelectedState2

Die **setSelectedState2-Methode** legt den ausgewählten Zustand des Elements mit dem angegebenen Index im **PLAYLIST-Element** fest.

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Artikel*
</dt> <dd>

**Zahl** (**long**), die den Index eines Elements in der Wiedergabeliste angibt.

</dd> <dt>

<span id="selected"></span><span id="SELECTED"></span>*Ausgewählten*
</dt> <dd>

**Boolescher Wert,** der angibt, ob das angegebene Element ausgewählt (TRUE) oder deaktiviert (FALSE) werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode kann mit geschachtelten Wiedergabelisten funktionieren und ersetzt die **setSelectedState-Methode,** die dies nicht kann. Sie können alle Elemente auf den angeforderten Zustand festlegen, indem Sie im *Elementparameter* 1 angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setSelectedState**](playlist-setselectedstate.md)
</dt> </dl>

 

 





