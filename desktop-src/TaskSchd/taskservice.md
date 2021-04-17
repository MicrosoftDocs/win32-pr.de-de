---
title: Task Service-Objekt
description: Bietet für die Skripterstellung Zugriff auf den Taskplaner-Dienst zum Verwalten registrierter Tasks.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- Task Service-Objekt Taskplaner
- Task Service-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TaskService
- HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762cd2445c3c6b720bba0f01ae48b787abc1fb38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478372"
---
# <a name="taskservice-object"></a>Task Service-Objekt

Bietet für die Skripterstellung Zugriff auf den Taskplaner-Dienst zum Verwalten registrierter Tasks.

Die [**TaskService. Connect**](taskservice-connect.md) -Methode sollte aufgerufen werden, bevor eine der anderen **Task Service** -Methoden aufgerufen wird.

## <a name="members"></a>Member

Das **TaskService** -Objekt verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Task Service** -Objekt verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verbinden**](taskservice-connect.md)                 | Stellt eine Verbindung mit einem Remote Computer her und ordnet alle nachfolgenden Aufrufe für diese Schnittstelle einer Remote Sitzung zu.<br/>                                                                                                 |
| [**GetFolder**](taskservice-getfolder.md)             | Ruft den Pfad zu einem Ordner registrierter Tasks ab.<br/>                                                                                                                                                            |
| [**Getrunningtasks**](taskservice-getrunningtasks.md) | Ruft eine Auflistung von Tasks ab, die ausgeführt werden.<br/>                                                                                                                                                                       |
| [**NewTask**](taskservice-newtask.md)                 | Gibt ein leeres Aufgaben Definitions Objekt zurück, das mit Einstellungen und Eigenschaften ausgefüllt und dann mithilfe der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode registriert werden soll.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **Task Service** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                          | BESCHREIBUNG                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Verbunden**](taskservice-connected.md)<br/>             | Ruft einen booleschen Wert ab, der angibt, ob eine Verbindung mit dem Taskplaner-Dienst besteht.<br/>                          |
| [**Connecteddomain**](taskservice-connecteddomain.md)<br/> | Ruft den Namen der Domäne ab, mit der der [**TargetServer**](taskservice-targetserver.md) -Computer verbunden ist.<br/> |
| [**ConnectedUser**](taskservice-connecteduser.md)<br/>     | Ruft den Namen des Benutzers ab, der mit dem Taskplaner-Dienst verbunden ist.<br/>                                       |
| Highestversion<br/>                                         | Ruft die höchste Version von Taskplaner ab, die von einem Computer unterstützt wird.<br/>                                             |
| [**TargetServer**](taskservice-targetserver.md)<br/>       | Ruft den Namen des Computers ab, auf dem der Taskplaner-Dienst ausgeführt wird, mit dem der Benutzer verbunden ist.<br/>          |



 

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

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





