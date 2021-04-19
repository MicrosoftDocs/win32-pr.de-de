---
description: Pro-Benutzer-Ereignis, das durch den Versuch generiert wurde, Inhalte mit einer Medien Anwendung wiederzugeben, die mit Jugendschutz Elementen verbunden ist.
ms.assetid: 478cc11e-afbd-411a-ab84-b8ca7c3aa503
title: WPCEVENT_MEDIA_PLAYBACK-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdf4e884cc0e87f579d245676f78232a5ae0177
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361128"
---
# <a name="wpcevent_media_playback-event"></a>Wpcevent- \_ Medien \_ Wiedergabe Ereignis

Pro-Benutzer-Ereignis, das durch den Versuch generiert wurde, Inhalte mit einer Medien Anwendung wiederzugeben, die mit Jugendschutz Elementen verbunden ist.


```C++
const EVENT_DESCRIPTOR WPCEVENT_MEDIA_PLAYBACK = {0x6, 0x0, 0x10, 0x4, 0x16, 0x6, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AppName* 
</dt> <dd>

Der Name der Medien Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Version der Medien Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*MediaType* 
</dt> <dd>

Ein Wert der [**WPC \_ \_ Medientyp**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_type) -Enumeration, der Informationen zum Typ der Mediendatei angibt, auf die zugegriffen wird.

</dd> <dt>

*Pfad* 
</dt> <dd>

Der Pfad zur Quelle des Medien Inhalts.

</dd> <dt>

*Titel* 
</dt> <dd>

Die Titel Metadaten für den Inhalt.

</dd> <dt>

*PML* 
</dt> <dd>

Die Jugend Verwaltungsebene.

</dd> <dt>

*Aufzunehmen* 
</dt> <dd>

Die Album Metadaten für den Inhalt.

</dd> <dt>

*Explizite* 
</dt> <dd>

Ein Wert der [**\_ \_ expliziten**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_explicit) Enumeration von WPC-Medien, der Informationen zur expliziten Bewertung der Mediendatei angibt.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Protokollierungs-APIs für Eltern Steuerelemente](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ Conversation ationinitevent**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




