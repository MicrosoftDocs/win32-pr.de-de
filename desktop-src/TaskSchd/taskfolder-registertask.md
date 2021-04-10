---
title: Taskfolder. RegisterTask-Methode
description: Bei der Skripterstellung (erstellt) eine neue Aufgabe im Ordner mithilfe von XML zum Definieren der Aufgabe.
ms.assetid: 9bf5c59b-5aa1-42b3-a307-f583cdf59a39
keywords:
- RegisterTask-Methode Taskplaner
- RegisterTask-Methode Taskplaner, taskfolder-Objekt
- Task Folder-Objekt Taskplaner, RegisterTask-Methode
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc0ed00ec736a90f716d895199812899d972930
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956925"
---
# <a name="taskfolderregistertask-method"></a>Taskfolder. RegisterTask-Methode

Bei der Skripterstellung (erstellt) eine neue Aufgabe im Ordner mithilfe von XML zum Definieren der Aufgabe.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.RegisterTask( _
  ByVal path, _
  ByVal xmlText, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef pTask _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* \[ in\]
</dt> <dd>

Der Name der Aufgabe. Wenn dieser Wert auf " **Nothing**" festgelegt ist, wird die Aufgabe im Stamm Aufgaben Ordner registriert, und der TaskName ist ein GUID-Wert, der vom Taskplaner-Dienst erstellt wird.

Ein Taskname darf nicht mit einem Leerzeichen beginnen oder enden. Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben. Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.

</dd> <dt>

*XmlText* \[ in\]
</dt> <dd>

Eine XML-formatierte Beschreibung der Aufgabe.

Die folgenden Themen enthalten Aufgaben, die mithilfe von XML definiert wurden.

-   [Beispiel für Zeit Auslösung (XML)](time-trigger-example--xml-.md)
-   [Ereignis auslöserbeispiel (XML)](/previous-versions//aa446889(v=vs.85))
-   [Beispiel für das tägliche Beispiel (XML)](daily-trigger-example--xml-.md)
-   [Registrierungs auslöserbeispiel (XML)](registration-trigger-example--xml-.md)
-   [Beispiel für einen wöchentlichen Beispiel (XML)](weekly-trigger-example--xml-.md)
-   [Beispiel eines LOGON-Auslösers (XML)](logon-trigger-example--xml-.md)
-   [Beispiel für einen Start Auslösers (XML)](boot-trigger-example--xml-.md)

</dd> <dt>

*Flags* \[ in\]
</dt> <dd>

Eine [**Aufgaben \_ Erstellungs**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) Konstante.



| Wert                                                                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <dt>**Aufgabe \_ \_Nur**</dt> <dt>0x1</dt> validieren </dl>                                                | Der Taskplaner überprüft die Syntax des XML-Codes, der den Task beschreibt, registriert jedoch nicht den Task. Diese Konstante kann nicht **mit den Werten Create \_ ,** **Task \_ Update** oder **Task \_ Create \_ oder \_ Update** kombiniert werden.<br/>                                                                                                                  |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <dt>**Aufgabe \_**</dt> <dt>0x2</dt> erstellen </dl>                                                                      | Der Taskplaner die den Task als neue Aufgabe registriert.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <dt>**Aufgabe \_ Update**</dt> <dt>0x4</dt> </dl>                                                                      | Der Taskplaner registriert den Task als aktualisierte Version eines vorhandenen Tasks. Wenn eine Aufgabe mit einem Registrierungs-ausgelöst wird, wird die Aufgabe ausgeführt, nachdem das Update ausgeführt wurde.<br/>                                                                                                                                                            |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <dt>**Aufgabe \_ 0x6 erstellen \_ oder \_ Aktualisieren**</dt> <dt></dt> </dl>                                      | Der Taskplaner registriert den Task entweder als neue Aufgabe oder als aktualisierte Version, wenn der Task bereits vorhanden ist. Entspricht der Aufgabe zum \_ Erstellen von \| Aufgaben \_ Aktualisierungen.<br/>                                                                                                                                                                                    |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <dt>**Aufgabe \_**</dt> <dt>0x8</dt> deaktivieren </dl>                                                                   | Mit dem Taskplaner wird die vorhandene Aufgabe deaktiviert.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <dt>**Aufgabe \_ \_ \_ Prinzipal- \_ ACE**</dt> <dt>0x10</dt> nicht hinzufügen </dl>                  | Der Taskplaner wird verhindert, dass der ACE (Access Control Entry, ACE) für den Kontext Prinzipal hinzugefügt wird. Wenn die **taskfolder. RegisterTask** -Funktion mit diesem Flag aufgerufen wird, um eine Aufgabe zu aktualisieren, fügt der Taskplaner-Dienst nicht den ACE für den neuen Kontext Prinzipal hinzu und entfernt den ACE nicht aus dem alten Kontext Prinzipal.<br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <dt>**Aufgabe \_ \_Registrierungs \_ Trigger ignorieren**</dt> <dt>0x20</dt> </dl> | Der Taskplaner erstellt die Aufgabe, ignoriert jedoch die Registrierungs Trigger in der Aufgabe. Durch das Ignorieren der Registrierungs Trigger wird die Aufgabe nicht ausgeführt, wenn Sie registriert wird, es sei denn, ein zeitbasierter Trigger führt die Ausführung bei der Registrierung aus.<br/>                                                                                               |



 

</dd> <dt>

*Benutzer-ID* \[ in\]
</dt> <dd>

Die Benutzer Anmelde Informationen, die zum Registrieren der Aufgabe verwendet werden.

> [!Note]  
> Wenn der Task als Taskplaner 1,0-Aufgabe definiert ist, verwenden Sie in diesem UserID-Parameter keinen Gruppennamen (anstelle eines bestimmten Benutzernamens). Ein Task wird als Taskplaner 1,0-Aufgabe definiert, wenn das Versions Attribut des Task-Elements im XML-Code der Aufgabe auf 1,1 festgelegt ist.

 

</dd> <dt>

*Kennwort* \[ in\]
</dt> <dd>

Das Kennwort für die Benutzer-ID, die zum Registrieren der Aufgabe verwendet wird. Wenn der \_ \_ Anmeldetyp für das Anmeldedienst \_ Konto verwendet wird, muss das Kennwort ein leerer **Variant** -Wert wie z. b. **VT \_ null** oder **VT \_ empty** sein.

</dd> <dt>

*logontype* \[ in\]
</dt> <dd>

Definiert, welche Anmelde Methode verwendet wird, um die registrierte Aufgabe auszuführen.



| Wert                                                                                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**Aufgabe \_ Login \_ None**</dt> <dt>0</dt> </dl>                                                                               | Die Anmelde Methode ist nicht angegeben. Wird für nicht-NT-Anmelde Informationen verwendet. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**Aufgabe \_ Anmelde \_ Kennwort**</dt> <dt>1</dt> </dl>                                                                   | Verwenden Sie ein Kennwort für die Anmeldung für den Benutzer. Das Kennwort muss beim Registrierungs Zeitpunkt angegeben werden.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**Aufgabe \_ Anmeldung \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Verwenden Sie ein vorhandenes interaktives Token, um eine Aufgabe auszuführen. Der Benutzer muss sich mithilfe eines Diensts für die Benutzeranmeldung (S4U) anmelden. Wenn eine S4U-Anmeldung verwendet wird, wird kein Kennwort vom System gespeichert, und es gibt keinen Zugriff auf das Netzwerk oder verschlüsselte Dateien.<br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**Aufgabe \_ \_Interaktives Anmelde \_ Token**</dt> <dt>3</dt> </dl>                                       | Der Benutzer muss bereits angemeldet sein. Der Task wird nur in einer vorhandenen interaktiven Sitzung ausgeführt.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**Aufgabe \_ Anmelde \_ Gruppe**</dt> <dt>4</dt> </dl>                                                                            | Gruppen Aktivierung. Das Feld **GroupID** gibt die Gruppe an.<br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**Aufgabe \_ Anmelde \_ Dienst \_ Konto**</dt> <dt>5</dt> </dl>                                             | Gibt an, dass ein lokales System, ein lokaler Dienst oder ein Netzwerkdienst Konto als Sicherheitskontext zum Ausführen des Tasks verwendet wird.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**Aufgabe \_ \_Interaktives \_ Token \_ oder \_ Kennwort**</dt> für die Anmeldung <dt>6</dt> </dl> | Verwenden Sie zuerst das interaktive Token. Wenn der Benutzer nicht angemeldet ist (kein interaktives Token verfügbar), wird das Kennwort verwendet. Das Kennwort muss angegeben werden, wenn ein Task registriert wird. Dieses Flag wird für neue Aufgaben nicht empfohlen, da es weniger zuverlässig ist als das Kennwort für die Task \_ Anmeldung \_ .<br/> |



 

</dd> <dt>

*SDDL* \[ in, optional\]
</dt> <dd>

Die Sicherheits Beschreibung, die der registrierten Aufgabe zugeordnet ist. Sie können die Zugriffs Steuerungs Liste (ACL) in der Sicherheits Beschreibung für eine Aufgabe angeben, um bestimmten Benutzern und Gruppen den Zugriff auf eine Aufgabe zu gewähren oder zu verweigern.

> [!Note]  
> Wenn dem lokalen System Konto der Zugriff auf eine Aufgabe verweigert wird, kann der Taskplaner Dienst unerwartete Ergebnisse liefern.

 

</dd> <dt>

*pTask* \[ vorgenommen\]
</dt> <dd>

Ein [**registeredtask**](registeredtask.md) -Objekt, das die neue Aufgabe darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Für einen Task, der eine MessageBox-Aktion enthält, wird das Meldungs Feld angezeigt, wenn die Aufgabe aktiviert ist und der Task einen interaktiven Anmeldetyp aufweist. Wenn Sie den Anmeldetyp für die Aufgabe interaktiv festlegen möchten, geben Sie in der [**logontype**](principal-logontype.md) -Eigenschaft des Task Prinzipals oder im *logontype* -Parameter von **taskfolder. RegisterTask** oder [**taskfolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)den Wert 3 an.**\_ \_ \_****\_ \_**

Nur ein Mitglied der Gruppe "Administratoren" kann eine Aufgabe mit einem Start--Vorgang erstellen.

Sie können eine Aufgabe erfolgreich mit einer Gruppe registrieren, die im *UserID* -Parameter angegeben ist, und 3 (**\_ \_ interaktives Anmelde \_ Token** für die Aufgabe), das im *logontype* -Parameter von **Task Folder. RegisterTask** oder [**taskfolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)angegeben ist, die Aufgabe jedoch nicht ausgeführt wird.

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

[**Registeredtask**](registeredtask.md)
</dt> <dt>

[**Task Folder**](taskfolder.md)
</dt> </dl>

 

