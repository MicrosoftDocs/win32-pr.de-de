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
# <a name="logon-trigger-example-scripting"></a><span data-ttu-id="f3fa9-103">Beispiel für LOGON-Auslösung (Skripterstellung)</span><span class="sxs-lookup"><span data-stu-id="f3fa9-103">Logon Trigger Example (Scripting)</span></span>

<span data-ttu-id="f3fa9-104">In diesem Skript Beispiel wird gezeigt, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad geplant ist, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-104">This scripting example shows how to create a task that is scheduled to execute Notepad when a user logs on.</span></span> <span data-ttu-id="f3fa9-105">Der Task enthält einen Logon-Auslösers, der eine Start Grenze für die zu startende Aufgabe und eine Benutzer-ID angibt, die den Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-105">The task contains a logon trigger that specifies a start boundary for the task to start and a user identifier that specifies the user.</span></span> <span data-ttu-id="f3fa9-106">Der Task wird mithilfe der Gruppe "Administratoren" als Sicherheitskontext zum Ausführen der Aufgabe registriert.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-106">The task is registered using the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="f3fa9-107">Im folgenden Verfahren wird beschrieben, wie eine ausführbare Datei (z. b. Editor) gestartet wird, wenn ein bestimmter Benutzer sich anmeldet.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-107">The following procedure describes how to schedule an executable such as Notepad to start when a specified user logs on.</span></span>

<span data-ttu-id="f3fa9-108">**So planen Sie den Start von Notepad, wenn sich ein Benutzer anmeldet**</span><span class="sxs-lookup"><span data-stu-id="f3fa9-108">**To schedule Notepad to start when a user logs on**</span></span>

1.  <span data-ttu-id="f3fa9-109">Erstellen Sie ein [**TaskService**](taskservice.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-109">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="f3fa9-110">Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-110">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="f3fa9-111">Rufen Sie einen Aufgaben Ordner ab, und erstellen Sie eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-111">Get a task folder and create a task.</span></span> <span data-ttu-id="f3fa9-112">Verwenden Sie die [**TaskService. GetFolder**](taskservice-getfolder.md) -Methode, um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService. newtask**](taskservice-newtask.md) -Methode zum Erstellen des [**Task Definition**](taskdefinition.md) -Objekts, das die Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-112">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="f3fa9-113">Definieren von Informationen über den Task mithilfe des [**Taskdefinition**](taskdefinition.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-113">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="f3fa9-114">Verwenden Sie die [**Task Definition. Settings**](taskdefinition-settings.md) -Eigenschaft, um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner Dienst den Task ausführt, und die [**Taskdefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) -Eigenschaft, um die Informationen zu definieren, die die Aufgabe beschreiben.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-114">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="f3fa9-115">Erstellen Sie einen Logon-Trigger mithilfe der [**Taskdefinition.**](taskdefinition-triggers.md) Triggers-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-115">Create a logon trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="f3fa9-116">Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection**](triggercollection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-116">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="f3fa9-117">Verwenden Sie die [**TriggerCollection. Create**](triggercollection-create.md) -Methode (die den Typ des zu erstellenden Auslösers angibt), um einen Logon-Trigger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-117">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a logon trigger.</span></span> <span data-ttu-id="f3fa9-118">Beim Erstellen des Auslösers legen Sie die Start-und die Endgrenze des Auslösers zum Aktivieren und Deaktivieren des-Auslösers fest.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-118">As you create the trigger, set the start boundary and end boundary of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="f3fa9-119">Sie müssen die [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) -Eigenschaft für den-Befehl so festlegen, dass die Aktionen der Aufgabe für die Ausführung geplant werden, wenn sich der angegebene Benutzer nach der Start Grenze anmeldet.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-119">You must set the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property for the trigger so that the task's actions will be scheduled to execute when the specified user logs on after the start boundary.</span></span>
5.  <span data-ttu-id="f3fa9-120">Erstellen Sie eine Aktion für die Ausführung der Aufgabe, indem Sie die [**Task Definition. Actions**](taskdefinition-actions.md) -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-120">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="f3fa9-121">Diese Eigenschaft ermöglicht den Zugriff auf das Objekt " [**Aktions Sammlung**](actioncollection.md) ".</span><span class="sxs-lookup"><span data-stu-id="f3fa9-121">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="f3fa9-122">Verwenden Sie die [**Action Collection. Create**](actioncollection-create.md) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-122">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="f3fa9-123">In diesem Beispiel wird ein [**execaction**](execaction.md) -Objekt verwendet, das eine Aktion darstellt, die eine ausführbare Datei startet.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-123">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="f3fa9-124">Registrieren Sie die Aufgabe mit der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-124">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="f3fa9-125">In diesem Beispiel wird die Aufgabe so registriert, dass Sie die Gruppe "Administratoren" als Sicherheitskontext zum Ausführen der Aufgabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-125">This example registers the task so that it uses the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="f3fa9-126">Im folgenden VBScript-Beispiel wird veranschaulicht, wie eine Aufgabe für die Ausführung von Notepad geplant wird, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="f3fa9-126">The following VBScript example shows how to schedule a task to execute Notepad when a user logs on.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f3fa9-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f3fa9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3fa9-128">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="f3fa9-128">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




