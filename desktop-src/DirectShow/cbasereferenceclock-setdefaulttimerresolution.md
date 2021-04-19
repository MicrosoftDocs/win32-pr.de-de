---
description: Die setdefaulttimerresolution-Methode legt die Auflösung des Zeit Gebers der verweisuhr fest.
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: Cbasereferenceclock. setdefaulttimerresolution-Methode (Ref. h)
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
ms.openlocfilehash: 146162784ad52a7f7930613ec5c648e40d22900f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366873"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a>Cbasereferenceclock. setdefaulttimerresolution-Methode

Die `SetDefaultTimerResolution` -Methode legt die Auflösung des Zeit Gebers der verweisuhr fest.

## <a name="syntax"></a>Syntax


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*timerresolution* 
</dt> <dd>

Minimale Zeit Geber Auflösung in 100-Nanosecond-Einheiten. Wenn der Wert 0 (null) ist, bricht die Referenzuhr die vorherige Anforderung ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode implementiert die [**ireferenceclocktimercontrol:: setdefaulttimerresolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ref. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasereferenceclock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




