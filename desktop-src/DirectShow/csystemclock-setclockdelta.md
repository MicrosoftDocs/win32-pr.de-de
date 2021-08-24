---
description: Die SetClockDelta-Methode passt die Uhrzeit an. Diese Methode implementiert die IAMClockAdjust::SetClockDelta-Methode.
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: CSystemClock.SetClockDelta-Methode (Sysclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c98ccf35e41886594a3aab8c3abec6737128d8d7e22f6dfb75d0ac88ac3b7a02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538660"
---
# <a name="csystemclocksetclockdelta-method"></a>CSystemClock.SetClockDelta-Methode

Die `SetClockDelta` -Methode passt die Uhrzeit an. Diese Methode implementiert die [**IAMClockAdjust::SetClockDelta-Methode.**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtDelta* 
</dt> <dd>

Gibt den Betrag an, um den die Uhr als [**REFERENCE \_ TIME-Wert**](reference-time.md) angepasst werden soll. Ein positiver Wert verschiebt die Uhr vorwärts, und ein negativer Wert verschiebt die Uhr rückwärts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen **HRESULT-Fehlercode** zurück.

## <a name="remarks"></a>Hinweise

Diese Methode ruft einfach [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md)auf.

Die von [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) zurückgegebenen Zeitwerte erhöhen sich monoton. Wenn Sie die Uhr zurückgesetzt haben, meldet **GetTime** weiterhin die alte Zeit, bis die interne Uhr aufholt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | CSystemClock-Klasse<br/>                                                                                                                                                              |
| Header<br/>  | <dl> <dt>Sysclock.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




