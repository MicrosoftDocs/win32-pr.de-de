---
description: Die getnexti-Methode ruft das Element an der angegebenen Position ab und erhöht die Position.
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: Cbaselist. getnexti-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370116"
---
# <a name="cbaselistgetnexti-method"></a>Cbaselist. getnexti-Methode

Die `GetNextI` -Methode ruft das Element an der angegebenen Position ab und erhöht die Position.

## <a name="syntax"></a>Syntax


```C++
void* GetNextI(
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

Gibt einen Zeiger auf das Element zurück. Wenn *RP* **null** ist, gibt die Methode **null** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode verschiebt den Positionsindikator auf die nächste Position. Wenn sich der Positionsindikator hinter das Ende der Liste bewegt, legt die-Methode ihn auf **null** fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




