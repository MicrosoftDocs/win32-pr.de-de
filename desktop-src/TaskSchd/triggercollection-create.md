---
title: TriggerCollection.Create-Methode
description: Erstellt für die Skripterstellung einen neuen Trigger für den Task.
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- triggers Taskplaner , creating
- Erstellen einer Taskplaner
- Create method Taskplaner , TriggerCollection object
- TriggerCollection-Objekt Taskplaner , Create-Methode
topic_type:
- apiref
api_name:
- TriggerCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7cfc32ebff941af374d2c4bb64db8ffe064961c13840e50244f416bad477a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001968"
---
# <a name="triggercollectioncreate-method"></a>TriggerCollection.Create-Methode

Erstellt für die Skripterstellung einen neuen Trigger für den Task.

## <a name="syntax"></a>Syntax


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*type* \[ In\]
</dt> <dd>

Dieser Parameter wird auf eine der folgenden [**TASK \_ TRIGGER \_ TYPE2-Enumerationskonst**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) constants festgelegt.



| Wert                                                                                                                                                                                                                                                                                | Bedeutung                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**AUFGABE \_ \_TRIGGEREREIGNIS**</dt> <dt>0</dt> </dl>                                                 | Löst die Aufgabe aus, wenn ein bestimmtes Ereignis auftritt.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**AUFGABE \_ \_TRIGGERZEIT**</dt> <dt>1</dt> </dl>                                                    | Löst die Aufgabe zu einer bestimmten Tageszeit aus.<br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ DAILY**</dt> <dt>2</dt> </dl>                                                 | Löst die Aufgabe nach einem täglichen Zeitplan aus. Die Aufgabe wird beispielsweise jeden Tag, jeden anderen Tag, jeden dritten Tag und so weiter zu einem bestimmten Zeitpunkt gestartet.<br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ WEEKLY**</dt> <dt>3</dt> </dl>                                              | Löst die Aufgabe nach einem wöchentlichen Zeitplan aus. Die Aufgabe beginnt beispielsweise jede Woche oder in einer anderen Woche um 8:00 Uhr an einem bestimmten Tag.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ MONTHLY**</dt> <dt>4</dt> </dl>                                           | Löst die Aufgabe nach einem monatlichen Zeitplan aus. Die Aufgabe wird z. B. an bestimmten Tagen bestimmter Monate gestartet.<br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Löst die Aufgabe nach einem monatlichen Wochentagszeitplan aus. Die Aufgabe beginnt beispielsweise an bestimmten Wochentagen, Wochen des Monats und Monaten des Jahres.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ IDLE**</dt> <dt>6</dt> </dl>                                                    | Löst den Task aus, wenn der Computer in den Leerlaufzustand übergeht.<br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**AUFGABE \_ \_TRIGGERREGISTRIERUNG**</dt> <dt>7</dt> </dl>                            | Löst die Aufgabe aus, wenn der Task registriert wird.<br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ BOOT**</dt> <dt>8</dt> </dl>                                                    | Löst die Aufgabe aus, wenn der Computer gestartet wird.<br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**AUFGABE \_ TRIGGER \_ LOGON**</dt> <dt>9</dt> </dl>                                                 | Löst die Aufgabe aus, wenn sich ein bestimmter Benutzer anmeldet.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**AUFGABE \_ AUSLÖSEN \_ DER \_ \_ SITZUNGSZUSTANDSÄNDERUNG**</dt> <dt>11</dt> </dl> | Löst die Aufgabe aus, wenn sich ein bestimmter Sitzungszustand ändert.<br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**Trigger-Objekt,**](trigger.md) das den neuen Trigger darstellt.

## <a name="remarks"></a>Hinweise

Informationen zu den einzelnen Triggertypen finden Sie unter [Triggertypen.](trigger-types.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**Trigger**](trigger.md)
</dt> </dl>

 

 





