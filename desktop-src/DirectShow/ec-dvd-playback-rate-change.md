---
description: Signalisiert, dass eine Änderungs Rate bei der DVD-Wiedergabe initiiert wurde.
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: EC_DVD_PLAYBACK_RATE_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_RATE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 20ddc41fd70906fabc522daa4dcb7714b71e4251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366007"
---
# <a name="ec_dvd_playback_rate_change"></a>Änderung der EC- \_ DVD- \_ Wiedergabe \_ Rate \_

Signalisiert, dass eine Änderungs Rate bei der DVD-Wiedergabe initiiert wurde.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Lange Angabe der neuen Wiedergabe Rate. Der Wert ist die tatsächliche Wiedergabe Rate multipliziert mit 10.000, sodass die Wiedergabe Rate 10000,0/ *lParam1* entspricht. Werte kleiner als 0 (null) geben den umgekehrten Wiedergabemodus an, und Werte größer als 0 (null) geben den vorwärts Wiedergabemodus

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird in der Titel Domäne ausgelöst.

Die Wiedergabe *Rate* ist die Umkehrung der Wiedergabe *Geschwindigkeit*. Wenn die Wiedergabegeschwindigkeit beispielsweise 2 x beträgt, ist die Rate 0,5.

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

 

 




