---
title: RunningTask.State(Eigenschaft)
description: Ruft für die Skripterstellung einen Bezeichner für den Status des ausgeführten Task ab.
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- Zustandseigenschafts-Taskplaner
- State-Eigenschaft Taskplaner , RunningTask-Objekt
- RunningTask-Objekt Taskplaner , State-Eigenschaft
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
ms.openlocfilehash: 1e3c83b35c348e3ab86eb04c03ef4c5d25a76ef3fe5040603ce32da54ec4e217
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975040"
---
# <a name="runningtaskstate-property"></a>RunningTask.State(Eigenschaft)

Ruft für die Skripterstellung einen Bezeichner für den Status des ausgeführten Task ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
RunningTask.State As String
```



## <a name="property-value"></a>Eigenschaftswert

Ein Bezeichner für den Status der ausgeführten Aufgabe.



| Wert                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <dt>**AUFGABE \_ STATE \_ UNKNOWN**</dt> <dt>0</dt> </dl>    | Der Status der Aufgabe ist unbekannt.<br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <dt>**AUFGABE \_ STATUS \_ DEAKTIVIERT**</dt> <dt>1</dt> </dl> | Die Aufgabe ist registriert, aber deaktiviert, und es werden keine Instanzen der Aufgabe in die Warteschlange gestellt oder ausgeführt. Die Aufgabe kann erst ausgeführt werden, wenn sie aktiviert ist.<br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <dt>**AUFGABE \_ STATE \_ QUEUED**</dt> <dt>2</dt> </dl>       | Instanzen der Aufgabe werden in die Warteschlange gestellt.<br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <dt>**AUFGABE \_ STATUS \_ BEREIT**</dt> <dt>3</dt> </dl>          | Die Aufgabe kann ausgeführt werden, aber es werden keine Instanzen in die Warteschlange gestellt oder ausgeführt.<br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <dt>**AUFGABE \_ STATUS \_ WIRD AUSGEFÜHRT**</dt> <dt>4</dt> </dl>    | Eine oder mehrere Instanzen der Aufgabe werden ausgeführt.<br/>                                                                                         |



 

## <a name="remarks"></a>Hinweise

Die [**RunningTask.Refresh-Methode**](runningtask-refresh.md) wird aufgerufen, bevor der Eigenschaftswert zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





