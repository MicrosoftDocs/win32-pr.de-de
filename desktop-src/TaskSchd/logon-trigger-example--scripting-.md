---
title: Beispiel für LOGON-Auslösung (Skripterstellung)
description: In diesem Skript Beispiel wird gezeigt, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad geplant ist, wenn sich ein Benutzer anmeldet.
ms.assetid: f25e105f-9439-4646-bdfd-609ee99a5d55
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72a8c4b5d0d67b59160eb3ed0b13885ee7e0eb51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206535"
---
# <a name="logon-trigger-example-scripting"></a>Beispiel für LOGON-Auslösung (Skripterstellung)

In diesem Skript Beispiel wird gezeigt, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad geplant ist, wenn sich ein Benutzer anmeldet. Der Task enthält einen Logon-Auslösers, der eine Start Grenze für die zu startende Aufgabe und eine Benutzer-ID angibt, die den Benutzer angibt. Der Task wird mithilfe der Gruppe "Administratoren" als Sicherheitskontext zum Ausführen der Aufgabe registriert.

Im folgenden Verfahren wird beschrieben, wie eine ausführbare Datei (z. b. Editor) gestartet wird, wenn ein bestimmter Benutzer sich anmeldet.

**So planen Sie den Start von Notepad, wenn sich ein Benutzer anmeldet**

1.  Erstellen Sie ein [**TaskService**](taskservice.md) -Objekt. Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.
2.  Rufen Sie einen Aufgaben Ordner ab, und erstellen Sie eine Aufgabe. Verwenden Sie die [**TaskService. GetFolder**](taskservice-getfolder.md) -Methode, um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService. newtask**](taskservice-newtask.md) -Methode zum Erstellen des [**Task Definition**](taskdefinition.md) -Objekts, das die Aufgabe darstellt.
3.  Definieren von Informationen über den Task mithilfe des [**Taskdefinition**](taskdefinition.md) -Objekts. Verwenden Sie die [**Task Definition. Settings**](taskdefinition-settings.md) -Eigenschaft, um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner Dienst den Task ausführt, und die [**Taskdefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) -Eigenschaft, um die Informationen zu definieren, die die Aufgabe beschreiben.
4.  Erstellen Sie einen Logon-Trigger mithilfe der [**Taskdefinition.**](taskdefinition-triggers.md) Triggers-Eigenschaft. Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection**](triggercollection.md) -Objekt. Verwenden Sie die [**TriggerCollection. Create**](triggercollection-create.md) -Methode (die den Typ des zu erstellenden Auslösers angibt), um einen Logon-Trigger zu erstellen. Beim Erstellen des Auslösers legen Sie die Start-und die Endgrenze des Auslösers zum Aktivieren und Deaktivieren des-Auslösers fest. Sie müssen die [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) -Eigenschaft für den-Befehl so festlegen, dass die Aktionen der Aufgabe für die Ausführung geplant werden, wenn sich der angegebene Benutzer nach der Start Grenze anmeldet.
5.  Erstellen Sie eine Aktion für die Ausführung der Aufgabe, indem Sie die [**Task Definition. Actions**](taskdefinition-actions.md) -Eigenschaft verwenden. Diese Eigenschaft ermöglicht den Zugriff auf das Objekt " [**Aktions Sammlung**](actioncollection.md) ". Verwenden Sie die [**Action Collection. Create**](actioncollection-create.md) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten. In diesem Beispiel wird ein [**execaction**](execaction.md) -Objekt verwendet, das eine Aktion darstellt, die eine ausführbare Datei startet.
6.  Registrieren Sie die Aufgabe mit der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode. In diesem Beispiel wird die Aufgabe so registriert, dass Sie die Gruppe "Administratoren" als Sicherheitskontext zum Ausführen der Aufgabe verwendet.

Im folgenden VBScript-Beispiel wird veranschaulicht, wie eine Aufgabe für die Ausführung von Notepad geplant wird, wenn sich ein Benutzer anmeldet.


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when a user logs on.
'---------------------------------------------------------

' A constant that specifies a logon trigger.
const TriggerTypeLogon = 9
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
regInfo.Description = "Task will execute Notepad when a " & _
    "specified user logs on."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a logon trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeLogon)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "LogonTriggerId"
trigger.UserId = "DOMAIN\UserName"   ' Must be a valid user account   

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
    "Test Logon Trigger", taskDefinition, createOrUpdateTask, _
    "Builtin\Administrators", , 4)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




