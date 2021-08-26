---
description: Benutzerspezifisches Ereignis, das für die Protokollierung der Initiierung von Konversationen durch Instant Messaging-Clients bereitgestellt wird.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: WPCEVENT_IM_INVITATION Ereignis (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f29b1adc556e29e03f7c8a189567b98055187f80d1574e201c54e3af0c1c0aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951390"
---
# <a name="wpcevent_im_invitation-event"></a>WPCEVENT \_ IM \_ INVITATION-Ereignis

Benutzerspezifisches Ereignis, das für die Protokollierung der Initiierung von Konversationen durch Instant Messaging-Clients bereitgestellt wird.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AppName* 
</dt> <dd>

Der Name der Anwendung, die das Ereignis generiert.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Versionszeichenfolge für die Anwendung, die das Ereignis generiert.

</dd> <dt>

*AccountName* 
</dt> <dd>

Die Identitätszeichenfolge des Instant Messaging-Kontos.

</dd> <dt>

*ConvID* 
</dt> <dd>

Der Bezeichner für die Konversation.

</dd> <dt>

*Anfordern vonIP* 
</dt> <dd>

Eine Zeichenfolge, die die IP-Adresse des Computers enthält, der die Einladung sendet.

</dd> <dt>

*Sender* 
</dt> <dd>

Die Identitätszeichenfolge des Instant Messaging-Kontos für das Konto, das die Einladung ausgibt.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**WPCFLAG \_ ISBLOCKED-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) der Informationen darüber angibt, welche Ereignisse für die Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Die Anzahl der Empfänger, die die Einladung erhalten und für die identitäten im Feld "Empfänger" definiert sind.

</dd> <dt>

*Recipient* 
</dt> <dd>

Eine durch Trennzeichen getrennte Zeichenfolge, die Identitätszeichenfolgen für das Instant Messaging-Konto für die Empfänger der Einladung enthält.

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

 

 




