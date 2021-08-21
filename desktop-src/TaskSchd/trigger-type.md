---
title: Trigger.Type-Eigenschaft
description: Ruft für die Skripterstellung den Typ des Triggers ab.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Typeigenschafts-Taskplaner
- Type-Eigenschaft Taskplaner , Triggerobjekt
- Triggerobjekt Taskplaner , Type-Eigenschaft
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
ms.openlocfilehash: bcc44e385324d161ca051b4270096e674adbba878448667ef176a9c1c63bb24b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002038"
---
# <a name="triggertype-property"></a>Trigger.Type-Eigenschaft

Ruft für die Skripterstellung den Typ des Triggers ab. Der Triggertyp wird beim Erstellen des Triggers definiert und kann später nicht mehr geändert werden. Informationen zum Erstellen eines Triggers finden Sie unter [**TriggerCollection.Create**](triggercollection-create.md).

## <a name="syntax"></a>Syntax


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a>Eigenschaftswert

Einer der folgenden [**TASK \_ TRIGGER \_ TYPE2-Enumerationswerte.**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)



| Wert                                                                                                                                                                                                                                                                                | Bedeutung                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**AUFGABE \_ \_TRIGGEREREIGNIS**</dt> <dt>0</dt> </dl>                                                 | Startet die Aufgabe, wenn ein bestimmtes Ereignis auftritt.<br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**AUFGABE \_ \_TRIGGERZEIT**</dt> <dt>1</dt> </dl>                                                    | Startet die Aufgabe zu einer bestimmten Tageszeit.<br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ DAILY**</dt> <dt>2</dt> </dl>                                                 | Startet die Aufgabe täglich.<br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ WEEKLY**</dt> <dt>3</dt> </dl>                                              | Startet die Aufgabe wöchentlich.<br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ MONTHLY**</dt> <dt>4</dt> </dl>                                           | Startet die Aufgabe monatlich.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Startet die Aufgabe jeden Monat an einem bestimmten Wochentag.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ IDLE**</dt> <dt>6</dt> </dl>                                                    | Startet den Task, wenn der Computer in den Leerlaufzustand übergeht.<br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**AUFGABE \_ \_TRIGGERREGISTRIERUNG**</dt> <dt>7</dt> </dl>                            | Startet die Aufgabe, wenn die Aufgabe registriert ist.<br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ BOOT**</dt> <dt>8</dt> </dl>                                                    | Startet die Aufgabe, wenn der Computer gestartet wird.<br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ LOGON**</dt> <dt>9</dt> </dl>                                                 | Startet die Aufgabe, wenn sich ein bestimmter Benutzer anmeldet.<br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**AUFGABE \_ AUSLÖSEN \_ DER \_ \_ SITZUNGSZUSTANDSÄNDERUNG**</dt> <dt>11</dt> </dl> | Löst die Aufgabe aus, wenn sich ein bestimmter Sitzungszustand ändert.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> <dt>

[**\_ \_ TASKTRIGGERTYP2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





