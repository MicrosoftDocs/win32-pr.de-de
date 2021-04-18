---
description: Die GetEvent-Methode ruft ein Ereignis Handle ab, das verwendet wird, um eine Änderung in der nächsten Empfehlung zu signalisieren.
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: Camschedule. GetEvent-Methode (dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 360a4b88c8c03d2f04ad55bc65eebf6be3797c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372066"
---
# <a name="camschedulegetevent-method"></a>Camschedule. GetEvent-Methode

Die- `GetEvent` Methode ruft ein Ereignis Handle ab, das verwendet wird, um eine Änderung in der nächsten Empfehlung zu signalisieren.

## <a name="syntax"></a>Syntax


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt ein Handle für ein Ereignis zurück.

## <a name="remarks"></a>Bemerkungen

Wenn sich die nächste Anforderungszeit geändert hat und eine neue anforderungsanforderung am Anfang der Liste hinzugefügt wird, signalisiert der Scheduler dieses Ereignis. Die Uhr sollte die Methode " [**camschedule:: Empfehlung**](camschedule-advise.md) " anrufen, um den nächsten Zeitpunkt der Empfehlung zu bestimmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dsschedule. h (Include Streams. h)</dt> </dl>                                                                                |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camschedule-Klasse**](camschedule.md)
</dt> </dl>

 

 




