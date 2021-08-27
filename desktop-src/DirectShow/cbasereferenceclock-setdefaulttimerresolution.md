---
description: Die SetDefaultTimerResolution-Methode legt die Auflösung des Zeitgebers der Verweisuhr fest.
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: CBaseReferenceClock.SetDefaultTimerResolution-Methode (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 980f31856aba14079da0f5b9625dca40846255d6f02361b2798d7c38c1cd4f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087420"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a>CBaseReferenceClock.SetDefaultTimerResolution-Methode

Die `SetDefaultTimerResolution` -Methode legt die Auflösung des Zeitgebers der Verweisuhr fest.

## <a name="syntax"></a>Syntax


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*timerResolution* 
</dt> <dd>

Minimale Timerauflösung in Einheiten von 100 Nanosekunden. Wenn der Wert 0 (null) ist, bricht die Referenzuhr ihre vorherige Anforderung ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Methode implementiert die [**IReferenceClockTimerControl::SetDefaultTimerResolution-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Refclock.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseReferenceClock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




