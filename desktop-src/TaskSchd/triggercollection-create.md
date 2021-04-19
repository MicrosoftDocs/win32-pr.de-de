---
title: TriggerCollection. Create-Methode
description: Erstellt bei der Skripterstellung einen neuen---------
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- Trigger Taskplaner, erstellen
- Create-Methode Taskplaner
- Create Method-Taskplaner, TriggerCollection-Objekt
- TriggerCollection-Objekt Taskplaner, Create-Methode
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
ms.openlocfilehash: ad0f1c5dd8bef3d81a8e9b5859bc2bbd8c969bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339138"
---
# <a name="triggercollectioncreate-method"></a>TriggerCollection. Create-Methode

Erstellt bei der Skripterstellung einen neuen---------

## <a name="syntax"></a>Syntax


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* \[ in\]
</dt> <dd>

Dieser Parameter ist auf einen der folgenden [**Aufgaben \_ Auslösers \_**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) festgelegt Typ2 Enumerationskonstanten.



| Wert                                                                                                                                                                                                                                                                                | Bedeutung                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**Aufgabe \_ Auslöse \_ Ereignis**</dt> <dt>0</dt> </dl>                                                 | Löst die Aufgabe aus, wenn ein bestimmtes Ereignis auftritt.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**Aufgabe \_ Auslöse \_ Zeit**</dt> <dt>1</dt> </dl>                                                    | Löst den Task zu einem bestimmten Zeitpunkt aus.<br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**Aufgabe \_ Auslösung \_ täglich**</dt> <dt>2</dt> </dl>                                                 | Löst die Aufgabe nach einem täglichen Zeitplan aus. Der Task wird z. b. jeden Tag, jeden Tag, jeden dritten Tag und so weiter zu einem bestimmten Zeitpunkt gestartet.<br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**Aufgabe \_ Auslösung \_ wöchentlich**</dt> <dt>3</dt> </dl>                                              | Löst die Aufgabe nach einem wöchentlichen Zeitplan aus. Der Task wird z. b. wöchentlich um 8:00 Uhr an einem bestimmten Tag gestartet.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**Aufgabe \_ Auslösung \_ monatlich**</dt> <dt>4</dt> </dl>                                           | Löst die Aufgabe nach einem monatlichen Zeitplan aus. Beispielsweise wird die Aufgabe an bestimmten Tagen eines bestimmten Monats gestartet.<br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**Aufgabe \_ \_Monthlydow**</dt> <dt>5</dt> -Ereignis </dl>                                  | Löst die Aufgabe an einem monatlichen Wochentag aus. Beispielsweise wird die Aufgabe an einem bestimmten Tag der Woche, Wochen des Monats und Monaten des Jahres gestartet.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**Aufgabe \_ Auslöse \_ Leerlauf**</dt> <dt>6</dt> </dl>                                                    | Löst die Aufgabe aus, wenn der Computer in den Leerlauf wechselt.<br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**Aufgabe \_ \_Registrierungs Registrierungs**</dt> <dt>7</dt> </dl>                            | Löst die Aufgabe aus, wenn die Aufgabe registriert wird.<br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**Aufgabe \_ \_Starten von Start**</dt> <dt>8</dt> </dl>                                                    | Löst die Aufgabe aus, wenn der Computer gestartet wird.<br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**Aufgabe \_ \_Logon-Anmeldung**</dt> <dt>9</dt> </dl>                                                 | Löst die Aufgabe aus, wenn sich ein bestimmter Benutzer anmeldet.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**Aufgabe \_ \_Änderung der Sitzungs \_ Status \_ Änderung**</dt> <dt>11</dt> </dl> | Löst die Aufgabe aus, wenn sich ein bestimmter Sitzungszustand ändert.<br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein- [**Auslöserobjekt**](trigger.md) , das den neuen-Typ darstellt.

## <a name="remarks"></a>Bemerkungen

Informationen zu den einzelnen Auslösertypen finden Sie unter [Auslösertypen](trigger-types.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**Trigger**](trigger.md)
</dt> </dl>

 

 





