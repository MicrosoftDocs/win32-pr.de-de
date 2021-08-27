---
description: Die TriggerThread-Methode reaktiviert den Arbeitsthread, der die Planung verarbeitet.
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: CBaseReferenceClock.TriggerThread-Methode (Refclock.h)
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
ms.openlocfilehash: a8b53af246e029b5142b68840cfde0e776208e3c51093438042dd74f42a1b3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076440"
---
# <a name="cbasereferenceclocktriggerthread-method"></a>CBaseReferenceClock.TriggerThread-Methode

Die `TriggerThread` -Methode reaktiviert den Arbeitsthread, der die Planung verarbeitet.

## <a name="syntax"></a>Syntax


```C++
void TriggerThread();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die Uhr verwendet einen Arbeitsthread, der die [**METHODE WEBCAMSchedule::Advise**](camschedule-advise.md) zu geeigneten Zeiten aufruft. Die abgeleitete Klasse kann `TriggerThread` aufrufen, um den Thread zu reaktiven.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Refclock.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseReferenceClock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




