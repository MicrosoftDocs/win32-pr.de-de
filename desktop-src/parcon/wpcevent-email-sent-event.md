---
description: Benutzerspezifisches Ereignis, das von einem E-Mail-Client generiert wird, wenn versucht wird, eine Nachricht in der Elternkontrolle zu senden.
ms.assetid: c49919a2-2a03-475d-9cfa-20a960184202
title: WPCEVENT_EMAIL_SENT -Ereignis (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe3d5fb08764aa83677fcca66af7f1e3b868f2b1bdf393741865bf64fd23049
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112730"
---
# <a name="wpcevent_email_sent-event"></a>WPCEVENT \_ EMAIL \_ SENT-Ereignis

Benutzerspezifisches Ereignis, das von einem E-Mail-Client generiert wird, wenn versucht wird, eine Nachricht in der Elternkontrolle zu senden.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_SENT = {0x5, 0x0, 0x10, 0x4, 0x16, 0x5, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sender* 
</dt> <dd>

Der E-Mail-Kontoname der sendenden Entität.

</dd> <dt>

*AppName* 
</dt> <dd>

Der Name der E-Mail-Anwendung, die das Ereignis generiert.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Version der E-Mail-Anwendung, die das Ereignis generiert.

</dd> <dt>

*Subject* 
</dt> <dd>

Die Betreffzeile der empfangenen Nachricht.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**WPCFLAG \_ ISBLOCKED-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) der Informationen darüber angibt, welche Ereignisse nicht verwendet werden und welche Steuerelemente verwendet werden.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Die Anzahl der E-Mail-Empfänger, die die Nachricht empfangen und für die identitäten im Empfängerfeld definiert sind.

</dd> <dt>

*Recipient* 
</dt> <dd>

Eine durch Trennzeichen getrennte Zeichenfolge, die die E-Mail-Kontonamen aller Empfänger der Nachricht enthält.

</dd> <dt>

*AttachCount* 
</dt> <dd>

Die Anzahl der Anlagen an der Nachricht.

</dd> <dt>

*AttachmentName* 
</dt> <dd>

Eine durch Trennzeichen getrennte Zeichenfolge, die die Namen aller Anlagen der Nachricht enthält.

</dd> <dt>

*ReceivedTime* 
</dt> <dd>

Der Zeitpunkt, zu dem versucht wurde, die Nachricht zu empfangen.

</dd> <dt>

*EmailAccount* 
</dt> <dd>

Der Name des E-Mail-Kontos für diesen Benutzer.

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

 

 




