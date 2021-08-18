---
title: Beispiel für Starttrigger (Skripterstellung)
description: In diesem Skriptbeispiel wird veranschaulicht, wie sie eine Aufgabe erstellen, die für die Ausführung Editor Systemstarts geplant ist.
ms.assetid: 73ae9cc4-ef89-4390-ac05-8a773f45fa46
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ff02bef70b4003c4e7b6e9aff03e2d615f24d7e15707cddcae3a4637ff2b11f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002518"
---
# <a name="boot-trigger-example-scripting"></a>Beispiel für Starttrigger (Skripterstellung)

In diesem Skriptbeispiel wird veranschaulicht, wie sie eine Aufgabe erstellen, die für die Ausführung Editor Systemstarts geplant ist. Die Aufgabe enthält einen Starttrigger, der eine Startgrenze und eine Verzögerungszeit für den Start des Task nach dem Systemstart angibt. Der Task enthält auch eine Aktion, die den Task angibt, der Editor. Die Aufgabe wird mithilfe des lokalen Dienstkontos als Sicherheitskontext registriert, um die Aufgabe auszuführen.

Im folgenden Verfahren wird beschrieben, wie Sie eine ausführbare Datei wie Editor starten, wenn das System gestartet wird.

**So planen Sie Editor starten, wenn das System gestartet wird**

1.  Erstellen Sie ein [**TaskService-Objekt.**](taskservice.md) Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.
2.  Erstellen Sie einen Taskordner, und erstellen Sie einen Task. Verwenden Sie [**die TaskService.GetFolder-Methode,**](taskservice-getfolder.md) um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService.NewTask-Methode,**](taskservice-newtask.md) um das [**TaskDefinition-Objekt**](taskdefinition.md) zu erstellen, das die Aufgabe darstellt.
3.  Definieren Sie Informationen zum Task mithilfe des [**TaskDefinition-Objekts.**](taskdefinition.md) Verwenden Sie [**die TaskDefinition.Einstellungen-Eigenschaft,**](taskdefinition-settings.md) um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner-Dienst die Aufgabe ausführt, und die [**TaskDefinition.RegistrationInfo-Eigenschaft,**](taskdefinition-registrationinfo.md) um die Informationen zu definieren, die den Task beschreiben.
4.  Erstellen Sie mithilfe der [**TaskDefinition.Triggers-Eigenschaft einen Logon-Trigger.**](taskdefinition-triggers.md) Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection-Objekt.**](triggercollection.md) Verwenden Sie [**die TriggerCollection.Create-Methode**](triggercollection-create.md) (unter Angabe des Triggertyps, den Sie erstellen möchten), um einen Starttrigger zu erstellen. Legen Sie beim Erstellen des Triggers die [**Eigenschaften StartBoundary**](trigger-startboundary.md) und [**EndBoundary**](trigger-endboundary.md) des Triggers fest, um den Trigger zu aktivieren und zu deaktivieren. Sie können auch einen Wert für die [**Delay-Eigenschaft**](boottrigger-delay.md) des Starttriggers angeben.
5.  Erstellen Sie mithilfe der [**TaskDefinition.Actions-Eigenschaft**](taskdefinition-actions.md) eine Aktion für die Auszuführende Aufgabe. Diese Eigenschaft ermöglicht den Zugriff auf das [**ActionCollection-Objekt.**](actioncollection.md) Verwenden Sie [**die ActionCollection.Create-Methode,**](actioncollection-create.md) um den Typ der Aktion anzugeben, die Sie erstellen möchten. In diesem Beispiel wird ein [**ExecAction-Objekt**](execaction.md) verwendet, das eine Aktion darstellt, die eine ausführbare Datei startet.
6.  Registrieren Sie die Aufgabe mithilfe der [**TaskFolder.RegisterTaskDefinition-Methode.**](taskfolder-registertaskdefinition.md) Die Aufgabe wird mithilfe des lokalen Dienstkontos als Sicherheitskontext registriert, um die Aufgabe auszuführen.

Das folgende VBScript-Beispiel zeigt, wie sie eine Aufgabe 30 Sekunden Editor, nachdem das System gestartet wurde, ausgeführt wird.


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds after
' the system is booted.
'---------------------------------------------------------

' A constant that specifies a boot trigger.
const TriggerTypeBoot = 8
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
regInfo.Description = "Task will execute Notepad when " & _
    "the computer is booted."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a boot trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeBoot)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "BootTriggerId"
trigger.Delay = "PT30S"                ' 30 Seconds   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.
const createOrUpdateTask = 6
call rootFolder.RegisterTaskDefinition( _
    "Test Boot Trigger", taskDefinition, createOrUpdateTask, _
    "Local Service", , 5)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




