---
description: Pro-Benutzer-Ereignis, das von einem e-Mail-Client generiert wird, wenn ein Nachrichten Empfang in Eltern Steuerelementen versucht wird
ms.assetid: 3b8d9bac-16b0-49e9-b360-b2d6e82f1753
title: WPCEVENT_EMAIL_RECEIVED-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f14d583cadb6bc976b85953bb09ea34811a5061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215868"
---
# <a name="wpcevent_email_received-event"></a>Ereignis "wpcevent \_ -e-Mail \_ empfangen

Pro-Benutzer-Ereignis, das von einem e-Mail-Client generiert wird, wenn ein Nachrichten Empfang in Eltern Steuerelementen versucht wird


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_RECEIVED = {0x4, 0x0, 0x10, 0x4, 0x16, 0x4, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sender* 
</dt> <dd>

Der e-Mail-Konto Name der sendenden Entität.

</dd> <dt>

*AppName* 
</dt> <dd>

Der Name der e-Mail-Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Version der e-Mail-Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*Subject* 
</dt> <dd>

Die Betreffzeile der empfangenen Nachricht.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*Anzahl der Mitarbeiter* 
</dt> <dd>

Gibt die Anzahl von e-Mail-Adressen an, die die Nachricht empfangen und deren Identitäten im Feld Empfänger definiert sind.

</dd> <dt>

*Recipient* 
</dt> <dd>

Eine Zeichenfolge mit Trennzeichen, die die e-Mail-Kontonamen aller Empfänger der Nachricht enthält.

</dd> <dt>

*Attachcount* 
</dt> <dd>

Die Anzahl der Anlagen für die Nachricht.

</dd> <dt>

*AttachmentName* 
</dt> <dd>

Eine durch Trennzeichen getrennte Zeichenfolge, die die Namen aller Anhänge der Nachricht enthält.

</dd> <dt>

*ReceivedTime* 
</dt> <dd>

Der Zeitpunkt, zu dem die Nachricht empfangen wurde.

</dd> <dt>

*Emailaccount* 
</dt> <dd>

Der Name des e-Mail-Kontos für diesen Benutzer.

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

 

 




