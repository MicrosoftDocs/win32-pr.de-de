---
title: Beispiel für einen Start-Beispiel (Skripterstellung)
description: In diesem Skript Beispiel wird veranschaulicht, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad geplant ist, wenn das System gestartet wird.
ms.assetid: 73ae9cc4-ef89-4390-ac05-8a773f45fa46
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72b7735c607dfc39b848532a70e4d24b1a14d346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036975"
---
# <a name="boot-trigger-example-scripting"></a>Beispiel für einen Start-Beispiel (Skripterstellung)

In diesem Skript Beispiel wird veranschaulicht, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad geplant ist, wenn das System gestartet wird. Der Task enthält einen Start--Fehler, der eine Start Grenze und eine Verzögerungszeit angibt, nach der der Task gestartet wird, nachdem das System gestartet wurde. Der Task enthält auch eine Aktion, die den Task zum Ausführen von Notepad angibt. Der Task wird mit dem lokalen Dienst Konto als Sicherheitskontext registriert, um den Task auszuführen.

Im folgenden Verfahren wird beschrieben, wie eine ausführbare Datei, z. b. Notepad, beim Starten des Systems gestartet wird.

**So planen Sie den Start von Notepad, wenn das System gestartet wird**

1.  Erstellen Sie ein [**TaskService**](taskservice.md) -Objekt. Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.
2.  Rufen Sie einen Aufgaben Ordner ab, und erstellen Sie eine Aufgabe. Verwenden Sie die [**TaskService. GetFolder**](taskservice-getfolder.md) -Methode, um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService. newtask**](taskservice-newtask.md) -Methode zum Erstellen des [**Task Definition**](taskdefinition.md) -Objekts, das die Aufgabe darstellt.
3.  Definieren von Informationen über den Task mithilfe des [**Taskdefinition**](taskdefinition.md) -Objekts. Verwenden Sie die [**Task Definition. Settings**](taskdefinition-settings.md) -Eigenschaft, um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner Dienst den Task ausführt, und die [**Taskdefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) -Eigenschaft, um die Informationen zu definieren, die die Aufgabe beschreiben.
4.  Erstellen Sie einen Logon-Trigger mithilfe der [**Taskdefinition.**](taskdefinition-triggers.md) Triggers-Eigenschaft. Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection**](triggercollection.md) -Objekt. Verwenden Sie die [**TriggerCollection. Create**](triggercollection-create.md) -Methode (die den Typ des zu erstellenden Auslösers angibt), um einen Start Trigger zu erstellen. Legen Sie beim Erstellen des Auslösers die Eigenschaften [**StartBoundary**](trigger-startboundary.md) und [**endboundary**](trigger-endboundary.md) des Auslösers auf Aktivieren und Deaktivieren des Auslösers fest. Sie können auch einen Wert für die [**Delay**](boottrigger-delay.md) -Eigenschaft des Start-Auslösers angeben.
5.  Erstellen Sie eine Aktion für die Ausführung der Aufgabe, indem Sie die [**Task Definition. Actions**](taskdefinition-actions.md) -Eigenschaft verwenden. Diese Eigenschaft ermöglicht den Zugriff auf das Objekt " [**Aktions Sammlung**](actioncollection.md) ". Verwenden Sie die [**Action Collection. Create**](actioncollection-create.md) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten. In diesem Beispiel wird ein [**execaction**](execaction.md) -Objekt verwendet, das eine Aktion darstellt, die eine ausführbare Datei startet.
6.  Registrieren Sie die Aufgabe mit der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode. Der Task wird mit dem lokalen Dienst Konto als Sicherheitskontext registriert, um den Task auszuführen.

Im folgenden VBScript-Beispiel wird veranschaulicht, wie Sie einen Task zum Ausführen von Notepad 30 Sekunden nach dem Starten des Systems planen.


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

 

 




