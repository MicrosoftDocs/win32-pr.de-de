---
description: Pro Benutzer-Ereignis, das von einem Instant Messaging-Client generiert wird, wenn ein Benutzer eine Konversation in Eltern Steuerelementen verlässt.
ms.assetid: e6bd6bce-9eba-4192-aac8-c9e47d7180a1
title: WPCEVENT_IM_LEAVE-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260833a30f08330da9c622faae06f76b5d79e682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369034"
---
# <a name="wpcevent_im_leave-event"></a>Wpcevent- \_ im- \_ Leave-Ereignis

Pro Benutzer-Ereignis, das von einem Instant Messaging-Client generiert wird, wenn ein Benutzer eine Konversation in Eltern Steuerelementen verlässt.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_LEAVE = {0x9, 0x0, 0x10, 0x4, 0x16, 0x9, 0x8000000000000030};
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

Die Identitäts Zeichenfolge für das Instant Messaging-Konto für diesen Benutzer.

</dd> <dt>

*Geseld* 
</dt> <dd>

Der Bezeichner für diese Konversation.

</dd> <dt>

*Leavingip* 
</dt> <dd>

Eine Zeichenfolge, die die IP-Adresse des Computers enthält, der diese Konversation verlässt.

</dd> <dt>

*Leavinguser* 
</dt> <dd>

Die Identitäts Zeichenfolge für das Instant Messaging-Konto für den Benutzer, der Sie verlässt.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*MemberCount* 
</dt> <dd>

Die Anzahl der Teilnehmer, die sich in der Konversation befinden und Identitäten im Element Feld definiert sind.

</dd> <dt>

*Member* 
</dt> <dd>

Eine durch Trennzeichen getrennte Zeichenfolge, die für alle aktuellen Member dieser Konversation Konto Identitäts Zeichenfolgen für Instant Messaging enthält.

</dd> <dt>

*Flags* 
</dt> <dd>

Ein Wert der [**wpcflag in \_ \_ Leave**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_leave) -Enumeration, die Informationen darüber angibt, wann ein Teilnehmer die sofortige Messaging Interaktion verlässt.

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

 

 




