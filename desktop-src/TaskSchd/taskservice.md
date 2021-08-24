---
title: TaskService-Objekt
description: Für die Skripterstellung bietet Zugriff auf den Taskplaner zum Verwalten registrierter Aufgaben.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- TaskService-Taskplaner
- TaskService-Objekt Taskplaner , beschrieben
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
ms.openlocfilehash: 74f20840a5580d0188354ca6b65ab3ce5b7402d57ea7346462d2f990ecfe34cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658650"
---
# <a name="taskservice-object"></a>TaskService-Objekt

Für die Skripterstellung bietet Zugriff auf den Taskplaner zum Verwalten registrierter Aufgaben.

Die [**TaskService.Verbinden-Methode**](taskservice-connect.md) sollte aufgerufen werden, bevor eine der anderen **TaskService-Methoden aufgerufen** wird.

## <a name="members"></a>Member

Das **TaskService-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **TaskService-Objekt** verfügt über diese Methoden.



| Methode                                                 | Beschreibung                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verbinden**](taskservice-connect.md)                 | Stellt eine Verbindung mit einem Remotecomputer und ordnet alle nachfolgenden Aufrufe dieser Schnittstelle einer Remotesitzung zu.<br/>                                                                                                 |
| [**GetFolder**](taskservice-getfolder.md)             | Ruft den Pfad zu einem Ordner registrierter Aufgaben ab.<br/>                                                                                                                                                            |
| [**GetRunningTasks**](taskservice-getrunningtasks.md) | Ruft eine Auflistung ausgeführter Aufgaben ab.<br/>                                                                                                                                                                       |
| [**NewTask**](taskservice-newtask.md)                 | Gibt ein leeres Aufgabendefinitionsobjekt zurück, das mit Einstellungen und Eigenschaften ausgefüllt und dann mithilfe der [**TaskFolder.RegisterTaskDefinition-Methode registriert werden**](taskfolder-registertaskdefinition.md) soll.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **TaskService-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                          | Beschreibung                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Verbunden**](taskservice-connected.md)<br/>             | Ruft einen booleschen Wert ab, der angibt, ob Sie mit dem Taskplaner sind.<br/>                          |
| [**ConnectedDomain**](taskservice-connecteddomain.md)<br/> | Ruft den Namen der Domäne ab, mit der der [**TargetServer-Computer**](taskservice-targetserver.md) verbunden ist.<br/> |
| [**ConnectedUser**](taskservice-connecteduser.md)<br/>     | Ruft den Namen des Benutzers ab, der mit dem Taskplaner verbunden ist.<br/>                                       |
| HighestVersion<br/>                                         | Ruft die höchste Version der Taskplaner, die ein Computer unterstützt.<br/>                                             |
| [**TargetServer**](taskservice-targetserver.md)<br/>       | Ruft den Namen des Computers ab, auf dem der Taskplaner ausgeführt wird, mit dem der Benutzer verbunden ist.<br/>          |



 

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skriptobjekt finden Sie unter Time [Trigger Example (Scripting)](time-trigger-example--scripting-.md), Event [Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), Registration Trigger [Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md)oder [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).

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
</dt> </dl>

 

 





