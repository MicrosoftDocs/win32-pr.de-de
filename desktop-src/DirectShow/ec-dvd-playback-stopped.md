---
description: Gibt an, dass die DVD-Wiedergabe beendet wurde. Dieses Ereignis wird gesendet, wenn ein Titel oder Kapitel abgeschlossen ist und der DVD-Navigator keine andere Verzweigungsanweisung für die nachfolgende Wiedergabe findet. Das Ereignis wird nicht gesendet, wenn die Anwendung die Wiedergabe beendet.
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: EC_DVD_PLAYBACK_STOPPED (Dvdevcode.h)
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
ms.openlocfilehash: 7a5f0b1b66e9d78309e33981910da467757a2b606b967cee5b78e86c4cc0049b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820456"
---
# <a name="ec_dvd_playback_stopped"></a>EC \_ DVD PLAYBACK STOPPED (EC-DVD-WIEDERGABE \_ \_ BEENDET)

Gibt an, dass die DVD-Wiedergabe beendet wurde. Dieses Ereignis wird gesendet, wenn ein Titel oder Kapitel abgeschlossen ist und [der DVD-Navigator](dvd-navigator-filter.md) keine andere Verzweigungsanweisung für die nachfolgende Wiedergabe findet. Das Ereignis wird nicht gesendet, wenn die Anwendung die Wiedergabe beendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Ein Member der [**PB \_ \_ STOPPED-Enumeration der DVD,**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) der angibt, warum die Wiedergabe beendet wurde.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Ereignis wird in allen Domänen ausgelöst.

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

 

 




