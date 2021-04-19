---
description: Gibt an, dass die DVD-Wiedergabe beendet wurde. Dieses Ereignis wird gesendet, wenn ein Titel oder ein Kapitel abgeschlossen ist und der DVD-Navigator keine andere Verzweigungs Anweisung für die nachfolgende Wiedergabe findet. Das Ereignis wird nicht gesendet, wenn die Anwendung die Wiedergabe beendet.
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: EC_DVD_PLAYBACK_STOPPED (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_STOPPED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2304d83aea532b764777b683c57c3bdd4d5df79a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367635"
---
# <a name="ec_dvd_playback_stopped"></a>EC- \_ DVD- \_ Wiedergabe \_ beendet

Gibt an, dass die DVD-Wiedergabe beendet wurde. Dieses Ereignis wird gesendet, wenn ein Titel oder ein Kapitel abgeschlossen ist und der [DVD-Navigator](dvd-navigator-filter.md) keine andere Verzweigungs Anweisung für die nachfolgende Wiedergabe findet. Das Ereignis wird nicht gesendet, wenn die Anwendung die Wiedergabe beendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Ein Member der [**DVD- \_ PB \_**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) hat die Enumeration beendet und gibt an, warum die Wiedergabe beendet wurde.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird in allen Domänen ausgelöst.

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

 

 




