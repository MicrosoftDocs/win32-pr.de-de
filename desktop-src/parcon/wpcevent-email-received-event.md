---
description: Benutzerspezifisches Ereignis, das von einem E-Mail-Client generiert wird, wenn versucht wird, eine Nachricht in der Jugendschutz-Steuerung zu empfangen.
ms.assetid: 3b8d9bac-16b0-49e9-b360-b2d6e82f1753
title: WPCEVENT_EMAIL_RECEIVED-Ereignis (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81a51e79125403504aae2ed6e823c10044ffc35ed36ff139e8333f955338d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951560"
---
# <a name="wpcevent_email_received-event"></a>WPCEVENT \_ EMAIL \_ RECEIVED-Ereignis

Benutzerspezifisches Ereignis, das von einem E-Mail-Client generiert wird, wenn versucht wird, eine Nachricht in der Jugendschutz-Steuerung zu empfangen.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_RECEIVED = {0x4, 0x0, 0x10, 0x4, 0x16, 0x4, 0x8000000000000030};
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

Ein Wert der [**WPCFLAG \_ ISBLOCKED-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) der Informationen darüber angibt, welche Ereignisse für die Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Die Anzahl der E-Mail-Empfänger, die die Nachricht empfangen, und die identitäten im Feld "Empfänger" definiert sind.

</dd> <dt>

*Recipient* 
</dt> <dd>

Eine zeichenfolge mit Trennzeichen, die die E-Mail-Kontonamen aller Empfänger der Nachricht enthält.

</dd> <dt>

*AttachCount* 
</dt> <dd>

Die Anzahl der Anlagen für die Nachricht.

</dd> <dt>

*AttachmentName* 
</dt> <dd>

Eine zeichenfolge mit Trennzeichen, die die Namen aller Anlagen der Nachricht enthält.

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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Protokollierungs-APIs für Jugendschutz](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




