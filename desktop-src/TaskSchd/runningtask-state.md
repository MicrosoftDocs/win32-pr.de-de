---
title: Runningtask. State (Eigenschaft)
description: Ruft für die Skripterstellung einen Bezeichner für den Zustand der aktuell laufenden Aufgabe ab.
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- State-Eigenschaft Taskplaner
- State-Eigenschaft Taskplaner, runningtask-Objekt
- Runningtask-Objekt Taskplaner, State-Eigenschaft
topic_type:
- apiref
api_name:
- RunningTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b962de116eef1301be209828181147dfe03273e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740856"
---
# <a name="runningtaskstate-property"></a>Runningtask. State (Eigenschaft)

Ruft für die Skripterstellung einen Bezeichner für den Zustand der aktuell laufenden Aufgabe ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
RunningTask.State As String
```



## <a name="property-value"></a>Eigenschaftswert

Ein Bezeichner für den Zustand der laufenden Aufgabe.



| Wert                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <dt>**Aufgabe \_ \_Unbekannter Status**</dt> <dt>0</dt> </dl>    | Der Task Status ist unbekannt.<br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <dt>**Aufgabe \_ Status \_ deaktiviert**</dt> <dt>1</dt> </dl> | Der Task ist registriert, aber deaktiviert, und es werden keine Instanzen der Aufgabe in die Warteschlange eingereiht oder ausgeführt. Der Task kann erst ausgeführt werden, wenn er aktiviert ist.<br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <dt>**Aufgabe \_ Status in \_ Warteschlange**</dt> <dt>2</dt> </dl>       | Instanzen der Aufgabe werden in die Warteschlange eingereiht.<br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <dt>**Aufgabe \_ Status \_ bereit**</dt> <dt>3</dt> </dl>          | Der Task ist für die Ausführung bereit, aber es werden keine Instanzen in die Warteschlange eingereiht oder ausgeführt.<br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <dt>**Aufgabe \_ Status \_**</dt> <dt>4</dt> </dl>    | Eine oder mehrere Instanzen der Aufgabe werden ausgeführt.<br/>                                                                                         |



 

## <a name="remarks"></a>Bemerkungen

Die [**runningtask. Refresh**](runningtask-refresh.md) -Methode wird aufgerufen, bevor der-Eigenschafts Wert zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





