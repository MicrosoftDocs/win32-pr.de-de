---
description: Die Advise-Methode versendet alle Anforderungen, die für einen bestimmten Zeitpunkt oder früher geplant sind.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: CAMSchedule.Advise-Methode (Dsschedule.h)
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
ms.openlocfilehash: a0943479aaa7fe2e6d699bba147977a73f48fc31186fb64ea26a211e2ea31d8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757790"
---
# <a name="camscheduleadvise-method"></a>CAMSchedule.Advise-Methode

Die `Advise` -Methode gibt alle Anforderungen weiter, die für einen bestimmten Zeitpunkt oder früher geplant sind.

## <a name="syntax"></a>Syntax


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtTime* \[ Ref\]
</dt> <dd>

Ein -Wert, der die aktuelle Verweiszeit angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Bezugszeit der nächsten geplanten Advise-Anforderung zurück, oder MAX \_ TIME, wenn keine noch verfügbar sind.

## <a name="remarks"></a>Hinweise

Wenn die Uhr diese Methode aufruft, gibt sie die aktuelle Verweiszeit an. Der Planer bestimmt, welche Advise-Anforderungen abgelaufen sind (falls möglich) und versendet sie. Wenn eine einmalige Anforderung abläuft, löscht der Planer sie. Wenn eine regelmäßige Anforderung abläuft, wird sie vom Planer für den nächsten Zeitpunkt der Beratung neu geplant. Die -Methode gibt die Zeit der nächsten ausstehenden Anforderung zurück.

Um eine Advise-Anforderung zu senden, signalisiert der Planer das Ereignis oder Semaphor, das bzw. das im *hNotify-Parameter* der [**METHODE WEBCAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) angegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dsschedule.h (include Streams.h)</dt> </dl>                                                                                |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CAMSchedule-Klasse**](camschedule.md)
</dt> </dl>

 

 




