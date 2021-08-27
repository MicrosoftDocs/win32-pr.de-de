---
description: Die Prev-Methode ruft die vorherige Position in der Liste ab.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: CBaseList.Prev-Methode (Wxlist.h)
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
ms.openlocfilehash: d04a63079e401b89286e10e927b540f40d04fc186546dbdbd4e31e8610fe617d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076600"
---
# <a name="cbaselistprev-method"></a>CBaseList.Prev-Methode

Die `Prev` -Methode ruft die vorherige Position in der Liste ab.

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

POSITION-Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Positionsindikator zurück, der vor der in pos angegebenen *Position liegt.*

## <a name="remarks"></a>Hinweise

Wenn *pos* die erste Position in der Liste ist, gibt die Methode **NULL zurück.** Wenn *pos* NULL **ist,** gibt die Methode die letzte Position in der Liste zurück.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




