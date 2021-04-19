---
title: Wiedergabeliste. ItemCount
description: Das ItemCount-Attribut ruft die Anzahl der Elemente ab, die momentan im Wiedergabelisten Element angezeigt werden.
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- Wiedergabeliste. ItemCount Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359785"
---
# <a name="playlistitemcount"></a>Wiedergabeliste. ItemCount

Das **ItemCount** -Attribut ruft die Anzahl der Elemente ab, die momentan im **Wiedergabe** Listenelement angezeigt werden.

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a>Mögliche Werte

Bei diesem Attribut handelt es sich um eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Die **ItemCount** -Eigenschaft zählt die Gesamtzahl der erweiterten Elemente. Wenn beispielsweise zwei Wiedergabelisten vorhanden sind, die jeweils drei Medienelemente enthalten, gibt **ItemCount** 2 zurück, wenn die Wiedergabelisten nicht erweitert werden. Wenn nur die erste Wiedergabeliste erweitert ist, wird von **ItemCount** der Wert 4 zurückgegeben. Wenn beide Wiedergabelisten erweitert werden, wird von **ItemCount** der Wert 6 zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> </dl>

 

 





