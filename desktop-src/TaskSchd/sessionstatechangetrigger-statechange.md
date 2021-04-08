---
title: Sessionstatechangeauslöst. StateChange (Eigenschaft)
description: Ruft bei der Skripterstellung die Art der Sitzungs Änderung für Terminal Server ab, die einen Task Start auslöst, oder legt diese fest.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- StateChange-Eigenschaft Taskplaner
- StateChange-Eigenschaft Taskplaner, sessionstatechange-Objekt
- Sessionstatechange-Objekt Taskplaner, StateChange-Eigenschaft
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.StateChange
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4be561482917788f6afb9b8eb7394cdcce7985
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740616"
---
# <a name="sessionstatechangetriggerstatechange-property"></a>Sessionstatechangeauslöst. StateChange (Eigenschaft)

Ruft bei der Skripterstellung die Art der Sitzungs Änderung für Terminal Server ab, die einen Task Start auslöst, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Die Art der Sitzungs Änderung für Terminal Server, die das Starten einer Aufgabe auslöst.

Die möglichen Werte stammen aus der Enumeration der [**\_ \_ \_ \_ statusänderungsart des Aufgaben Sitzungs Zustands**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) .



| Wert                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <dt>**Aufgabe \_ Konsolen \_ Verbindung**</dt> <dt>1</dt> </dl>          | Statusänderung der Terminal Server-Konsolen Verbindung. Wenn Sie z. b. eine Verbindung mit einer Benutzersitzung auf dem lokalen Computer herstellen, indem Sie die Benutzer auf dem Computer wechseln. <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <dt>**Aufgabe \_ Konsolen \_ Trennung**</dt> <dt>2</dt> </dl> | Statusänderung der Terminal Server Konsole wird getrennt. Wenn Sie z. b. eine Verbindung mit einer Benutzersitzung auf dem lokalen Computer trennen, indem Sie die Benutzer auf dem Computer wechseln.<br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <dt>**Aufgabe \_ Remote \_ Verbindung**</dt> <dt>3</dt> </dl>             | Statusänderung für Terminal Server-Remote Verbindung. Dies ist beispielsweise der Fall, wenn ein Benutzer mithilfe des Remotedesktopverbindung Programms von einem Remote Computer aus eine Verbindung mit einer Benutzersitzung herstellt.<br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <dt>**Aufgabe \_ Remote \_**</dt> Verbindung <dt>4</dt> </dl>    | Statusänderung des Terminal Server-Remote Verbindungs Wechsels. Dies ist beispielsweise der Fall, wenn ein Benutzer die Verbindung mit einer Benutzersitzung trennt, während das Remotedesktopverbindung Programm von einem Remote Computer aus verwendet wird.<br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <dt>**Aufgabe \_ Sitzungs \_ Sperre**</dt> <dt>7</dt> </dl>                   | Statusänderung für Terminal Server Sitzung gesperrt. Diese Statusänderung bewirkt beispielsweise, dass die Aufgabe ausgeführt wird, wenn der Computer gesperrt wird. <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <dt>**Aufgabe \_ Aufheben \_ der Sitzung**</dt> <dt>8</dt> </dl>             | Die Statusänderung der Terminal Server Sitzung wurde aufgehoben. Diese Statusänderung bewirkt beispielsweise, dass die Aufgabe ausgeführt wird, wenn der Computer entsperrt wird.<br/>                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





