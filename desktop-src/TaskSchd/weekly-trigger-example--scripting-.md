---
title: Beispiel für wöchentlichen Trigger (Skripterstellung)
description: Dieses Skriptbeispiel zeigt, wie Sie eine Aufgabe erstellen, die Editor montags jeder Woche um 8:00 Uhr ausgeführt wird.
ms.assetid: 68ef73b0-3780-480e-90fe-940b6e8a5340
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6500dae3c0444bc41b982acc06b0e331e63aa4fb821385b416dd0d3e079671d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001768"
---
# <a name="weekly-trigger-example-scripting"></a>Beispiel für wöchentlichen Trigger (Skripterstellung)

Dieses Skriptbeispiel zeigt, wie Sie eine Aufgabe erstellen, die Editor montags jeder Woche um 8:00 Uhr ausgeführt wird. Die Aufgabe enthält einen täglichen Trigger, der angibt, wann der Task ausgeführt wird, und eine ausführbare Aktion, die Editor.

Im folgenden Verfahren wird beschrieben, wie Sie einen Task so planen, dass eine ausführbare Datei am Montag jeder Woche um 8:00 Uhr gestartet wird.

**So planen Editor, dass der Start am Montag jeder Woche um 8:00 Uhr beginnt**

1.  Erstellen Sie ein [**TaskService-Objekt.**](taskservice.md) Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.
2.  Erstellen Sie einen Taskordner, und erstellen Sie einen Task. Verwenden Sie [**die TaskService.GetFolder-Methode,**](taskservice-getfolder.md) um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService.NewTask-Methode,**](taskservice-newtask.md) um das [**TaskDefinition-Objekt**](taskdefinition.md) zu erstellen, das die Aufgabe darstellt.
3.  Definieren Sie Informationen zum Task mithilfe des [**TaskDefinition-Objekts.**](taskdefinition.md) Verwenden Sie [**die TaskDefinition.Einstellungen-Eigenschaft,**](taskdefinition-settings.md) um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner-Dienst die Aufgabe ausführt, und die [**TaskDefinition.RegistrationInfo-Eigenschaft,**](taskdefinition-registrationinfo.md) um die Informationen zu definieren, die den Task beschreiben.
4.  Erstellen Sie mithilfe der [**TaskDefinition.Triggers-Eigenschaft einen wöchentlichen**](taskdefinition-triggers.md) Trigger. Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection-Objekt,**](triggercollection.md) das zum Erstellen des Triggers verwendet wird.

    Verwenden Sie [**die TriggerCollection.Create-Methode**](triggercollection-create.md) (unter Angabe des Triggertyps, den Sie erstellen möchten), um einen wöchentlichen Trigger zu erstellen.

    Legen Sie [**die WeeklyTrigger.StartBoundary-Eigenschaft**](trigger-startboundary.md) fest, um anzugeben, wann der Trigger aktiviert wird und zu welchem Zeitpunkt der Task ausgeführt wird. In diesem Beispiel wird der Trigger am 1. Januar 2005 aktiviert, und die Aufgabe wird um 8:00 Uhr ausgeführt.

    Legen Sie [**die WeeklyTrigger.EndBoundary-Eigenschaft fest,**](trigger-endboundary.md)um anzugeben, wann der Trigger deaktiviert wird. In diesem Beispiel wird der Trigger am 1. Januar 2015 deaktiviert.

    Legen Sie [**die WeeklyTrigger.DaysOfWeek-Eigenschaft fest,**](weeklytrigger-daysofweek.md) um die Wochentage anzugeben, an denen der Task ausgeführt wird. In diesem Beispiel wird die Aufgabe am Montag ausgeführt.

    Legen Sie die [**WeeklyTrigger.WeeksInterval-Eigenschaft**](weeklytrigger-weeksinterval.md)fest, um das Intervall zwischen den Wochen im Zeitplan anzugeben. In diesem Beispiel wird die Aufgabe jede Woche ausgeführt.

5.  Erstellen Sie mithilfe der [**TaskDefinition.Actions-Eigenschaft**](taskdefinition-actions.md) eine Aktion für die Auszuführende Aufgabe. Diese Eigenschaft ermöglicht den Zugriff auf das [**ActionCollection-Objekt,**](actioncollection.md) das zum Erstellen der Aktion verwendet wird. Verwenden Sie die [**ActionCollection.Create-Methode,**](actioncollection-create.md) um den Typ der Aktion anzugeben, die Sie erstellen möchten. In diesem Beispiel wird ein [**ExecAction-Objekt**](execaction.md) verwendet, das eine Aktion darstellt, die einen Befehlszeilenvorgang ausgeführt.
6.  Registrieren Sie die Aufgabe mithilfe der [**TaskFolder.RegisterTaskDefinition-Methode.**](taskfolder-registertaskdefinition.md) In diesem Beispiel wird die Aufgabe Editor montags jeder Woche um 8:00 Uhr gestartet.

Im folgenden VBScript-Beispiel wird veranschaulicht, wie sie eine Aufgabe so planen, dass Editor täglich um 8:00 Uhr ausgeführt wird.


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a weekly basis.
'------------------------------------------------------------------

' A constant that specifies a weekly trigger.
const TriggerTypeWeekly = 3
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
regInfo.Description = "Start Notepad weekly."
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a weekly trigger. Note that the start boundary 
' specifies the time of day that the task starts, the 
' day-of-week specfies on what day of the week the task 
' runs, and the interval specifies what weeks the task runs.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeWeekly)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this tims is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysOfWeek = 1
trigger.WeeksInterval = 1    'Task runs every week.
trigger.Id = "WeeklyTriggerId"
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
    "Test Weekly Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




