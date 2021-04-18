---
description: Die isbeendete-Methode bestimmt, ob der Filter, der diese PIN enthält, angehalten wird.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: Cbasepin. isbeendete-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4185c02b396f7d0d570081ba1401e0ec9e301d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365798"
---
# <a name="cbasepinisstopped-method"></a>Cbasepin. isbeendet-Methode

Die- `IsStopped` Methode bestimmt, ob der Filter, der diese PIN enthält, angehalten wird.

## <a name="syntax"></a>Syntax


```C++
BOOL IsStopped();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn der Filter beendet wurde. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Nennen Sie diese Methode nicht innerhalb der **cbasepin** -Konstruktormethode, da der Filter möglicherweise noch nicht initialisiert wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




