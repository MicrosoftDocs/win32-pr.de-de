---
description: Ereignis pro Benutzer zur Protokollierung der Initiierung von Konversationen durch Instant Messaging-Clients.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: WPCEVENT_IM_INVITATION-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87c9d7e90eaa901b5e18a072e03e3112ee8c2934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363661"
---
# <a name="wpcevent_im_invitation-event"></a>Wpcevent \_ im- \_ Einladungs Ereignis

Ereignis pro Benutzer zur Protokollierung der Initiierung von Konversationen durch Instant Messaging-Clients.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AppName* 
</dt> <dd>

Der Name der Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Versions Zeichenfolge für die Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*AccountName* 
</dt> <dd>

Die Identitäts Zeichenfolge für das Instant Messaging-Konto.

</dd> <dt>

*Geseld* 
</dt> <dd>

Der Bezeichner für die Konversation.

</dd> <dt>

*Requestingip* 
</dt> <dd>

Eine Zeichenfolge, die die IP-Adresse des Computers enthält, von dem die Einladung gesendet wird.

</dd> <dt>

*Sender* 
</dt> <dd>

Die Identitäts Zeichenfolge für das Instant Messaging-Konto für das Konto, von dem die Einladung ausgegeben wird.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*Anzahl der Mitarbeiter* 
</dt> <dd>

Die Anzahl der Empfänger, die die Einladung erhalten und deren Identitäten im Feld Empfänger definiert sind.

</dd> <dt>

*Recipient* 
</dt> <dd>

Eine durch Trennzeichen getrennte Zeichenfolge, die für die Empfänger der Einladung Instant Messaging-Konto Identitäts Zeichenfolgen enthält.

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

 

 




