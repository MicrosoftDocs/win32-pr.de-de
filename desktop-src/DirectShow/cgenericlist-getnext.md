---
description: Die GetNext-Methode ruft das Element an der angegebenen Position ab und erhöht die Position.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: Cgenericlist. GetNext-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9491e58d817ce2c9dc4fb59fafa9bf96812a013a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366765"
---
# <a name="cgenericlistgetnext-method"></a>Cgenericlist. GetNext-Methode

Die `GetNext` -Methode ruft das Element an der angegebenen Position ab und erhöht die Position.

## <a name="syntax"></a>Syntax


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RP* \[ atur\]
</dt> <dd>

Verweis auf einen Positionswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp) zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode verschiebt den Positionsindikator auf die nächste Position. Wenn sich der Positionsindikator hinter das Ende der Liste bewegt, legt die-Methode ihn auf **null** fest.

Wenn *RP* **null** ist, gibt die Methode **null** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cgenericlist-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




