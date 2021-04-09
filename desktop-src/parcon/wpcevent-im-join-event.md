---
description: Pro-Benutzer-Ereignis, das von einer Instant Messaging-Anwendung generiert wird, wenn eine Entität versucht, einer Konversation in der Jugend Steuerungsmethode beizutreten.
ms.assetid: 5251234b-0280-4d5d-80f5-295d720a89d1
title: WPCEVENT_IM_JOIN-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b020eb3d4204f946002f59f472e5c95b715f88f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864768"
---
# <a name="wpcevent_im_join-event"></a>Wpcevent \_ im \_ Join-Ereignis

Pro-Benutzer-Ereignis, das von einer Instant Messaging-Anwendung generiert wird, wenn eine Entität versucht, einer Konversation in der Jugend Steuerungsmethode beizutreten.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_JOIN = {0x8, 0x0, 0x10, 0x4, 0x16, 0x8, 0x8000000000000030};
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

*Joiningip* 
</dt> <dd>

Eine Zeichenfolge, die die IP-Adresse des Computers enthält, der dieser Konversation Beitritt.

</dd> <dt>

*Joininguser* 
</dt> <dd>

Die Identitäts Zeichenfolge für das Instant Messaging-Konto für den Benutzer, der beitreten soll.

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

*Sender* 
</dt> <dd>

Die Identitäts Zeichenfolge für das Instant Messaging-Konto für den Benutzer, der die Anforderung zum beitreten an die Konversation sendet.

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

 

 




