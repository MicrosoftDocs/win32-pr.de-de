---
title: Beispiel für den täglichen Auslösung (Skripterstellung)
description: In diesem Skript Beispiel wird gezeigt, wie Sie einen Task erstellen, der den Notepad täglich um 8 00 Uhr ausgeführt wird.
ms.assetid: a13bd54d-b45a-46e5-8281-d080f50f6bef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3399934786e1cd0f95ca020c92027ccafafa5272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855963"
---
# <a name="daily-trigger-example-scripting"></a>Beispiel für den täglichen Auslösung (Skripterstellung)

In diesem Skript Beispiel wird gezeigt, wie Sie einen Task erstellen, der den Notepad täglich um 8:00 Uhr ausgeführt wird. Der Task enthält einen täglichen-Triggertyp, der eine Start Grenze zum Aktivieren des Auslösers angibt und die Uhrzeit angibt, zu der der Task ausgeführt wird, ein triggerintervall, das angibt, dass der Task jeden Tag ausgeführt wird, und eine Endgrenze, um den Triggervorgang zu deaktivieren. Das Beispiel zeigt auch, wie Sie ein Wiederholungsmuster für den-Vorgang festlegen, um die Aufgabe zu wiederholen. Der Task enthält auch eine ausführbare Aktion, die den Notepad ausführt.

Im folgenden Verfahren wird beschrieben, wie eine Aufgabe zum Starten einer ausführbaren Datei täglich um 8:00 Uhr geplant wird. (Diese Schritte entsprechen den Code Kommentaren, die im Beispielcode enthalten sind.)

**So planen Sie den Start von Notepad täglich um 8:00 Uhr**

1.  Erstellen Sie ein [**TaskService**](taskservice.md) -Objekt. Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.
2.  Rufen Sie einen Aufgaben Ordner ab, und erstellen Sie eine Aufgabe. Verwenden Sie die [**TaskService. GetFolder**](taskservice-getfolder.md) -Methode, um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService. newtask**](taskservice-newtask.md) -Methode zum Erstellen des [**Task Definition**](taskdefinition.md) -Objekts, das die Aufgabe darstellt.
3.  Definieren von Informationen über den Task mithilfe des [**Taskdefinition**](taskdefinition.md) -Objekts. Verwenden Sie die [**Task Definition. Settings**](taskdefinition-settings.md) -Eigenschaft, um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner Dienst den Task ausführt, und die [**Taskdefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) -Eigenschaft, um die Informationen zu definieren, die die Aufgabe beschreiben.
4.  Erstellen Sie einen täglichen Trigger mithilfe der [**Taskdefinition.**](taskdefinition-triggers.md) Triggers-Eigenschaft. Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection**](triggercollection.md) -Objekt, das verwendet wird, um den Trigger zu erstellen. Verwenden Sie die [**TriggerCollection. Create**](triggercollection-create.md) -Methode (gibt den Typ des zu erstellenden Auslösers an), um einen täglichen Trigger zu erstellen. Legen Sie beim Erstellen des Auslösers die Start Grenze fest, um den-Triggervorgang zu aktivieren, und geben Sie die Uhrzeit an, zu der der Task ausgeführt wird, das Intervall zwischen den Tagen und die Endgrenze, um den-Triggervorgang Im folgenden Beispiel wird gezeigt, wie Sie ein Wiederholungsmuster für den-Vorgang festlegen, um die Aufgabe zu wiederholen.
5.  Erstellen Sie eine Aktion für die Ausführung der Aufgabe, indem Sie die [**Task Definition. Actions**](taskdefinition-actions.md) -Eigenschaft verwenden. Diese Eigenschaft ermöglicht den Zugriff auf das " [**Action Collection**](actioncollection.md) "-Objekt, das zum Erstellen der Aktion verwendet wird. Verwenden Sie die [**Action Collection. Create**](actioncollection-create.md) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten. In diesem Beispiel wird ein [**execaction**](execaction.md) -Objekt verwendet, das eine Aktion darstellt, die einen Befehlszeilen Vorgang ausführt.
6.  Registrieren Sie die Aufgabe mit der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode. In diesem Beispiel startet der Task Notepad täglich um 8:00 Uhr.

Im folgenden VBScript-Beispiel wird gezeigt, wie ein Task zum Ausführen von Notepad jeden Tag um 8:00 Uhr geplant wird.


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

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




