---
title: "\". Type\"-Eigenschaft"
description: Ruft bei der Skripterstellung den Typ des Auslösers ab.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Type-Eigenschafts Taskplaner
- Type-Eigenschafts Taskplaner, Auslöserobjekt
- Auslöse Objekt Taskplaner, Typeigenschaft
topic_type:
- apiref
api_name:
- Trigger.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2cef2d6ae33ceeac028e10a0f545afbc0a0ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740792"
---
# <a name="triggertype-property"></a>". Type"-Eigenschaft

Ruft bei der Skripterstellung den Typ des Auslösers ab. Der auslösertyp wird beim Erstellen des Auslösers definiert und kann später nicht geändert werden. Weitere Informationen zum Erstellen eines Auslösers finden Sie unter [**TriggerCollection. Create**](triggercollection-create.md).

## <a name="syntax"></a>Syntax


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a>Eigenschaftswert

Einer der folgenden [**Aufgaben \_ löst \_ Typ2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) Enumerationswerte aus.



| Wert                                                                                                                                                                                                                                                                                | Bedeutung                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**Aufgabe \_ Auslöse \_ Ereignis**</dt> <dt>0</dt> </dl>                                                 | Startet die Aufgabe, wenn ein bestimmtes Ereignis auftritt.<br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**Aufgabe \_ Auslöse \_ Zeit**</dt> <dt>1</dt> </dl>                                                    | Startet die Aufgabe zu einem bestimmten Zeitpunkt.<br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**Aufgabe \_ Auslösung \_ täglich**</dt> <dt>2</dt> </dl>                                                 | Startet die Aufgabe täglich.<br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**Aufgabe \_ Auslösung \_ wöchentlich**</dt> <dt>3</dt> </dl>                                              | Startet die Aufgabe wöchentlich.<br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**Aufgabe \_ Auslösung \_ monatlich**</dt> <dt>4</dt> </dl>                                           | Startet die Aufgabe monatlich.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**Aufgabe \_ \_Monthlydow**</dt> <dt>5</dt> -Ereignis </dl>                                  | Startet die Aufgabe monatlich an einem bestimmten Tag der Woche.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**Aufgabe \_ Auslöse \_ Leerlauf**</dt> <dt>6</dt> </dl>                                                    | Startet den Task, wenn der Computer in den Leerlauf wechselt.<br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**Aufgabe \_ \_Registrierungs Registrierungs**</dt> <dt>7</dt> </dl>                            | Startet die Aufgabe, wenn die Aufgabe registriert wird.<br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**Aufgabe \_ \_Starten von Start**</dt> <dt>8</dt> </dl>                                                    | Startet die Aufgabe, wenn der Computer startet.<br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**Aufgabe \_ \_Logon-Anmeldung**</dt> <dt>9</dt> </dl>                                                 | Startet die Aufgabe, wenn sich ein bestimmter Benutzer anmeldet.<br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**Aufgabe \_ \_Änderung der Sitzungs \_ Status \_ Änderung**</dt> <dt>11</dt> </dl> | Löst die Aufgabe aus, wenn sich ein bestimmter Sitzungszustand ändert.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> <dt>

[**Task \_ - \_ Typ2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





