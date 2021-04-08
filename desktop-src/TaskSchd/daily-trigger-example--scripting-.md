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
# <a name="daily-trigger-example-scripting"></a><span data-ttu-id="5c859-103">Beispiel für den täglichen Auslösung (Skripterstellung)</span><span class="sxs-lookup"><span data-stu-id="5c859-103">Daily Trigger Example (Scripting)</span></span>

<span data-ttu-id="5c859-104">In diesem Skript Beispiel wird gezeigt, wie Sie einen Task erstellen, der den Notepad täglich um 8:00 Uhr ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c859-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="5c859-105">Der Task enthält einen täglichen-Triggertyp, der eine Start Grenze zum Aktivieren des Auslösers angibt und die Uhrzeit angibt, zu der der Task ausgeführt wird, ein triggerintervall, das angibt, dass der Task jeden Tag ausgeführt wird, und eine Endgrenze, um den Triggervorgang zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="5c859-105">The task contains a daily trigger that specifies a start boundary to activate the trigger and to specify the time of day that the task runs, a trigger interval to specify that the task runs every day, and an end boundary to deactivates the trigger.</span></span> <span data-ttu-id="5c859-106">Das Beispiel zeigt auch, wie Sie ein Wiederholungsmuster für den-Vorgang festlegen, um die Aufgabe zu wiederholen.</span><span class="sxs-lookup"><span data-stu-id="5c859-106">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span> <span data-ttu-id="5c859-107">Der Task enthält auch eine ausführbare Aktion, die den Notepad ausführt.</span><span class="sxs-lookup"><span data-stu-id="5c859-107">The task also contains an executable action that runs Notepad.</span></span>

<span data-ttu-id="5c859-108">Im folgenden Verfahren wird beschrieben, wie eine Aufgabe zum Starten einer ausführbaren Datei täglich um 8:00 Uhr geplant wird.</span><span class="sxs-lookup"><span data-stu-id="5c859-108">The following procedure describes how to schedule a task to start an executable at 8:00 AM every day.</span></span> <span data-ttu-id="5c859-109">(Diese Schritte entsprechen den Code Kommentaren, die im Beispielcode enthalten sind.)</span><span class="sxs-lookup"><span data-stu-id="5c859-109">(These steps correspond to the code comments included in the example code.)</span></span>

<span data-ttu-id="5c859-110">**So planen Sie den Start von Notepad täglich um 8:00 Uhr**</span><span class="sxs-lookup"><span data-stu-id="5c859-110">**To schedule Notepad to start at 8:00 AM every day**</span></span>

1.  <span data-ttu-id="5c859-111">Erstellen Sie ein [**TaskService**](taskservice.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5c859-111">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="5c859-112">Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="5c859-112">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="5c859-113">Rufen Sie einen Aufgaben Ordner ab, und erstellen Sie eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="5c859-113">Get a task folder and create a task.</span></span> <span data-ttu-id="5c859-114">Verwenden Sie die [**TaskService. GetFolder**](taskservice-getfolder.md) -Methode, um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService. newtask**](taskservice-newtask.md) -Methode zum Erstellen des [**Task Definition**](taskdefinition.md) -Objekts, das die Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="5c859-114">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="5c859-115">Definieren von Informationen über den Task mithilfe des [**Taskdefinition**](taskdefinition.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="5c859-115">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="5c859-116">Verwenden Sie die [**Task Definition. Settings**](taskdefinition-settings.md) -Eigenschaft, um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner Dienst den Task ausführt, und die [**Taskdefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) -Eigenschaft, um die Informationen zu definieren, die die Aufgabe beschreiben.</span><span class="sxs-lookup"><span data-stu-id="5c859-116">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="5c859-117">Erstellen Sie einen täglichen Trigger mithilfe der [**Taskdefinition.**](taskdefinition-triggers.md) Triggers-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5c859-117">Create a daily trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="5c859-118">Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection**](triggercollection.md) -Objekt, das verwendet wird, um den Trigger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5c859-118">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span> <span data-ttu-id="5c859-119">Verwenden Sie die [**TriggerCollection. Create**](triggercollection-create.md) -Methode (gibt den Typ des zu erstellenden Auslösers an), um einen täglichen Trigger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5c859-119">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a daily trigger.</span></span> <span data-ttu-id="5c859-120">Legen Sie beim Erstellen des Auslösers die Start Grenze fest, um den-Triggervorgang zu aktivieren, und geben Sie die Uhrzeit an, zu der der Task ausgeführt wird, das Intervall zwischen den Tagen und die Endgrenze, um den-Triggervorgang</span><span class="sxs-lookup"><span data-stu-id="5c859-120">As you create the trigger, set the start boundary to activate the trigger and specify the time of day that the task runs, the interval between the days, and the end boundary to deactivate the trigger.</span></span> <span data-ttu-id="5c859-121">Im folgenden Beispiel wird gezeigt, wie Sie ein Wiederholungsmuster für den-Vorgang festlegen, um die Aufgabe zu wiederholen.</span><span class="sxs-lookup"><span data-stu-id="5c859-121">The example below shows how to set a repetition pattern for the trigger to repeat the task.</span></span>
5.  <span data-ttu-id="5c859-122">Erstellen Sie eine Aktion für die Ausführung der Aufgabe, indem Sie die [**Task Definition. Actions**](taskdefinition-actions.md) -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c859-122">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="5c859-123">Diese Eigenschaft ermöglicht den Zugriff auf das " [**Action Collection**](actioncollection.md) "-Objekt, das zum Erstellen der Aktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c859-123">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="5c859-124">Verwenden Sie die [**Action Collection. Create**](actioncollection-create.md) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="5c859-124">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="5c859-125">In diesem Beispiel wird ein [**execaction**](execaction.md) -Objekt verwendet, das eine Aktion darstellt, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="5c859-125">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="5c859-126">Registrieren Sie die Aufgabe mit der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5c859-126">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="5c859-127">In diesem Beispiel startet der Task Notepad täglich um 8:00 Uhr.</span><span class="sxs-lookup"><span data-stu-id="5c859-127">For this example the task will start Notepad at 8:00 AM every day.</span></span>

<span data-ttu-id="5c859-128">Im folgenden VBScript-Beispiel wird gezeigt, wie ein Task zum Ausführen von Notepad jeden Tag um 8:00 Uhr geplant wird.</span><span class="sxs-lookup"><span data-stu-id="5c859-128">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5c859-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c859-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c859-130">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="5c859-130">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




