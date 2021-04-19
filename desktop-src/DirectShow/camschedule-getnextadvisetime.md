---
description: Die getnextadviantime-Methode ruft den Zeitpunkt der nächsten anforderungsanforderung ab.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: Camschedule. getnextadvitstime-Methode (dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5894ae98666c9134abd4bce96922a5f28d5919b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366755"
---
# <a name="camschedulegetnextadvisetime-method"></a>Camschedule. getnextadvictime-Methode

Die- `GetNextAdviseTime` Methode ruft den Zeitpunkt der nächsten anforderungsanforderung ab.

## <a name="syntax"></a>Syntax


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die Verweis Zeit der nächsten anforderungsanforderung oder die maximale Zeit für die geplante Ausführung von \_ Anforderungen zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dsschedule. h (Include Streams. h)</dt> </dl>                                                                                |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camschedule-Klasse**](camschedule.md)
</dt> </dl>

 

 




