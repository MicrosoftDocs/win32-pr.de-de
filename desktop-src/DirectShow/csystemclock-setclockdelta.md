---
description: 'Die setclockdelta-Methode passt die Uhrzeit an. Diese Methode implementiert die iamclockadjust:: setclockdelta-Methode.'
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Csystemclock. setclockdelta-Methode (sysclock. h)
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
ms.openlocfilehash: cc1027081cc8713cffd2979e20627c037d0799f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355270"
---
# <a name="csystemclocksetclockdelta-method"></a>Csystemclock. setclockdelta-Methode

Die- `SetClockDelta` Methode passt die Uhrzeit an. Diese Methode implementiert die [**iamclockadjust:: setclockdelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtdelta* 
</dt> <dd>

Gibt den Betrag an, um den die Uhr als [**Verweis \_ Zeitwert**](reference-time.md) angepasst werden soll. Ein positiver Wert verschiebt die Uhr vorwärts, und ein negativer Wert verschiebt die Uhr nach unten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen **HRESULT** -Fehlercode zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft einfach [**cbasereferenceclock:: settimedelta**](cbasereferenceclock-settimedelta.md)auf.

Die von [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) zurückgegebenen Zeit Werte werden monoton vergrößert. Wenn Sie die Uhr wieder festlegen, meldet **GetTime** weiterhin die alte Zeit, bis die interne Uhr abfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Csystemclock-Klasse<br/>                                                                                                                                                              |
| Header<br/>  | <dl> <dt>Sysclock. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




