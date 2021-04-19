---
title: Wiedergabeliste. setCheckedState2
description: Die setCheckedState2-Methode legt den aktivierten Zustand des Elements mit dem angegebenen Index im Wiedergabelisten Element fest.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- Wiedergabeliste. setCheckedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37cc9c821ae783e79d327e93b0c2f297fb75eab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360279"
---
# <a name="playlistsetcheckedstate2"></a>Wiedergabeliste. setCheckedState2

Die **setCheckedState2** -Methode legt den aktivierten Zustand des Elements mit dem angegebenen Index im **Wiedergabe** Listenelement fest.

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Position*
</dt> <dd>

**Zahl** (**Long**), die den Index des Wiedergabelisten Elements angibt, das überprüft oder deaktiviert werden soll.

</dd> <dt>

<span id="checked"></span><span id="CHECKED"></span>*über*
</dt> <dd>

**Boolescher** Wert, der angibt, ob das angegebene Element überprüft (true) oder deaktiviert (false) ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen** Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann mit schsted-Wiedergabelisten arbeiten und ersetzt die **setcheckedstate** -Methode, die nicht. Sie können alle Elemente auf den angeforderten Zustand festlegen, indem Sie im *Item* -Parameter den Wert 1 angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> <dt>

[**Wiedergabeliste. setcheckedstate**](playlist-setcheckedstate.md)
</dt> </dl>

 

 





