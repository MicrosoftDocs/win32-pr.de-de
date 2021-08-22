---
title: IdleTrigger-Objekt
description: Skripterstellungsobjekt, das einen Trigger darstellt, der eine Aufgabe startet, wenn eine Leerlaufbedingung auftritt.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- Leerlauftrigger Taskplaner , Objekt
- IdleTrigger-Taskplaner
- IdleTrigger-Objekt Taskplaner , beschrieben
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a3c538dbd04f3eb20a86f495fcf4a8b027b51fbe5cd6443cd8ff3a69ac6ff5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621140"
---
# <a name="idletrigger-object"></a>IdleTrigger-Objekt

Skripterstellungsobjekt, das einen Trigger darstellt, der eine Aufgabe startet, wenn eine Leerlaufbedingung auftritt. Informationen zu Leerlaufbedingungen finden Sie unter [Aufgaben-Leerlaufbedingungen.](task-idle-conditions.md)

## <a name="members"></a>Member

Das **IdleTrigger-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **IdleTrigger-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | Beschreibung                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft einen booleschen Wert ab, der angibt, ob der Trigger aktiviert ist, oder legt diesen fest.<br/>                                                              |
| [EndBoundary](trigger-endboundary.md)<br/>                   | Lesen/Schreiben<br/> | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft das Datum und die Uhrzeit der Deaktivierung des Triggers ab oder legt diese fest. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft die maximale Zeitdauer ab, in der der Task vom Trigger gestartet werden kann, oder legt diese fest.<br/>                                                 |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lesen/Schreiben<br/> | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft den Bezeichner für den Trigger ab oder legt den Bezeichner fest.<br/>                                                                                             |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft einen Wert ab, der angibt, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde, oder legt diesen fest.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft das Datum und die Uhrzeit der Aktivierung des Triggers ab oder legt diese fest.<br/>                                                                            |
| [**Typ**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Schreibgeschützt<br/>  | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft den Typ des Triggers ab.<br/>                                                                                                            |



 

## <a name="remarks"></a>Hinweise

Ein Trigger im Leerlauf löst nur dann eine Taskaktion aus, wenn der Computer nach der Startgrenze des Triggers in den Leerlaufzustand übergeht.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird ein Trigger im Leerlauf mithilfe des [**IdleTrigger-Elements**](taskschedulerschema-idletrigger-triggergroup-element.md) des Taskplaner angegeben.

Wenn eine Aufgabe durch einen Trigger im Leerlauf ausgelöst wird, wird die [**IdleSettings.WaitTimeout-Eigenschaft**](idlesettings-waittimeout.md) ignoriert.

Wenn die erste Instanz einer Aufgabe mit einem Trigger im Leerlauf noch ausgeführt wird, wird die Aufgabe nur einmal ohne Wiederholungen gestartet, auch wenn in der [**Wiederholungseigenschaft**](trigger-repetition.md) mehrere Wiederholungen definiert sind. Dieses Verhalten tritt nicht auf, wenn die Aufgabe allein beendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[Taskplaner Objekte](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





