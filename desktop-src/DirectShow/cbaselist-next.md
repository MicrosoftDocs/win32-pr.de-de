---
description: Die Next-Methode ruft die nächste Position in der Liste ab.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: CBaseList.Next-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d07030c046f3fe55178707af297542f383bfd5cf75f40169b5c93cfafa1c698b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658956"
---
# <a name="cbaselistnext-method"></a>CBaseList.Next-Methode

Die `Next` -Methode ruft die nächste Position in der Liste ab.

## <a name="syntax"></a>Syntax


```C++
POSITION Next(
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

Gibt den Positionsindikator zurück, der der durch pos angegebenen Position *folgt.*

## <a name="remarks"></a>Hinweise

Wenn *pos* die letzte Position in der Liste ist, gibt die Methode **NULL zurück.** Wenn *pos* **NULL ist,** gibt die Methode die erste Position in der Liste zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




