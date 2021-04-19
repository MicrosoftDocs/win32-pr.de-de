---
description: Die triggerthread-Methode aktiviert den Arbeits Thread, der die Planung verarbeitet.
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: Cbasereferenceclock. triggerthread-Methode (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.TriggerThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f18b4f7dee15ea95046091da006f537830fcbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369235"
---
# <a name="cbasereferenceclocktriggerthread-method"></a>Cbasereferenceclock. triggerthread-Methode

Die- `TriggerThread` Methode aktiviert den Arbeits Thread, der die Planung verarbeitet.

## <a name="syntax"></a>Syntax


```C++
void TriggerThread();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Uhr verwendet einen Arbeits Thread, der die Methode " [**camschedule:: Empfehlung**](camschedule-advise.md) " zu den entsprechenden Zeitpunkten aufruft. Von der abgeleiteten Klasse kann aufgerufen `TriggerThread` werden, um den Thread zu reaktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ref. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasereferenceclock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




