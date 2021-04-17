---
title: Principal. logontype (Eigenschaft)
description: Dient zum Abrufen oder Festlegen der Sicherheits Anmelde Methode, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- Logontype-Eigenschaft Taskplaner
- Logontype-Eigenschaft Taskplaner, Prinzipal Objekt
- Principal-Objekt Taskplaner, logontype-Eigenschaft
topic_type:
- apiref
api_name:
- Principal.LogonType
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4455fd273144b2d6abd81c78be31a1b037cd889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477199"
---
# <a name="principallogontype-property"></a>Principal. logontype (Eigenschaft)

Dient zum Abrufen oder Festlegen der Sicherheits Anmelde Methode, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.

## <a name="syntax"></a>Syntax


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Legen Sie auf eine der folgenden Enumerationskonstanten für den [**\_ Anmeldetyp der Aufgabe**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) fest.



| Wert                                                                                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**Aufgabe \_ Login \_ None**</dt> <dt>0</dt> </dl>                                                                               | Die Anmelde Methode ist nicht angegeben. Wird für nicht-NT-Anmelde Informationen verwendet. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**Aufgabe \_ Anmelde \_ Kennwort**</dt> <dt>1</dt> </dl>                                                                   | Verwenden Sie ein Kennwort für die Anmeldung für den Benutzer. Das Kennwort muss beim Registrierungs Zeitpunkt angegeben werden.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**Aufgabe \_ Anmeldung \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Verwenden Sie ein vorhandenes interaktives Token, um eine Aufgabe auszuführen. Der Benutzer muss sich mithilfe eines Diensts für die Benutzeranmeldung (S4U) anmelden. Wenn eine S4U-Anmeldung verwendet wird, wird kein Kennwort vom System gespeichert, und es gibt keinen Zugriff auf das Netzwerk oder verschlüsselte Dateien.<br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**Aufgabe \_ \_Interaktives Anmelde \_ Token**</dt> <dt>3</dt> </dl>                                       | Der Benutzer muss bereits angemeldet sein. Der Task wird nur in einer vorhandenen interaktiven Sitzung ausgeführt.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**Aufgabe \_ Anmelde \_ Gruppe**</dt> <dt>4</dt> </dl>                                                                            | Gruppen Aktivierung. Das Feld "UserID" gibt die Gruppe an.<br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**Aufgabe \_ Anmelde \_ Dienst \_ Konto**</dt> <dt>5</dt> </dl>                                             | Gibt an, dass ein lokales System, ein lokaler Dienst oder ein Netzwerkdienst Konto als Sicherheitskontext zum Ausführen des Tasks verwendet wird.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**Aufgabe \_ \_Interaktives \_ Token \_ oder \_ Kennwort**</dt> für die Anmeldung <dt>6</dt> </dl> | Verwenden Sie zuerst das interaktive Token. Wenn der Benutzer nicht angemeldet ist (kein interaktives Token verfügbar), wird das Kennwort verwendet. Das Kennwort muss angegeben werden, wenn ein Task registriert wird. Dieses Flag wird für neue Aufgaben nicht empfohlen, da es weniger zuverlässig ist als das Kennwort für die Task \_ Anmeldung \_ .<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist nur gültig, wenn eine Benutzer-ID von der [**UserID**](principal-userid.md) -Eigenschaft angegeben wird.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Anmeldetyp im- [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) Element des Taskplaner Schemas angegeben.

Für einen Task, der eine MessageBox-Aktion enthält, wird das Meldungs Feld angezeigt, wenn die Aufgabe aktiviert ist und der Task einen interaktiven Anmeldetyp aufweist. Wenn Sie den Anmeldetyp für die Aufgabe interaktiv festlegen möchten, geben Sie in der **logontype** -Eigenschaft des Task Prinzipals oder im *logontype* -Parameter von [**taskfolder. RegisterTask**](taskfolder-registertask.md) oder [**taskfolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)den Wert 3 an.**\_ \_ \_****\_ \_**

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

[**Prinzipal**](principal.md)
</dt> </dl>

 

 





