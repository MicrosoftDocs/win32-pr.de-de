---
description: Das Ereignis auf System Ebene, das von Richtlinien für Software Einschränkungen (SRP) generiert wird, wenn eine Anwendung durch sicherere Regeln blockiert wird.
ms.assetid: 6772a2c9-35c1-4b75-94e4-baa84af7c0ed
title: WPCEVENT_SYSTEM_APPBLOCKED-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c3f6255911f59717c1fa594aee4bfc49f6c5a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350202"
---
# <a name="wpcevent_system_appblocked-event"></a>Wpcevent \_ System \_ appblockierte-Ereignis

Das Ereignis auf System Ebene, das von Richtlinien für Software Einschränkungen (SRP) generiert wird, wenn eine Anwendung durch sicherere Regeln blockiert wird.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYSTEM_APPBLOCKED = {0x10, 0x0, 0x10, 0x4, 0x16, 0x10, 0x8000000000000010};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zeitstempel* 
</dt> <dd>

Der Zeitpunkt, zu dem der-Block aufgetreten ist.

</dd> <dt>

*UserID* 
</dt> <dd>

Die Sicherheits-ID des Benutzers, der versucht, die Anwendung zu starten.

</dd> <dt>

*Pfad* 
</dt> <dd>

Der Pfad zu der Anwendung, die vom Benutzer gestartet werden soll.

</dd> <dt>

*RuleID* 
</dt> <dd>

Die ID der Regel innerhalb des Satzes von Eltern Steuerelementen sicherere Regeln, die die Ausführung blockieren.

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

 

 




