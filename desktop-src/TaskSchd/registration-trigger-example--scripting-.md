---
title: Beispiel für Registrierungstrigger (Skripterstellung)
description: In diesem Skriptbeispiel wird gezeigt, wie Sie eine Aufgabe erstellen, die Editor ausgeführt werden soll, wenn ein Task registriert wird.
ms.assetid: 956b3a21-7d36-4d06-be84-690884ba653a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f036d4772c98392881f254e07e192c970a2cb407727294c7f196c9c15cb9e11f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011320"
---
# <a name="registration-trigger-example-scripting"></a>Beispiel für Registrierungstrigger (Skripterstellung)

In diesem Skriptbeispiel wird gezeigt, wie Sie eine Aufgabe erstellen, die Editor ausgeführt werden soll, wenn ein Task registriert wird. Die Aufgabe enthält einen Registrierungstrigger, der eine Startgrenze und eine Endgrenze für den Task angibt. Die Startgrenze gibt an, wann der Trigger aktiviert wird. Der Task enthält auch eine Aktion, die den Task angibt, der Editor ausgeführt werden soll.

> [!Note]  
> Wenn eine Aufgabe mit einem Registrierungstrigger aktualisiert wird, wird der Task nach dem Update ausgeführt.

 

Im folgenden Verfahren wird beschrieben, wie Sie eine ausführbare Datei wie Editor planen, die gestartet wird, wenn eine Aufgabe registriert wird.

**So planen Sie Editor, wenn eine Aufgabe registriert wird**

1.  Erstellen Sie ein [**TaskService-Objekt.**](taskservice.md) Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.
2.  Abrufen eines Aufgabenordners und Erstellen einer Aufgabe Verwenden Sie die [**TaskService.GetFolder-Methode,**](taskservice-getfolder.md) um den Ordner abzurufen, in dem der Task gespeichert ist, und die [**TaskService.NewTask-Methode,**](taskservice-newtask.md) um das [**TaskDefinition-Objekt**](taskdefinition.md) zu erstellen, das den Task darstellt.
3.  Definieren Sie Informationen zur Aufgabe mithilfe des [**TaskDefinition-Objekts.**](taskdefinition.md) Verwenden Sie die [**TaskDefinition.Einstellungen**](taskdefinition-settings.md) -Eigenschaft, um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner-Dienst die Aufgabe ausführt, und die [**TaskDefinition.RegistrationInfo-Eigenschaft,**](taskdefinition-registrationinfo.md) um die Informationen zu definieren, die die Aufgabe beschreiben.
4.  Erstellen Sie einen Registrierungstrigger mithilfe der [**TaskDefinition.Triggers-Eigenschaft.**](taskdefinition-triggers.md) Diese Eigenschaft bietet Zugriff auf das [**TriggerCollection-Objekt.**](triggercollection.md) Verwenden Sie die [**TriggerCollection.Create-Methode**](triggercollection-create.md) (die den Typ des Triggers angibt, den Sie erstellen möchten), um einen Registrierungstrigger zu erstellen.
5.  Erstellen Sie mithilfe der [**TaskDefinition.Actions-Eigenschaft**](taskdefinition-actions.md) eine Aktion für die auszuführende Aufgabe. Diese Eigenschaft bietet Zugriff auf das [**ActionCollection-Objekt.**](actioncollection.md) Verwenden Sie die [**ActionCollection.Create-Methode,**](actioncollection-create.md) um den Typ der Aktion anzugeben, die Sie erstellen möchten. In diesem Beispiel wird ein [**ExecAction-Objekt**](execaction.md) verwendet, das eine Aktion darstellt, die eine ausführbare Datei startet.
6.  Registrieren Sie die Aufgabe mithilfe der [**TaskFolder.RegisterTaskDefinition-Methode.**](taskfolder-registertaskdefinition.md)

Das folgende VBScript-Beispiel zeigt, wie Sie eine Aufgabe erstellen, die Editor für die Ausführung plant, wenn der Task registriert wird.


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when
' the task is registered.
'---------------------------------------------------------

' A constant that specifies a registration trigger.
const TriggerTypeRegistration = 7
' A constant that specifies an executable action.
const ActionTypeExecutable = 0   


'********************************************************
' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

'********************************************************
' Get a folder to create a task definition in. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")

' The taskDefinition variable is the TaskDefinition object.
Dim taskDefinition
' The flags parameter is 0 because it is not supported.
Set taskDefinition = service.NewTask(0) 

'********************************************************
' Define information about the task.

' Set the registration info for the task by 
' creating the RegistrationInfo object.
Dim regInfo
Set regInfo = taskDefinition.RegistrationInfo
regInfo.Description = "Start Notepad when the task is registered."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a registration trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeRegistration)

trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "RegistrationTriggerId"   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes Notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Registration Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




