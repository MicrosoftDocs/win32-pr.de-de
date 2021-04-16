---
title: Tasksettings. multipleinhaltungen (Eigenschaft)
description: Ruft bei der Skripterstellung die Richtlinie ab oder legt Sie fest, die definiert, wie die Taskplaner mehrere Instanzen der Aufgabe behandelt.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- Multipleinhaltungen-Eigenschaft Taskplaner
- Multipleinhaltungen-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, multipleinhaltungen (Eigenschaft)
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794ea07f1c01dabe957181bd327f8787f873917b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517468"
---
# <a name="tasksettingsmultipleinstances-property"></a>Tasksettings. multipleinhaltungen (Eigenschaft)

Ruft bei der Skripterstellung die Richtlinie ab oder legt Sie fest, die definiert, wie die Taskplaner mehrere Instanzen der Aufgabe behandelt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a>Eigenschaftswert

[**Aufgabe \_ Instanzen \_ Richtlinien**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) Konstanten.



| Wert                                                                                                                                                                                                                                                               | Bedeutung                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <dt>**Aufgabe \_ Instanzen \_ parallel**</dt> <dt>0</dt> </dl>                 | Startet eine neue-Instanz, während eine vorhandene Instanz der Aufgabe ausgeführt wird.<br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <dt>**Aufgabe \_ Instanzen \_ Warteschlange**</dt> <dt>1</dt> </dl>                          | Startet eine neue Instanz der Aufgabe, nachdem alle anderen Instanzen der Aufgabe vollständig sind.<br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <dt>**Aufgabe \_ Instanzen \_ ignorieren \_ neu**</dt> <dt>2</dt> </dl>          | Startet keine neue Instanz, wenn eine vorhandene Instanz der Aufgabe ausgeführt wird.<br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <dt>**Aufgabe \_ Instanzen, die \_ \_ vorhandene**</dt> <dt>3</dt> Abbrechen </dl> | Beendet eine vorhandene Instanz der Aufgabe vor dem Starten der neuen Instanz.<br/>                 |



 

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**multipleinstancespolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Task \_ Instanzen \_ Richtlinie**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





