---
title: SessionStateChangeTrigger.StateChange-Eigenschaft
description: Für die Skripterstellung ruft die Art der Terminalserver-Sitzungsänderung ab, die einen Taskstart auslösen würde, oder legt diese fest.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- StateChange-Taskplaner
- StateChange-Eigenschaft Taskplaner , SessionStateChangeTrigger-Objekt
- SessionStateChangeTrigger-Objekt Taskplaner , StateChange-Eigenschaft
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
ms.openlocfilehash: cfbd2037f19ca2d9fe8ec5d0ba046e69894f431b81d623b61b9474515bcef3a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100160"
---
# <a name="sessionstatechangetriggerstatechange-property"></a>SessionStateChangeTrigger.StateChange-Eigenschaft

Für die Skripterstellung ruft die Art der Terminalserver-Sitzungsänderung ab, die einen Taskstart auslösen würde, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Die Art der Terminalserver-Sitzungsänderung, die das Starten einer Aufgabe auslöst.

Die möglichen Werte sind aus der [**TASK SESSION STATE CHANGE \_ \_ \_ \_ TYPE-Enumeration.**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type)



| Wert                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <dt>**AUFGABE \_ CONSOLE \_ CONNECT**</dt> <dt>1</dt> </dl>          | Änderung des Verbindungsstatus der Terminalserverkonsole. Beispielsweise, wenn Sie eine Verbindung mit einer Benutzersitzung auf dem lokalen Computer herstellen, indem Sie die Benutzer auf dem Computer wechseln. <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <dt>**AUFGABE \_ CONSOLE \_ DISCONNECT**</dt> <dt>2</dt> </dl> | Änderung des Verbindungsstatus der Terminalserverkonsole. Beispiel: Wenn Sie die Verbindung mit einer Benutzersitzung auf dem lokalen Computer trennen, indem Sie die Benutzer auf dem Computer wechseln.<br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <dt>**AUFGABE \_ REMOTE \_ CONNECT**</dt> <dt>3</dt> </dl>             | Änderung des Remoteverbindungsstatus des Terminalservers. Beispielsweise, wenn ein Benutzer mithilfe des Remotedesktopverbindung von einem Remotecomputer eine Verbindung mit einer Benutzersitzung herstellt.<br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <dt>**AUFGABE \_ REMOTE \_ DISCONNECT**</dt> <dt>4</dt> </dl>    | Änderung des Zustands der Remotetrennung des Terminalservers. Beispiel: Ein Benutzer trennt die Verbindung mit einer Benutzersitzung, während er das Remotedesktopverbindung einem Remotecomputer verwendet.<br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <dt>**AUFGABE \_ \_SITZUNGSSPERRE**</dt> <dt>7</dt> </dl>                   | Statusänderung für gesperrte Terminalserversitzung. Diese Zustandsänderung bewirkt beispielsweise, dass der Task ausgeführt wird, wenn der Computer gesperrt ist. <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <dt>**AUFGABE \_ SITZUNG \_ ENTSPERRUNG**</dt> <dt>8</dt> </dl>             | Statusänderung für entsperrte Terminalserversitzung. Diese Zustandsänderung bewirkt beispielsweise, dass der Task ausgeführt wird, wenn der Computer entsperrt wird.<br/>                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





