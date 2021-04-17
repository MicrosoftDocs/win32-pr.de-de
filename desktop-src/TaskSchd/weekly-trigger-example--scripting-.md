---
title: Beispiel für einen wöchentlichen Auslösung (Skripterstellung)
description: In diesem Skript Beispiel wird gezeigt, wie Sie einen Task erstellen, der den Notepad um 8 00 Uhr am Montag jeder Woche ausführt.
ms.assetid: 68ef73b0-3780-480e-90fe-940b6e8a5340
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d9cf627591250c341008ba3a5129c4cc10cad6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388131"
---
# <a name="weekly-trigger-example-scripting"></a>Beispiel für einen wöchentlichen Auslösung (Skripterstellung)

In diesem Skript Beispiel wird gezeigt, wie Sie einen Task erstellen, der den Notepad um 8:00 Uhr am Montag jeder Woche ausführt. Der Task enthält einen täglichen-Triggerwert, der angibt, wann der Task ausgeführt wird, und eine ausführbare Aktion, die Editor ausführt.

Im folgenden Verfahren wird beschrieben, wie eine Aufgabe zum Starten einer ausführbaren Datei um 8:00 Uhr am Montag jeder Woche geplant wird.

**So planen Sie den Start von Notepad um 8:00 Uhr am Montag jeder Woche**

1.  Erstellen Sie ein [**TaskService**](taskservice.md) -Objekt. Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.
2.  Rufen Sie einen Aufgaben Ordner ab, und erstellen Sie eine Aufgabe. Verwenden Sie die [**TaskService. GetFolder**](taskservice-getfolder.md) -Methode, um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService. newtask**](taskservice-newtask.md) -Methode zum Erstellen des [**Task Definition**](taskdefinition.md) -Objekts, das die Aufgabe darstellt.
3.  Definieren von Informationen über den Task mithilfe des [**Taskdefinition**](taskdefinition.md) -Objekts. Verwenden Sie die [**Task Definition. Settings**](taskdefinition-settings.md) -Eigenschaft, um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner Dienst den Task ausführt, und die [**Taskdefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) -Eigenschaft, um die Informationen zu definieren, die die Aufgabe beschreiben.
4.  Erstellen Sie einen wöchentlichen Trigger mithilfe der [**Taskdefinition.**](taskdefinition-triggers.md) Triggers-Eigenschaft. Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection**](triggercollection.md) -Objekt, das verwendet wird, um den Trigger zu erstellen.

    Verwenden Sie die [**TriggerCollection. Create**](triggercollection-create.md) -Methode (gibt den Typ des zu erstellenden Auslösers an), um einen wöchentlichen Trigger zu erstellen.

    Legen Sie die Eigenschaft " [**weeklyauslöst. StartBoundary**](trigger-startboundary.md) " fest, um anzugeben, wann der ausgelöst wird, und die Uhrzeit, zu der die Aufgabe ausgeführt wird. In diesem Beispiel wird der-Triggern am 1. Januar 2005 aktiviert, und der Task wird um 8:00 Uhr ausgeführt.

    Legen Sie die Eigenschaft [**weeklyauslöst. endboundary**](trigger-endboundary.md)auf fest, wenn der-Fehler deaktiviert wird. In diesem Beispiel wird der-Wert am 1. Januar 2015 deaktiviert.

    Legen Sie die Eigenschaft [**weeklytrigger\daysofweek**](weeklytrigger-daysofweek.md) fest, um die Tage der Woche anzugeben, an denen der Task ausgeführt wird. In diesem Beispiel wird die Aufgabe am Montag ausgeführt.

    Legen Sie die Eigenschaft " [**weeklyauth. weeksinterval**](weeklytrigger-weeksinterval.md)" fest, um das Intervall zwischen den Wochen im Zeitplan anzugeben. In diesem Beispiel wird die Aufgabe wöchentlich ausgeführt.

5.  Erstellen Sie eine Aktion für die Ausführung der Aufgabe, indem Sie die [**Task Definition. Actions**](taskdefinition-actions.md) -Eigenschaft verwenden. Diese Eigenschaft ermöglicht den Zugriff auf das " [**Action Collection**](actioncollection.md) "-Objekt, das zum Erstellen der Aktion verwendet wird. Verwenden Sie die [**Action Collection. Create**](actioncollection-create.md) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten. In diesem Beispiel wird ein [**execaction**](execaction.md) -Objekt verwendet, das eine Aktion darstellt, die einen Befehlszeilen Vorgang ausführt.
6.  Registrieren Sie die Aufgabe mit der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode. In diesem Beispiel startet der Task Notepad um 8:00 Uhr am Montag jeder Woche.

Im folgenden VBScript-Beispiel wird gezeigt, wie ein Task zum Ausführen von Notepad jeden Tag um 8:00 Uhr geplant wird.


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

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




