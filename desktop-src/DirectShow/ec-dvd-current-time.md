---
description: Signalisiert den Anfang jeder Video Object Unit (vobu), ein Video Segment, das zwischen 0,4 und 1,0 Sekunden lang ist.
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: EC_DVD_CURRENT_TIME (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0f1bb2f5f31efa881917ac71ea381cc0a82e8744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354142"
---
# <a name="ec_dvd_current_time"></a>\_ \_ aktuelle \_ Uhrzeit der EC-DVD

Signalisiert den Anfang jeder Video Object Unit (vobu), ein Video Segment, das zwischen 0,4 und 1,0 Sekunden lang ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** -Wert, der den aktuellen Wiedergabezeit Code in einem Binärformat (Binary Coded Decimal, BCD), Minuten, Sekunden, Frames (hh: mm: SS: FF) angibt. Member der [**DVD- \_ Zeit Code**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) Struktur.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Boolescher Wert (**boolescher** Wert), der den Timecode angibt. NULL (0) gibt 25 Frames pro Sekunde an, 1 gibt 30 Frames pro Sekunde an (nicht gelöscht). Der Wert 2 gibt an, dass die Wiedergabezeit nicht bestimmt werden kann.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Nur einfache lineare Filme signalisieren dieses Ereignis.

Dieses Ereignis wird in der Titel Domäne ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode. h (Include DShow. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> <dt>

[DVD-Ereignis Benachrichtigungs Codes](dvd-notification-codes.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




