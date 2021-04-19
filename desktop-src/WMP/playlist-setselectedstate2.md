---
title: Wiedergabeliste. setSelectedState2
description: Die setSelectedState2-Methode legt den ausgewählten Zustand des Elements mit dem angegebenen Index im Wiedergabelisten Element fest.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- Wiedergabeliste. setSelectedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1a4e317543765fb24755516a0637b16958ad679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374037"
---
# <a name="playlistsetselectedstate2"></a>Wiedergabeliste. setSelectedState2

Die **setSelectedState2** -Methode legt den ausgewählten Zustand des Elements mit dem angegebenen Index im **Wiedergabe** Listenelement fest.

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Position*
</dt> <dd>

**Zahl** (**Long**), die den Index eines Elements in der Wiedergabeliste angibt.

</dd> <dt>

<span id="selected"></span><span id="SELECTED"></span>*gewählte*
</dt> <dd>

Ein **boolescher** Wert, der angibt, ob das angegebene Element ausgewählt (true) oder nicht ausgewählt (false) ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann mit zusammengefügten Wiedergabelisten arbeiten und ersetzt die **setselectedstate** -Methode, die nicht. Sie können alle Elemente auf den angeforderten Zustand festlegen, indem Sie im *Item* -Parameter den Wert 1 angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> <dt>

[**Wiedergabeliste. setselectedstate**](playlist-setselectedstate.md)
</dt> </dl>

 

 





