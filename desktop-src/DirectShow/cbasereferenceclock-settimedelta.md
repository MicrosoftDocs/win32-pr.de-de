---
description: Die settimedelta-Methode passt die interne Uhrzeit an.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Cbasereferenceclock. settimedelta-Methode (Ref. h)
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
ms.openlocfilehash: de58363119dc08c21d2cab0070b438ad6b4331e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367778"
---
# <a name="cbasereferenceclocksettimedelta-method"></a>Cbasereferenceclock. settimedelta-Methode

Die- `SetTimeDelta` Methode passt die interne Uhrzeit an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Timedelta* \[ atur\]
</dt> <dd>

Der Wert für die Anpassung der Uhrzeitangabe in 100-Nanosecond-Einheiten. Ein positiver Wert verschiebt die Uhr vorwärts, und ein negativer Wert verschiebt die Uhr nach unten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann von der abgeleiteten Klasse verwendet werden, um die interne Uhr anzupassen, wenn Sie von dem Gerät abweicht, das Zeit Steuerungsinformationen bereitstellt.

Die [**cbasereferenceclock:: getTime**](cbasereferenceclock-gettime.md) -Methode gibt keine abnehmenden Werte zurück. Wenn Sie die Uhr rückwärts anpassen, gibt **GetTime** den vorherigen Wert zurück, bis die Uhr diesen Wert wieder erreicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ref. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasereferenceclock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




