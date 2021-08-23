---
title: Principal.LogonType-Eigenschaft
description: Für die Skripterstellung ruft die Sicherheitsanmeldungsmethode ab, die zum Ausführen der aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt diese fest.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- LogonType-Taskplaner
- LogonType-Eigenschaft Taskplaner , Principal-Objekt
- Prinzipalobjekt Taskplaner , LogonType-Eigenschaft
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
ms.openlocfilehash: e7db85573072c54a613009c3afec4873a38db4ff7336e487553437967b4c6e1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060078"
---
# <a name="principallogontype-property"></a>Principal.LogonType-Eigenschaft

Für die Skripterstellung ruft die Sicherheitsanmeldungsmethode ab, die zum Ausführen der aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Legen Sie auf eine der folgenden [**TASK \_ LOGON TYPE-Enumerationskonst**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) constants fest.



| Wert                                                                                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**AUFGABE \_ LOGON \_ NONE**</dt> <dt>0</dt> </dl>                                                                               | Die Anmeldemethode ist nicht angegeben. Wird für Nicht-NT-Anmeldeinformationen verwendet. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**AUFGABE \_ \_ANMELDEKENNWORT**</dt> <dt>1</dt> </dl>                                                                   | Verwenden Sie ein Kennwort für die Benutzerprotokollierung. Das Kennwort muss zum Zeitpunkt der Registrierung angegeben werden.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**AUFGABE \_ LOGON \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Verwenden Sie ein vorhandenes interaktives Token, um eine Aufgabe auszuführen. Der Benutzer muss sich mit einem Dienst für die Benutzeranmeldung (S4U) anmelden. Wenn eine S4U-Anmeldung verwendet wird, wird kein Kennwort vom System gespeichert, und es besteht kein Zugriff auf das Netzwerk oder auf verschlüsselte Dateien.<br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**AUFGABE \_ INTERAKTIVES \_ TOKEN FÜR DIE \_ ANMELDUNG**</dt> <dt>3</dt> </dl>                                       | Der Benutzer muss bereits angemeldet sein. Die Aufgabe wird nur in einer vorhandenen interaktiven Sitzung ausgeführt.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**AUFGABE \_ LOGON \_ GROUP**</dt> <dt>4</dt> </dl>                                                                            | Gruppenaktivierung. Das Feld userId gibt die Gruppe an.<br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**AUFGABE \_ \_ \_ ANMELDEDIENSTKONTO**</dt> <dt>5</dt> </dl>                                             | Gibt an, dass ein lokales Systemkonto, ein lokaler Dienst oder ein Netzwerkdienstkonto als Sicherheitskontext zum Ausführen der Aufgabe verwendet wird.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**AUFGABE \_ INTERAKTIVES \_ TOKEN ODER KENNWORT FÜR DIE \_ \_ \_ ANMELDUNG**</dt> <dt>6</dt> </dl> | Verwenden Sie zunächst das interaktive Token. Wenn der Benutzer nicht angemeldet ist (kein interaktives Token verfügbar), wird das Kennwort verwendet. Das Kennwort muss angegeben werden, wenn eine Aufgabe registriert wird. Dieses Flag wird für neue Aufgaben nicht empfohlen, da es weniger zuverlässig als TASK \_ LOGON \_ PASSWORD ist.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nur gültig, wenn ein Benutzerbezeichner von der [**UserId-Eigenschaft angegeben**](principal-userid.md) wird.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Anmeldetyp im -Element des Taskplaner [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) angegeben.

Für eine Aufgabe, die eine Meldungsfeldaktion enthält, wird das Meldungsfeld angezeigt, wenn der Task aktiviert ist und der Task über einen interaktiven Anmeldetyp verfügt. Um den Taskanmeldungstyp auf interaktiv festzulegen, geben Sie 3 (**TASK \_ LOGON \_ INTERACTIVE \_ TOKEN**) oder 4 (**TASK \_ LOGON \_ GROUP**) in der **LogonType-Eigenschaft** des Aufgabenprinzipals oder im *logonType-Parameter* von [**TaskFolder.RegisterTask**](taskfolder-registertask.md) oder [**TaskFolder.RegisterTaskDefinition an.**](taskfolder-registertaskdefinition.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**Prinzipal**](principal.md)
</dt> </dl>

 

 





