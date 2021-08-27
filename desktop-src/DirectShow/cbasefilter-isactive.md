---
description: Die IsActive-Methode bestimmt, ob der Filter derzeit aktiv ist (wird ausgeführt oder angehalten).
ms.assetid: 3bbb50d5-6a07-4932-940c-4466b95e6412
title: CBaseFilter.IsActive-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fbbd9fedf94816d518ef9f8826542399d1d1e97f97137b2d86581d36c4a33e53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076640"
---
# <a name="cbasefilterisactive-method"></a>CBaseFilter.IsActive-Methode

Die `IsActive` -Methode bestimmt, ob der Filter derzeit aktiv ist (wird ausgeführt oder angehalten).

## <a name="syntax"></a>Syntax


```C++
BOOL IsActive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn der Filter angehalten oder ausgeführt wird, oder **FALSE,** wenn er beendet wird.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




