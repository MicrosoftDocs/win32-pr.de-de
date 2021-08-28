---
description: Ereignis auf Systemebene, das durch Richtlinien für Softwareeinschränkungen (Software Restrictions Policies, SRP) generiert wird, wenn eine Anwendung durch sicherere Regeln blockiert wird.
ms.assetid: 6772a2c9-35c1-4b75-94e4-baa84af7c0ed
title: WPCEVENT_SYSTEM_APPBLOCKED Ereignis (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0444cee0a2844ae868923b5cf51923e0024c9de9a2a12ad51e20d8db9fa3b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112720"
---
# <a name="wpcevent_system_appblocked-event"></a>WPCEVENT \_ SYSTEM \_ APPBLOCKED-Ereignis

Ereignis auf Systemebene, das durch Richtlinien für Softwareeinschränkungen (Software Restrictions Policies, SRP) generiert wird, wenn eine Anwendung durch sicherere Regeln blockiert wird.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYSTEM_APPBLOCKED = {0x10, 0x0, 0x10, 0x4, 0x16, 0x10, 0x8000000000000010};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Timestamp* 
</dt> <dd>

Der Zeitpunkt, zu dem der Block aufgetreten ist.

</dd> <dt>

*UserID* 
</dt> <dd>

Die Sicherheits-ID des Benutzers, der versucht, die Anwendung zu starten.

</dd> <dt>

*Path* 
</dt> <dd>

Der Pfad zur Anwendung, die der Benutzer zu starten versucht.

</dd> <dt>

*RuleID* 
</dt> <dd>

Die ID der Regel innerhalb des Satzes sichererer Regeln für die Jugendschutz, die die Ausführung blockieren.

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

 

 




