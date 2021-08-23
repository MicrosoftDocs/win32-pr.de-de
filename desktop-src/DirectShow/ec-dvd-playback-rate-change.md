---
description: Signalisiert, dass eine Änderung der Rate bei der DVD-Wiedergabe initiiert wurde.
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: EC_DVD_PLAYBACK_RATE_CHANGE (Dvdevcode.h)
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
ms.openlocfilehash: 8de40dc8fd7f70dda522f4d1faf34f8c05059c6928f80a141d7ac9ae1889ecec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823680"
---
# <a name="ec_dvd_playback_rate_change"></a>ÄNDERUNG DER \_ \_ WIEDERGABERATE DER \_ \_ EC-DVD

Signalisiert, dass eine Änderung der Rate bei der DVD-Wiedergabe initiiert wurde.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

LONG gibt die neue Wiedergaberate an. Der Wert ist die tatsächliche Wiedergaberate multipliziert mit 10.000, sodass die Wiedergaberate 10000,0 */lParam1 entspricht.* Werte kleiner als 0 (null) geben den Reversewiedergabemodus an, und Werte größer als 0 (null) geben den Vorwärtswiedergabemodus an.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Ereignis wird in der Titeldomäne ausgelöst.

Die *Wiedergaberate* ist die Umkehrung der *Wiedergabegeschwindigkeit.* Wenn die Wiedergabegeschwindigkeit beispielsweise 2x beträgt, beträgt die Rate 0,5.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode.h (include Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> <dt>

[DVD-Ereignisbenachrichtigungscodes](dvd-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




