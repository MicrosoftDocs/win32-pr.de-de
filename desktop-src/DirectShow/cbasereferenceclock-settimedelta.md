---
description: Die SetTimeDelta-Methode passt die interne Uhrzeit an.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: CBaseReferenceClock.SetTimeDelta-Methode (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac9eba5337fa43e43e3b7a45a7a92263fd4e6d69388185a2096c1a270590e482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403439"
---
# <a name="cbasereferenceclocksettimedelta-method"></a>CBaseReferenceClock.SetTimeDelta-Methode

Die `SetTimeDelta` -Methode passt die interne Uhrzeit an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TimeDelta* \[ Ref\]
</dt> <dd>

Betrag zum Anpassen der Uhrzeit in Einheiten von 100 Nanosekunden. Ein positiver Wert verschiebt die Uhr vorwärts, und ein negativer Wert verschiebt die Uhr rückwärts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Die abgeleitete Klasse kann diese Methode verwenden, um die interne Uhr anzupassen, wenn sie vom Gerät abweicht, das Zeitsteuerungsinformationen bereitstellt.

Die [**CBaseReferenceClock::GetTime-Methode**](cbasereferenceclock-gettime.md) gibt nie abnehmende Werte zurück. Wenn Sie die Uhr rückwärts anpassen, gibt **GetTime** den vorherigen Wert zurück, bis die Uhr diesen Wert erneut erreicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Refclock.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseReferenceClock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




