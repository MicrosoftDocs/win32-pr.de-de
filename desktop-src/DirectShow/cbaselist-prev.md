---
description: Die prev-Methode ruft die vorherige Position in der Liste ab.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: Cbaselist. prev-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03c35a89754b27aa67a5bba33ee694433d74c0fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365462"
---
# <a name="cbaselistprev-method"></a>Cbaselist. prev-Methode

Die- `Prev` Methode ruft die vorherige Position in der Liste ab.

## <a name="syntax"></a>Syntax


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

Positionswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Positionsindikator zurück, der vor der in *POS* angegebenen Position liegt.

## <a name="remarks"></a>Bemerkungen

Wenn *POS* die erste Position in der Liste ist, gibt die Methode **null** zurück. Wenn *POS* **null** ist, gibt die Methode die letzte Position in der Liste zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




