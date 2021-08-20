---
title: Beispiel für Zeittrigger (Skripterstellung)
description: In diesem Skriptbeispiel wird gezeigt, wie Sie eine Aufgabe erstellen, Editor zu einem bestimmten Zeitpunkt ausgeführt wird.
ms.assetid: 8511ffcd-166f-4c63-9cd2-ead53dde9ed8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b448bf0aaa2c5670fb79ca10755a68bda77fd8d5b6e1c33d3fa292122bd5dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117942592"
---
# <a name="time-trigger-example-scripting"></a>Beispiel für Zeittrigger (Skripterstellung)

In diesem Skriptbeispiel wird gezeigt, wie Sie eine Aufgabe erstellen, Editor zu einem bestimmten Zeitpunkt ausgeführt wird. Die Aufgabe enthält einen zeitbasierten Trigger, der eine Startgrenze zum Aktivieren der Aufgabe, eine ausführbare Aktion, die Editor ausgeführt wird, und eine Endgrenze angibt, die die Aufgabe deaktiviert.

Im folgenden Verfahren wird beschrieben, wie Sie einen Task so planen, dass eine ausführbare Datei zu einem bestimmten Zeitpunkt gestartet wird.

**So planen Editor, dass der Start zu einem bestimmten Zeitpunkt beginnt**

1.  Erstellen Sie ein [**TaskService-Objekt.**](taskservice.md) Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.
2.  Erstellen Sie einen Taskordner, und erstellen Sie einen Task. Verwenden Sie [**die TaskService.GetFolder-Methode,**](taskservice-getfolder.md) um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService.NewTask-Methode,**](taskservice-newtask.md) um das [**TaskDefinition-Objekt**](taskdefinition.md) zu erstellen, das die Aufgabe darstellt.
3.  Definieren Sie Informationen zum Task mithilfe des [**TaskDefinition-Objekts.**](taskdefinition.md) Verwenden Sie [**die TaskDefinition.Einstellungen-Eigenschaft,**](taskdefinition-settings.md) um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner-Dienst die Aufgabe ausführt, und die [**TaskDefinition.RegistrationInfo-Eigenschaft,**](taskdefinition-registrationinfo.md) um die Informationen zu definieren, die den Task beschreiben.
4.  Erstellen Sie mithilfe der [**TaskDefinition.Triggers-Eigenschaft einen zeitbasierten**](taskdefinition-triggers.md) Trigger. Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection-Objekt.**](triggercollection.md) Verwenden Sie [**die TriggerCollection.Create-Methode**](triggercollection-create.md) (unter Angabe des Triggertyps, den Sie erstellen möchten), um einen zeitbasierten Trigger zu erstellen. Legen Sie beim Erstellen des Triggers die Start- und Endgrenze des Triggers fest, um den Trigger zu aktivieren und zu deaktivieren. Die Startgrenze gibt an, wann die Aktion des Task ausgeführt wird.
5.  Erstellen Sie mithilfe der [**TaskDefinition.Actions-Eigenschaft**](taskdefinition-actions.md) eine Aktion für die Auszuführende Aufgabe. Diese Eigenschaft ermöglicht den Zugriff auf das [**ActionCollection-Objekt.**](actioncollection.md) Verwenden Sie die [**ActionCollection.Create-Methode,**](actioncollection-create.md) um den Typ der Aktion anzugeben, die Sie erstellen möchten. In diesem Beispiel wird ein [**ExecAction-Objekt**](execaction.md) verwendet, das eine Aktion darstellt, die einen Befehlszeilenvorgang ausgeführt.
6.  Registrieren Sie die Aufgabe mithilfe der [**TaskFolder.RegisterTaskDefinition-Methode.**](taskfolder-registertaskdefinition.md) In diesem Beispiel wird der Task Editor der aktuellen Zeit plus 30 Sekunden gestartet.

Das folgende VBScript-Beispiel zeigt, wie sie eine Aufgabe 30 Sekunden Editor, nachdem der Task registriert wurde, ausgeführt wird.


```VB
'------------------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds
' from the time the task is registered.
'------------------------------------------------------------------

' A constant that specifies a time-based trigger.
const TriggerTypeTime = 1
' A constant that specifies an executable action.
const ActionTypeExec = 0   


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
regInfo.Description = "Start notepad at a certain time"
regInfo.Author = "Author Name"

'********************************************************
' Set the principal for the task
Dim principal
Set principal = taskDefinition.Principal

' Set the logon type to interactive logon
principal.LogonType = 3


' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a time-based trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeTime)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime

Dim time
time = DateAdd("s", 30, Now)  'start time = 30 seconds from now
startTime = XmlTime(time)

time = DateAdd("n", 5, Now) 'end time = 5 minutes from now
endTime = XmlTime(time)

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "TimeTriggerId"
trigger.Enabled = True

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task to run notepad.exe.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExec )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test TimeTrigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."



'------------------------------------------------------------------
' Used to get the time for the trigger 
' startBoundary and endBoundary.
' Return the time in the correct format: 
' YYYY-MM-DDTHH:MM:SS. 
'------------------------------------------------------------------
Function XmlTime(t)
    Dim cSecond, cMinute, CHour, cDay, cMonth, cYear
    Dim tTime, tDate

    cSecond = "0" & Second(t)
    cMinute = "0" & Minute(t)
    cHour = "0" & Hour(t)
    cDay = "0" & Day(t)
    cMonth = "0" & Month(t)
    cYear = Year(t)

    tTime = Right(cHour, 2) & ":" & Right(cMinute, 2) & _
        ":" & Right(cSecond, 2)
    tDate = cYear & "-" & Right(cMonth, 2) & "-" & Right(cDay, 2)
    XmlTime = tDate & "T" & tTime 
End Function

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




