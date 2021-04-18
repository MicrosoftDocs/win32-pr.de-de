---
description: Die Methode "Request" verteilt alle Anforderungen, die für eine angegebene Zeit oder eine frühere Zeit geplant sind.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: Camschedule. Empfehlung-Methode (dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Advise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70880243cef294ebe747463cd11737027faf9277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371179"
---
# <a name="camscheduleadvise-method"></a>Camschedule. Empfehlung-Methode

Die- `Advise` Methode sendet alle Anforderungen, die für eine angegebene Zeit oder früher geplant sind.

## <a name="syntax"></a>Syntax


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rttime* \[ atur\]
</dt> <dd>

Der-Wert, der die aktuelle Verweis Zeit angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Verweis Zeitpunkt der nächsten geplanten anforderungsanforderung oder die maximale Zeit zurück, \_ Wenn keine Links vorhanden sind.

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode von der Uhr aufgerufen wird, wird die aktuelle Verweis Zeit angegeben. Der Planer bestimmt, welche Anforderungs Anforderungen ggf. abgelaufen sind, und sendet Sie. Wenn eine One-Shot-Anforderung abläuft, wird Sie vom Scheduler gelöscht. Wenn eine regelmäßige Anforderung abläuft, plant der Scheduler diese für den nächsten Zeitpunkt der Empfehlung erneut. Die-Methode gibt die Zeit der nächsten ausstehenden Anforderung zurück.

Zum Senden einer Benachrichtigungs Anforderung signalisiert der Planer das Ereignis oder die Semaphor, die im *hnotify* -Parameter der Methode " [**camschedule:: addadvisepacket**](camschedule-addadvisepacket.md) " angegeben sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dsschedule. h (Include Streams. h)</dt> </dl>                                                                                |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camschedule-Klasse**](camschedule.md)
</dt> </dl>

 

 




