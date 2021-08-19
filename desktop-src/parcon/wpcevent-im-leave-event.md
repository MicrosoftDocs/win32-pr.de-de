---
description: Benutzerspezifisches Ereignis, das von einem Instant Messaging-Client generiert wird, wenn ein Benutzer eine Konversation in Der Jugendschutz verlässt.
ms.assetid: e6bd6bce-9eba-4192-aac8-c9e47d7180a1
title: WPCEVENT_IM_LEAVE Ereignis (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d814f6c9d4e3ec5acd3ee3cf3a6eb6e67d315148304f2766baf45fc633fa22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951210"
---
# <a name="wpcevent_im_leave-event"></a>WPCEVENT \_ IM \_ LEAVE-Ereignis

Benutzerspezifisches Ereignis, das von einem Instant Messaging-Client generiert wird, wenn ein Benutzer eine Konversation in Der Jugendschutz verlässt.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_LEAVE = {0x9, 0x0, 0x10, 0x4, 0x16, 0x9, 0x8000000000000030};
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

Die Identitätszeichenfolge des Instant Messaging-Kontos für diesen Benutzer.

</dd> <dt>

*ConvID* 
</dt> <dd>

Der Bezeichner für diese Konversation.

</dd> <dt>

*LeavingIP* 
</dt> <dd>

Eine Zeichenfolge, die die IP-Adresse des Computers enthält, der diese Konversation verlässt.

</dd> <dt>

*LeavingUser* 
</dt> <dd>

Die Identitätszeichenfolge des Instant Messaging-Kontos für den Benutzer, der den Dienst verlässt.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**WPCFLAG \_ ISBLOCKED-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) der Informationen darüber angibt, welche Ereignisse für die Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*MemberCount* 
</dt> <dd>

Die Anzahl der Teilnehmer, die sich in der Konversation befinden und für die Identitäten im Elementfeld definiert sind.

</dd> <dt>

*Member* 
</dt> <dd>

Eine durch Trennzeichen getrennte Zeichenfolge, die Identitätszeichenfolgen des Instant Messaging-Kontos für alle aktuellen Mitglieder dieser Konversation enthält.

</dd> <dt>

*Flags* 
</dt> <dd>

Ein Wert der [**WPCFLAG \_ IM \_ LEAVE-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_leave) der Informationen darüber angibt, wann ein Teilnehmer die Instant Messaging-Interaktion verlässt.

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

 

 




