---
description: Benutzerspezifisches Ereignis, das vom Webinhaltsfilter aufgrund des Zugriffs auf eine URL generiert wurde.
ms.assetid: 636b0ce8-cf08-4536-9b41-79512b02a066
title: WPCEVENT_WEB_URLVISIT -Ereignis (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9524909ee78d14395e2f208fe265b3abc31240d2036788b8b84c4fea05aac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112700"
---
# <a name="wpcevent_web_urlvisit-event"></a>WPCEVENT \_ WEB \_ URLVISIT-Ereignis

Benutzerspezifisches Ereignis, das vom Webinhaltsfilter aufgrund des Zugriffs auf eine URL generiert wurde.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_URLVISIT = {0x3, 0x0, 0x10, 0x4, 0x18, 0x3, 0x8000000000000010};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*URL* 
</dt> <dd>

Die URL, die geöffnet werden soll.

</dd> <dt>

*Anwendung* 
</dt> <dd>

Die Anwendung, die das Ereignis generiert.

</dd> <dt>

*Version* 
</dt> <dd>

Die Versionszeichenfolge für die Anwendung.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**WPCFLAG \_ ISBLOCKED-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) der Informationen darüber angibt, welche Ereignisse nicht verwendet werden und welche Steuerelemente verwendet werden.

</dd> <dt>

*RatingSystemID* 
</dt> <dd>

Eine GUID, die das aktuelle Bewertungssystem identifiziert.

</dd> <dt>

*CatCount* 
</dt> <dd>

Die Anzahl der blockierten Einträge im Kategoriefeld.

</dd> <dt>

*Kategorie* 
</dt> <dd>

Eine durch Trennzeichen getrennte Zeichenfolge von Kategoriebezeichnern, die blockiert werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verwenden von Protokollierungs-APIs für Jugendschutz](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




