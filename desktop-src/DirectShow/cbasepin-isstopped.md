---
description: Die IsStopped-Methode bestimmt, ob der Filter, der diesen Pin enthält, beendet wird.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: CBasePin.IsStopped-Methode (Amfilter.h)
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
ms.openlocfilehash: 64e833ef495ace41a9dcd1614b69e4a081befce0e429fa7aad800a73ce490439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916390"
---
# <a name="cbasepinisstopped-method"></a>CBasePin.IsStopped-Methode

Die `IsStopped` -Methode bestimmt, ob der Filter, der diesen Pin enthält, beendet wird.

## <a name="syntax"></a>Syntax


```C++
BOOL IsStopped();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn der Filter beendet wird. Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode nicht innerhalb der **CBasePin-Konstruktormethode** auf, da der Filter möglicherweise noch nicht initialisiert wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




