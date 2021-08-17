---
title: Beispiel für einen täglichen Trigger (Skripterstellung)
description: In diesem Skriptbeispiel wird veranschaulicht, wie Sie eine Aufgabe erstellen, Editor täglich um 8:00 Uhr ausgeführt wird.
ms.assetid: a13bd54d-b45a-46e5-8281-d080f50f6bef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 530d687264af9d2e7dbd4e9d05cf7dde39a449d3249c3576a35edc8a9e9f088d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139533"
---
# <a name="daily-trigger-example-scripting"></a>Beispiel für einen täglichen Trigger (Skripterstellung)

In diesem Skriptbeispiel wird veranschaulicht, wie Sie eine Aufgabe erstellen, Editor täglich um 8:00 Uhr ausgeführt wird. Die Aufgabe enthält einen täglichen Trigger, der eine Startgrenze angibt, um den Trigger zu aktivieren und die Tageszeit anzugeben, zu der der Task ausgeführt wird, ein Triggerintervall, um anzugeben, dass die Aufgabe täglich ausgeführt wird, und eine Endgrenze zum Deaktivieren des Triggers. Das Beispiel zeigt auch, wie ein Wiederholungsmuster für den Trigger festgelegt wird, um die Aufgabe zu wiederholen. Der Task enthält auch eine ausführbare Aktion, die Editor.

Im folgenden Verfahren wird beschrieben, wie Sie einen Task so planen, dass täglich um 8:00 Uhr eine ausführbare Datei gestartet wird. (Diese Schritte entsprechen den Codekommentaren, die im Beispielcode enthalten sind.)

**So planen Editor täglich um 8:00 Uhr**

1.  Erstellen Sie ein [**TaskService-Objekt.**](taskservice.md) Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.
2.  Erstellen Sie einen Taskordner, und erstellen Sie einen Task. Verwenden Sie [**die TaskService.GetFolder-Methode,**](taskservice-getfolder.md) um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService.NewTask-Methode,**](taskservice-newtask.md) um das [**TaskDefinition-Objekt**](taskdefinition.md) zu erstellen, das die Aufgabe darstellt.
3.  Definieren Sie Informationen zum Task mithilfe des [**TaskDefinition-Objekts.**](taskdefinition.md) Verwenden Sie [**die TaskDefinition.Einstellungen-Eigenschaft,**](taskdefinition-settings.md) um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner-Dienst die Aufgabe ausführt, und die [**TaskDefinition.RegistrationInfo-Eigenschaft,**](taskdefinition-registrationinfo.md) um die Informationen zu definieren, die den Task beschreiben.
4.  Erstellen Sie mithilfe der [**TaskDefinition.Triggers-Eigenschaft einen täglichen**](taskdefinition-triggers.md) Trigger. Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection-Objekt,**](triggercollection.md) das zum Erstellen des Triggers verwendet wird. Verwenden Sie [**die TriggerCollection.Create-Methode**](triggercollection-create.md) (unter Angabe des Triggertyps, den Sie erstellen möchten), um einen täglichen Trigger zu erstellen. Legen Sie beim Erstellen des Triggers die Startgrenze fest, um den Trigger zu aktivieren, und geben Sie die Tageszeit, die die Aufgabe ausgeführt wird, das Intervall zwischen den Tagen und die Endgrenze zum Deaktivieren des Triggers an. Das folgende Beispiel zeigt, wie sie ein Wiederholungsmuster für den Trigger festlegen, um die Aufgabe zu wiederholen.
5.  Erstellen Sie mithilfe der [**TaskDefinition.Actions-Eigenschaft**](taskdefinition-actions.md) eine Aktion für die Auszuführende Aufgabe. Diese Eigenschaft ermöglicht den Zugriff auf das [**ActionCollection-Objekt,**](actioncollection.md) das zum Erstellen der Aktion verwendet wird. Verwenden Sie die [**ActionCollection.Create-Methode,**](actioncollection-create.md) um den Typ der Aktion anzugeben, die Sie erstellen möchten. In diesem Beispiel wird ein [**ExecAction-Objekt**](execaction.md) verwendet, das eine Aktion darstellt, die einen Befehlszeilenvorgang ausgeführt.
6.  Registrieren Sie die Aufgabe mithilfe der [**TaskFolder.RegisterTaskDefinition-Methode.**](taskfolder-registertaskdefinition.md) In diesem Beispiel wird die Aufgabe täglich Editor 8:00 Uhr gestartet.

Im folgenden VBScript-Beispiel wird veranschaulicht, wie sie eine Aufgabe so planen, dass Editor täglich um 8:00 Uhr ausgeführt wird.


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a daily basis.
'------------------------------------------------------------------

' A constant that specifies a daily trigger.
const TriggerTypeDaily = 2
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
regInfo.Description = "Start notepad at 8:00AM daily"
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a daily trigger. Note that the start boundary 
' specifies the time of day that the task starts and the 
' interval specifies what days the task is run.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeDaily)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this time is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysInterval = 1    'Task runs every day.
trigger.Id = "DailyTriggerId"
trigger.Enabled = True

' Set the task repetition pattern for the task.
' This will repeat the task 5 times.
Dim repetitionPattern
Set repetitionPattern = trigger.Repetition
repetitionPattern.Duration = "PT4M"
repetitionPattern.Interval = "PT1M"

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
    "Test Daily Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




