---
title: Beispiel für Registrierungs Beispiel (Skripterstellung)
description: In diesem Skript Beispiel wird gezeigt, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad geplant ist, wenn ein Task registriert wird.
ms.assetid: 956b3a21-7d36-4d06-be84-690884ba653a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bce6271927e74e31f25b3ac86783b35899bbd862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311418"
---
# <a name="registration-trigger-example-scripting"></a><span data-ttu-id="9364e-103">Beispiel für Registrierungs Beispiel (Skripterstellung)</span><span class="sxs-lookup"><span data-stu-id="9364e-103">Registration Trigger Example (Scripting)</span></span>

<span data-ttu-id="9364e-104">In diesem Skript Beispiel wird gezeigt, wie eine Aufgabe erstellt wird, die für die Ausführung von Notepad geplant ist, wenn ein Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="9364e-104">This scripting example shows how to create a task that is scheduled to execute Notepad when a task is registered.</span></span> <span data-ttu-id="9364e-105">Der Task enthält einen Registrierungs--Auslösung, der eine Start Grenze und eine Endgrenze für den Task angibt.</span><span class="sxs-lookup"><span data-stu-id="9364e-105">The task contains a registration trigger that specifies a start boundary and an end boundary for the task.</span></span> <span data-ttu-id="9364e-106">Die Start Grenze gibt an, wann der-Auslösers aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="9364e-106">The start boundary specifies when the trigger is activated.</span></span> <span data-ttu-id="9364e-107">Der Task enthält auch eine Aktion, die den Task zum Ausführen von Notepad angibt.</span><span class="sxs-lookup"><span data-stu-id="9364e-107">The task also contains an action that specifies the task to execute Notepad.</span></span>

> [!Note]  
> <span data-ttu-id="9364e-108">Wenn eine Aufgabe mit einem Registrierungs-ausgelöst wird, wird die Aufgabe ausgeführt, nachdem das Update ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="9364e-108">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

<span data-ttu-id="9364e-109">Im folgenden Verfahren wird beschrieben, wie eine ausführbare Datei (z. b. Notepad) gestartet wird, wenn ein Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="9364e-109">The following procedure describes how to schedule an executable such as Notepad to start when a task is registered.</span></span>

<span data-ttu-id="9364e-110">**So planen Sie den Start von Notepad, wenn ein Task registriert wird**</span><span class="sxs-lookup"><span data-stu-id="9364e-110">**To schedule Notepad to start when a task is registered**</span></span>

1.  <span data-ttu-id="9364e-111">Erstellen Sie ein [**TaskService**](taskservice.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9364e-111">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="9364e-112">Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="9364e-112">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="9364e-113">Rufen Sie einen Aufgaben Ordner ab, und erstellen Sie eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="9364e-113">Get a task folder and create a task.</span></span> <span data-ttu-id="9364e-114">Verwenden Sie die [**TaskService. GetFolder**](taskservice-getfolder.md) -Methode, um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService. newtask**](taskservice-newtask.md) -Methode zum Erstellen des [**Task Definition**](taskdefinition.md) -Objekts, das die Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="9364e-114">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="9364e-115">Definieren von Informationen über den Task mithilfe des [**Taskdefinition**](taskdefinition.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="9364e-115">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="9364e-116">Verwenden Sie die [**Task Definition. Settings**](taskdefinition-settings.md) -Eigenschaft, um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner Dienst den Task ausführt, und die [**Taskdefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) -Eigenschaft, um die Informationen zu definieren, die die Aufgabe beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9364e-116">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="9364e-117">Erstellen Sie einen Registrierungs Trigger mithilfe der [**Taskdefinition.**](taskdefinition-triggers.md) Triggers-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9364e-117">Create a registration trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="9364e-118">Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection**](triggercollection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9364e-118">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="9364e-119">Verwenden Sie die [**TriggerCollection. Create**](triggercollection-create.md) -Methode (die den Typ des zu erstellenden Auslösers angibt), um einen Registrierungs Trigger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9364e-119">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger that you want to create) to create a registration trigger.</span></span>
5.  <span data-ttu-id="9364e-120">Erstellen Sie eine Aktion für die Ausführung der Aufgabe, indem Sie die [**Task Definition. Actions**](taskdefinition-actions.md) -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="9364e-120">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="9364e-121">Diese Eigenschaft ermöglicht den Zugriff auf das Objekt " [**Aktions Sammlung**](actioncollection.md) ".</span><span class="sxs-lookup"><span data-stu-id="9364e-121">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="9364e-122">Verwenden Sie die [**Action Collection. Create**](actioncollection-create.md) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="9364e-122">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="9364e-123">In diesem Beispiel wird ein [**execaction**](execaction.md) -Objekt verwendet, das eine Aktion darstellt, die eine ausführbare Datei startet.</span><span class="sxs-lookup"><span data-stu-id="9364e-123">This example uses an [**ExecAction**](execaction.md) object, which represents an action that starts an executable.</span></span>
6.  <span data-ttu-id="9364e-124">Registrieren Sie die Aufgabe mit der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9364e-124">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span>

<span data-ttu-id="9364e-125">Im folgenden VBScript-Beispiel wird gezeigt, wie eine Aufgabe erstellt wird, die die Ausführung von Notepad plant, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="9364e-125">The following VBScript example shows how to create a task that schedules Notepad to execute when the task is registered.</span></span>


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when
' the task is registered.
'---------------------------------------------------------

' A constant that specifies a registration trigger.
const TriggerTypeRegistration = 7
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
regInfo.Description = "Start Notepad when the task is registered."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a registration trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeRegistration)

trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "RegistrationTriggerId"   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes Notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Registration Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a><span data-ttu-id="9364e-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9364e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9364e-127">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="9364e-127">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




