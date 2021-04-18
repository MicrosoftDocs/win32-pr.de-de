---
description: Die getprivatetime-Methode ruft die Echt Zeit von der Uhr ab.
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: Cbasereferenceclock. getprivatetime-Methode (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 387df10472e4913d33722492bf07601faf08e3ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352101"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a>Cbasereferenceclock. getprivatetime-Methode

Die- `GetPrivateTime` Methode ruft die Echt Zeit von der Uhr ab.

## <a name="syntax"></a>Syntax


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die aktuelle Uhrzeit in 100-Nanosecond-Einheiten zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt die von der Uhr gemeldete Echt Zeit zurück. Externe Aufrufer verwenden die [**cbasereferenceclock:: getTime**](cbasereferenceclock-gettime.md) -Methode, die diese Methode aufruft. Anders als bei der **GetTime** -Methode kann die interne Uhr rückwärts gehen. Wenn dies der Fall ist, gibt die **GetTime** -Methode weiterhin den Zeitpunkt der letzten Meldung zurück, bis die `GetPrivateTime` Methode abfängt.

Diese Methode gibt die Systemzeit zurück. Überschreiben Sie diese Methode, wenn die Uhr die Zeit aus einer anderen Quelle erhält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ref. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasereferenceclock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




