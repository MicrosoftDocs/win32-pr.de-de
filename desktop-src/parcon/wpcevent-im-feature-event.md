---
description: Benutzerspezifisches Ereignis, das von einem Instant Messaging-Client generiert wird, wenn definierte Features in der Jugendschutzfunktion verwendet werden.
ms.assetid: 45e80314-90b1-4fcf-9c8f-c9840ae1775b
title: WPCEVENT_IM_FEATURE Ereignis (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8046e755540a2282e84ea25c5278cf0c0b113264e78a3db31b6bd8a42de599cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951442"
---
# <a name="wpcevent_im_feature-event"></a>WPCEVENT \_ IM \_ FEATURE-Ereignis

Benutzerspezifisches Ereignis, das von einem Instant Messaging-Client generiert wird, wenn definierte Features in der Jugendschutzfunktion verwendet werden.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_FEATURE = {0xb, 0x0, 0x10, 0x4, 0x16, 0xb, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AppName* 
</dt> <dd>

Der Name der Instant Messaging-Anwendung.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Versionszeichenfolge für die Anwendung.

</dd> <dt>

*AccountName* 
</dt> <dd>

Der Name des Instant Messaging-Kontos dieses Benutzers.

</dd> <dt>

*ConvID* 
</dt> <dd>

Die ID für diese Konversation.

</dd> <dt>

*MediaType* 
</dt> <dd>

Ein Wert der [**WPCFLAG \_ IM \_ FEATURE-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_feature) der Informationen zu den Features angibt, auf die während einer Sofortnachrichteninteraktion zugegriffen wird.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**WPCFLAG \_ ISBLOCKED-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) der Informationen darüber angibt, welche Ereignisse für die Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Die Anzahl der Instant Messaging-Benutzer, die das Feature empfangen und für die identitäten im Feld "Empfänger" definiert sind.

</dd> <dt>

*Recipient* 
</dt> <dd>

Eine zeichenfolge mit Trennzeichen, die Instant Messaging-Kontoidentitäten aller Benutzer enthält, die das Feature erhalten.

</dd> <dt>

*Sender* 
</dt> <dd>

Der Name des Instant Messaging-Kontos für den Benutzer, der das Feature ausgibt.

</dd> <dt>

*SenderIP* 
</dt> <dd>

Die IP-Adresse des Computers des Absenders.

</dd> <dt>

*Daten* 
</dt> <dd>

Die Beschreibung der Daten in der Funktion.

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

 

 




