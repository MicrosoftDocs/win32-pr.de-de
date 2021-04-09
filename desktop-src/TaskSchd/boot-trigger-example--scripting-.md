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
# <a name="boot-trigger-example-scripting"></a><span data-ttu-id="8b1b5-103">Beispiel für einen Start-Beispiel (Skripterstellung)</span><span class="sxs-lookup"><span data-stu-id="8b1b5-103">Boot Trigger Example (Scripting)</span></span>

<span data-ttu-id="8b1b5-104">In diesem Skript Beispiel wird veranschaulicht, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad geplant ist, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-104">This scripting example shows how to create a task that is scheduled to execute Notepad when the system is booted.</span></span> <span data-ttu-id="8b1b5-105">Der Task enthält einen Start--Fehler, der eine Start Grenze und eine Verzögerungszeit angibt, nach der der Task gestartet wird, nachdem das System gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-105">The task contains a boot trigger that specifies a start boundary and delay time for the task to start after the system is booted.</span></span> <span data-ttu-id="8b1b5-106">Der Task enthält auch eine Aktion, die den Task zum Ausführen von Notepad angibt.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-106">The task also contains an action that specifies the task to execute Notepad.</span></span> <span data-ttu-id="8b1b5-107">Der Task wird mit dem lokalen Dienst Konto als Sicherheitskontext registriert, um den Task auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-107">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="8b1b5-108">Im folgenden Verfahren wird beschrieben, wie eine ausführbare Datei, z. b. Notepad, beim Starten des Systems gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-108">The following procedure describes how to schedule an executable such as Notepad to start when the system is booted.</span></span>

<span data-ttu-id="8b1b5-109">**So planen Sie den Start von Notepad, wenn das System gestartet wird**</span><span class="sxs-lookup"><span data-stu-id="8b1b5-109">**To schedule Notepad to start when the system is booted**</span></span>

1.  <span data-ttu-id="8b1b5-110">Erstellen Sie ein [**TaskService**](taskservice.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-110">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="8b1b5-111">Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-111">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="8b1b5-112">Rufen Sie einen Aufgaben Ordner ab, und erstellen Sie eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-112">Get a task folder and create a task.</span></span> <span data-ttu-id="8b1b5-113">Verwenden Sie die [**TaskService. GetFolder**](taskservice-getfolder.md) -Methode, um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService. newtask**](taskservice-newtask.md) -Methode zum Erstellen des [**Task Definition**](taskdefinition.md) -Objekts, das die Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-113">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="8b1b5-114">Definieren von Informationen über den Task mithilfe des [**Taskdefinition**](taskdefinition.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-114">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="8b1b5-115">Verwenden Sie die [**Task Definition. Settings**](taskdefinition-settings.md) -Eigenschaft, um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner Dienst den Task ausführt, und die [**Taskdefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) -Eigenschaft, um die Informationen zu definieren, die die Aufgabe beschreiben.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-115">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="8b1b5-116">Erstellen Sie einen Logon-Trigger mithilfe der [**Taskdefinition.**](taskdefinition-triggers.md) Triggers-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-116">Create a logon trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="8b1b5-117">Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection**](triggercollection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-117">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="8b1b5-118">Verwenden Sie die [**TriggerCollection. Create**](triggercollection-create.md) -Methode (die den Typ des zu erstellenden Auslösers angibt), um einen Start Trigger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-118">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a boot trigger.</span></span> <span data-ttu-id="8b1b5-119">Legen Sie beim Erstellen des Auslösers die Eigenschaften [**StartBoundary**](trigger-startboundary.md) und [**endboundary**](trigger-endboundary.md) des Auslösers auf Aktivieren und Deaktivieren des Auslösers fest.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-119">As you create the trigger, set the [**StartBoundary**](trigger-startboundary.md) and [**EndBoundary**](trigger-endboundary.md) properties of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="8b1b5-120">Sie können auch einen Wert für die [**Delay**](boottrigger-delay.md) -Eigenschaft des Start-Auslösers angeben.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-120">You can also specify a value for the [**Delay**](boottrigger-delay.md) property of the boot trigger.</span></span>
5.  <span data-ttu-id="8b1b5-121">Erstellen Sie eine Aktion für die Ausführung der Aufgabe, indem Sie die [**Task Definition. Actions**](taskdefinition-actions.md) -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-121">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="8b1b5-122">Diese Eigenschaft ermöglicht den Zugriff auf das Objekt " [**Aktions Sammlung**](actioncollection.md) ".</span><span class="sxs-lookup"><span data-stu-id="8b1b5-122">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="8b1b5-123">Verwenden Sie die [**Action Collection. Create**](actioncollection-create.md) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-123">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="8b1b5-124">In diesem Beispiel wird ein [**execaction**](execaction.md) -Objekt verwendet, das eine Aktion darstellt, die eine ausführbare Datei startet.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-124">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="8b1b5-125">Registrieren Sie die Aufgabe mit der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-125">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="8b1b5-126">Der Task wird mit dem lokalen Dienst Konto als Sicherheitskontext registriert, um den Task auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-126">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="8b1b5-127">Im folgenden VBScript-Beispiel wird veranschaulicht, wie Sie einen Task zum Ausführen von Notepad 30 Sekunden nach dem Starten des Systems planen.</span><span class="sxs-lookup"><span data-stu-id="8b1b5-127">The following VBScript example shows how to schedule a task to execute Notepad 30 seconds after the system is booted.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8b1b5-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8b1b5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b1b5-129">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="8b1b5-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




