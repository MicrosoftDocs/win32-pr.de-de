---
description: Die getdefaulttimerresolution-Methode gibt die aktuelle Auflösung des Zeit Gebers der verweisuhr zurück.
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: Cbasereferenceclock. getdefaulttimerresolution-Methode (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40a1c430f95b13086d50811e63cc2e411b3bf377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352986"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a>Cbasereferenceclock. getdefaulttimerresolution-Methode

Die `GetDefaultTimerResolution` -Methode gibt die aktuelle Auflösung des Zeit Gebers der verweisuhr zurück.

## <a name="syntax"></a>Syntax


```C++
STDMETHODIMP GetDefaultTimerResolution(
   REFERENCE_TIME *pTimerResolution
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptimerresolution* 
</dt> <dd>

Empfängt die angeforderte Zeit Geber Auflösung in 100-Nanosecond-Einheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode implementiert die [**ireferenceclocktimercontrol:: getdefaulttimerresolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ref. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasereferenceclock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




