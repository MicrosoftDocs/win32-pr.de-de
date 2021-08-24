---
description: Benutzerspezifisches Ereignis, das von einer Instant Messaging-Anwendung generiert wird, wenn eine Entität versucht, einer Konversation bei der Jugendkontrolle beizukommen.
ms.assetid: 5251234b-0280-4d5d-80f5-295d720a89d1
title: WPCEVENT_IM_JOIN -Ereignis (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 181bc849cf89e8a78a7a5aaad97463baf0c611d99ca0dc05caf9bfaf879eb804
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951290"
---
# <a name="wpcevent_im_join-event"></a>WPCEVENT \_ IM \_ JOIN-Ereignis

Benutzerspezifisches Ereignis, das von einer Instant Messaging-Anwendung generiert wird, wenn eine Entität versucht, einer Konversation bei der Jugendkontrolle beizukommen.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_JOIN = {0x8, 0x0, 0x10, 0x4, 0x16, 0x8, 0x8000000000000030};
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

*JoiningIP* 
</dt> <dd>

Eine Zeichenfolge, die die IP-Adresse des Computers enthält, der dieser Konversation beitritt.

</dd> <dt>

*JoiningUser* 
</dt> <dd>

Die Identitätszeichenfolge des Instant Messaging-Kontos für den Benutzer, der beitritt.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**WPCFLAG \_ ISBLOCKED-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) der Informationen darüber angibt, welche Ereignisse nicht verwendet werden und welche Steuerelemente verwendet werden.

</dd> <dt>

*MemberCount* 
</dt> <dd>

Die Anzahl der Teilnehmer, die an der Konversation teilnehmen und für die identitäten im Memberfeld definiert sind.

</dd> <dt>

*Member* 
</dt> <dd>

Eine durch Trennzeichen getrennte Zeichenfolge, die Die Identitätszeichenfolgen des Instant Messaging-Kontos für alle aktuellen Mitglieder dieser Konversation enthält.

</dd> <dt>

*Sender* 
</dt> <dd>

Die Identitätszeichenfolge des Instant Messaging-Kontos für den Benutzer, der die Anforderung zum Beitreten zur Konversation vorgibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Protokollierungs-APIs für Jugendschutz](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




