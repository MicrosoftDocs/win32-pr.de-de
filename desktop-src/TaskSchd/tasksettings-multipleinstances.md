---
title: TaskSettings.MultipleInstances-Eigenschaft
description: Ruft für die Skripterstellung die Richtlinie ab, die definiert, wie die Taskplaner mit mehreren Instanzen der Aufgabe umgeht, oder legt sie fest.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- MultipleInstances-Eigenschaft Taskplaner
- MultipleInstances-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Objekt Taskplaner , MultipleInstances-Eigenschaft
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
ms.openlocfilehash: 2ff0091b9051840fea4c37869b51902f0c5f4c7cfed43a47c4f3924b398fe3e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059688"
---
# <a name="tasksettingsmultipleinstances-property"></a>TaskSettings.MultipleInstances-Eigenschaft

Ruft für die Skripterstellung die Richtlinie ab, die definiert, wie die Taskplaner mit mehreren Instanzen der Aufgabe umgeht, oder legt sie fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a>Eigenschaftswert

[**TASK \_ INSTANCES \_ POLICY-Konstanten.**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)



| Wert                                                                                                                                                                                                                                                               | Bedeutung                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <dt>**TASK \_ INSTANCES \_ PARALLEL**</dt> <dt>0</dt> </dl>                 | Startet eine neue -Instanz, während eine vorhandene Instanz des Tasks ausgeführt wird.<br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <dt>**TASK \_ INSTANCES \_ QUEUE**</dt> <dt>1</dt> </dl>                          | Startet eine neue Instanz des Tasks, nachdem alle anderen Instanzen des Tasks abgeschlossen sind.<br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <dt>**TASK \_ INSTANZEN \_ IGNORIEREN \_ NEUE**</dt> <dt>2</dt> </dl>          | Startet keine neue Instanz, wenn eine vorhandene Instanz des Tasks ausgeführt wird.<br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <dt>**TASK \_ INSTANZEN \_ BEENDEN \_ VORHANDENE**</dt> <dt>3</dt> </dl> | Beendet eine vorhandene Instanz des Tasks, bevor die neue Instanz gestartet wird.<br/>                 |



 

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**MultipleInstancesPolicy-Element**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_TASKINSTANZRICHTLINIE \_**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





