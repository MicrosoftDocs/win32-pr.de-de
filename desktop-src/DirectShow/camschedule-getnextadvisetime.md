---
description: Die GetNextAdviseTime-Methode ruft den Zeitpunkt der nächsten Empfehlungsanforderung ab.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: CABSchedule.GetNextAdviseTime-Methode (Dsschedule.h)
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
ms.openlocfilehash: 6c7fd04622a5cdab8bade32f41b090d8f480db292209d284804b5180134954f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662346"
---
# <a name="camschedulegetnextadvisetime-method"></a>CABSchedule.GetNextAdviseTime-Methode

Die `GetNextAdviseTime` -Methode ruft den Zeitpunkt der nächsten Empfehlungsanforderung ab.

## <a name="syntax"></a>Syntax


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die Referenzzeit der nächsten Empfehlungsanforderung oder MAX TIME zurück, \_ für die keine Anforderungen geplant sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dsschedule.h (include Streams.h)</dt> </dl>                                                                                |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WEBCAMSchedule-Klasse**](camschedule.md)
</dt> </dl>

 

 




