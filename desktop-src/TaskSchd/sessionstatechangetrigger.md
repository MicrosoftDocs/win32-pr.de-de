---
title: SessionStateChangeTrigger-Objekt
description: Skriptobjekt, das Aufgaben für Konsolenverbindungs- oder -trennungsbenachrichtigungen, Remoteverbindungs- oder Trennungsbenachrichtigungen oder Benachrichtigungen zum Sperren oder Entsperren der Arbeitsstation auslöst.
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- SessionStateChangeTrigger-Objekt Taskplaner
- SessionStateChangeTrigger-Objekt Taskplaner beschrieben
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4fe4f0e328adc44d4330a1bdef81b5dca62be53c7add2589b6e7c537bbd38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118858834"
---
# <a name="sessionstatechangetrigger-object"></a>SessionStateChangeTrigger-Objekt

Skriptobjekt, das Aufgaben für Konsolenverbindungs- oder -trennungsbenachrichtigungen, Remoteverbindungs- oder Trennungsbenachrichtigungen oder Benachrichtigungen zum Sperren oder Entsperren der Arbeitsstation auslöst.

## <a name="members"></a>Member

Das **SessionStateChangeTrigger-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **SessionStateChangeTrigger-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                | Zugriffstyp           | Beschreibung                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögern**](sessionstatechangetrigger-delay.md)<br/>             | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, wie lange eine Verzögerung dauert, bevor ein Task gestartet wird, nachdem eine Änderung des Terminalserver-Sitzungszustands erkannt wurde, oder legt diesen fest.<br/>                                         |
| [**Aktiviert**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft einen booleschen Wert ab, der angibt, ob der Trigger aktiviert ist, oder legt diesen fest.<br/>                                                              |
| [**EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft das Datum und die Uhrzeit der Deaktivierung des Triggers ab oder legt diese fest. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.<br/>               |
| [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft die maximale Zeitspanne ab, in der der Task vom Trigger gestartet werden kann, oder legt diese fest.<br/>                                                 |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft den Bezeichner für den Trigger ab oder legt den Bezeichner fest.<br/>                                                                                             |
| [**Wiederholen**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft einen Wert ab, der angibt, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster nach dem Starten der Aufgabe wiederholt wird, oder legt diesen fest.<br/> |
| [**StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | Lesen/Schreiben<br/> | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft das Datum und die Uhrzeit der Aktivierung des Triggers ab oder legt diese fest.<br/>                                                                            |
| [**StateChange**](sessionstatechangetrigger-statechange.md)<br/> | Lesen/Schreiben<br/> | Ruft die Art der Terminalserversitzungsänderung ab, die einen Taskstart auslösen würde, oder legt diese fest.<br/>                                                                                                      |
| [**Typ**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | Schreibgeschützt<br/>  | Geerbt [](trigger.md) vom Trigger-Objekt. Ruft den Typ des Triggers ab.<br/>                                                                                                            |
| [**Userid**](sessionstatechangetrigger-userid.md)<br/>           | Lesen/Schreiben<br/> | Ruft den Benutzer für die Terminalserversitzung ab oder legt den Benutzer fest. Wenn eine Sitzungszustandsänderung für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.<br/>                                                               |



 

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben eigener XML-Daten für eine Aufgabe wird ein Trigger zur Änderung des Sitzungszustands mithilfe des [**SessionStateChangeTrigger-Elements**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Triggercollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





