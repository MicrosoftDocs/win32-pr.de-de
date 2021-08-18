---
title: RegisteredTask.State-Eigenschaft
description: Ruft für die Skripterstellung den Betriebszustand der registrierten Aufgabe ab.
ms.assetid: 1acd4946-322f-4f24-b317-92be80e19de5
keywords:
- Zustandseigenschaft Taskplaner
- State-Eigenschaft Taskplaner , RegisteredTask-Objekt
- RegisteredTask-Objekt Taskplaner , State-Eigenschaft
topic_type:
- apiref
api_name:
- RegisteredTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6099c47590397556937b8b1cceb59bc231117aa16c92012d59964afec4f6bcf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759601"
---
# <a name="registeredtaskstate-property"></a>RegisteredTask.State-Eigenschaft

Ruft für die Skripterstellung den Betriebszustand der registrierten Aufgabe ab.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.State As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Eine [**TASK \_ STATE-Konstante,**](/windows/desktop/api/taskschd/ne-taskschd-task_state) die den Betriebszustand der Aufgabe definiert.



| Wert                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <dt>**TASK \_ STATE \_ UNKNOWN**</dt> <dt>0</dt> </dl>    | Der Status des Tasks ist unbekannt.<br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <dt>**TASK \_ ZUSTAND \_ DEAKTIVIERT**</dt> <dt>1</dt> </dl> | Der Task ist registriert, ist jedoch deaktiviert, und es werden keine Instanzen des Tasks in die Warteschlange eingereiht oder ausgeführt. Der Task kann erst ausgeführt werden, wenn er aktiviert ist.<br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <dt>**TASK \_ STATE \_ QUEUED**</dt> <dt>2</dt> </dl>       | Instanzen des Tasks werden in die Warteschlange eingereiht.<br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <dt>**TASK \_ \_ZUSTANDSBEREIT**</dt> <dt>3</dt> </dl>          | Die Aufgabe kann ausgeführt werden, aber es werden keine Instanzen in die Warteschlange eingereiht oder ausgeführt.<br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <dt>**TASK \_ STATUS \_ WIRD AUSGEFÜHRT**</dt> <dt>4</dt> </dl>    | Mindestens eine Instanz des Tasks wird ausgeführt.<br/>                                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





