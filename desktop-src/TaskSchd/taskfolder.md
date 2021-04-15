---
title: Taskfolder-Objekt
description: Skript Objekt, das die Methoden bereitstellt, die verwendet werden, um Aufgaben im Ordner zu registrieren (zu erstellen), Tasks aus dem Ordner zu entfernen und Unterordner aus dem Ordner zu erstellen oder zu entfernen.
ms.assetid: f6fd09ec-2777-4903-83b5-e3ac1aa472a0
keywords:
- Task Folder-Objekt Taskplaner
- Task Folder-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TaskFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ccad9331cf3df12ea5752fdd7e5ac94bfbeba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518599"
---
# <a name="taskfolder-object"></a>Taskfolder-Objekt

Skript Objekt, das die Methoden bereitstellt, die verwendet werden, um Aufgaben im Ordner zu registrieren (zu erstellen), Tasks aus dem Ordner zu entfernen und Unterordner aus dem Ordner zu erstellen oder zu entfernen.

## <a name="members"></a>Member

Das **taskfolder** -Objekt verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **taskfolder** -Objekt verfügt über diese Methoden.



| Methode                                                              | BESCHREIBUNG                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFolder**](taskfolder-createfolder.md)                     | Erstellt einen Ordner für Verwandte Aufgaben.<br/>                                                                                                 |
| [**DeleteFolder**](taskfolder-deletefolder.md)                     | Löscht einen Unterordner aus dem übergeordneten Ordner.<br/>                                                                                         |
| [**DeleteTask**](taskfolder-deletetask.md)                         | Löscht eine Aufgabe aus dem Ordner.<br/>                                                                                                     |
| [**GetFolder**](taskfolder-getfolder.md)                           | Ruft einen Ordner ab, der Tasks an einem angegebenen Speicherort enthält.<br/>                                                                          |
| [**GetFolders**](taskfolder-getfolders.md)                         | Ruft alle Unterordner im Ordner ab.<br/>                                                                                              |
| [**GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)   | Ruft die Sicherheits Beschreibung für den Ordner ab.<br/>                                                                                        |
| [**GetTask**](taskfolder-gettask.md)                               | Ruft eine Aufgabe an einem angegebenen Speicherort in einem Ordner ab.<br/>                                                                                    |
| [**GetTasks**](taskfolder-gettasks.md)                             | Ruft alle Tasks im Ordner ab.<br/>                                                                                                   |
| [**Register Task**](taskfolder-registertask.md)                     | Registriert (erstellt) eine neue Aufgabe im Ordner mithilfe von XML, um den Task zu definieren.<br/>                                                          |
| [**Methode**](taskfolder-registertaskdefinition.md) | Registriert (erstellt) einen Task an einem angegebenen Speicherort mithilfe der [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Schnittstelle zum Definieren einer Aufgabe.<br/> |
| [**SETSECURITYDESCRIPTOR**](taskfolder-setsecuritydescriptor.md)   | Legt die Sicherheits Beschreibung für den Ordner fest.<br/>                                                                                        |



 

### <a name="properties"></a>Eigenschaften

Das **taskfolder** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                   | Zugriffstyp          | BESCHREIBUNG                                                                        |
|:-------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [**Name**](taskfolder-name.md)<br/> | Schreibgeschützt<br/> | Ruft den Namen ab, der verwendet wird, um den Ordner zu identifizieren, der einen Task enthält.<br/> |
| [**ADS**](taskfolder-path.md)<br/> | Schreibgeschützt<br/> | Ruft den Pfad zum Speicherort des Ordners ab.<br/>                            |



 

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md), [Ereignis auslöserbeispiel (Skripterstellung)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), Beispiel für den [täglichen Aufruf (Skripterstellung)](daily-trigger-example--scripting-.md), Registrierungs- [auslöserbeispiel (Skripterstellung)](registration-trigger-example--scripting-.md), Beispiel für einen [wöchentlichen](weekly-trigger-example--scripting-.md)Vorgang (Skripterstellung), Beispiel für den Logon-Vorgang [(Skripterstellung)](logon-trigger-example--scripting-.md), Beispiel für den [Start](boot-trigger-example--scripting-.md) [-](displaying-task-names-and-state--scripting-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Objekte](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





