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
# <a name="weekly-trigger-example-scripting"></a><span data-ttu-id="6409e-103">Beispiel für einen wöchentlichen Auslösung (Skripterstellung)</span><span class="sxs-lookup"><span data-stu-id="6409e-103">Weekly Trigger Example (Scripting)</span></span>

<span data-ttu-id="6409e-104">In diesem Skript Beispiel wird gezeigt, wie Sie einen Task erstellen, der den Notepad um 8:00 Uhr am Montag jeder Woche ausführt.</span><span class="sxs-lookup"><span data-stu-id="6409e-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM on Monday of every week.</span></span> <span data-ttu-id="6409e-105">Der Task enthält einen täglichen-Triggerwert, der angibt, wann der Task ausgeführt wird, und eine ausführbare Aktion, die Editor ausführt.</span><span class="sxs-lookup"><span data-stu-id="6409e-105">The task contains a daily trigger that specifies when the task runs and an executable action that runs Notepad.</span></span>

<span data-ttu-id="6409e-106">Im folgenden Verfahren wird beschrieben, wie eine Aufgabe zum Starten einer ausführbaren Datei um 8:00 Uhr am Montag jeder Woche geplant wird.</span><span class="sxs-lookup"><span data-stu-id="6409e-106">The following procedure describes how to schedule a task to start an executable at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="6409e-107">**So planen Sie den Start von Notepad um 8:00 Uhr am Montag jeder Woche**</span><span class="sxs-lookup"><span data-stu-id="6409e-107">**To schedule Notepad to start at 8:00 AM on Monday of every week**</span></span>

1.  <span data-ttu-id="6409e-108">Erstellen Sie ein [**TaskService**](taskservice.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6409e-108">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="6409e-109">Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="6409e-109">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="6409e-110">Rufen Sie einen Aufgaben Ordner ab, und erstellen Sie eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="6409e-110">Get a task folder and create a task.</span></span> <span data-ttu-id="6409e-111">Verwenden Sie die [**TaskService. GetFolder**](taskservice-getfolder.md) -Methode, um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService. newtask**](taskservice-newtask.md) -Methode zum Erstellen des [**Task Definition**](taskdefinition.md) -Objekts, das die Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="6409e-111">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="6409e-112">Definieren von Informationen über den Task mithilfe des [**Taskdefinition**](taskdefinition.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="6409e-112">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="6409e-113">Verwenden Sie die [**Task Definition. Settings**](taskdefinition-settings.md) -Eigenschaft, um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner Dienst den Task ausführt, und die [**Taskdefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) -Eigenschaft, um die Informationen zu definieren, die die Aufgabe beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6409e-113">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="6409e-114">Erstellen Sie einen wöchentlichen Trigger mithilfe der [**Taskdefinition.**](taskdefinition-triggers.md) Triggers-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6409e-114">Create a weekly trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="6409e-115">Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection**](triggercollection.md) -Objekt, das verwendet wird, um den Trigger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6409e-115">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span>

    <span data-ttu-id="6409e-116">Verwenden Sie die [**TriggerCollection. Create**](triggercollection-create.md) -Methode (gibt den Typ des zu erstellenden Auslösers an), um einen wöchentlichen Trigger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6409e-116">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a weekly trigger.</span></span>

    <span data-ttu-id="6409e-117">Legen Sie die Eigenschaft " [**weeklyauslöst. StartBoundary**](trigger-startboundary.md) " fest, um anzugeben, wann der ausgelöst wird, und die Uhrzeit, zu der die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6409e-117">Set the [**WeeklyTrigger.StartBoundary**](trigger-startboundary.md) property to specify when the trigger is activated and the time of the day when the task is run.</span></span> <span data-ttu-id="6409e-118">In diesem Beispiel wird der-Triggern am 1. Januar 2005 aktiviert, und der Task wird um 8:00 Uhr ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6409e-118">In this example the trigger is activated on January 1, 2005 and the task runs at 8:00 AM.</span></span>

    <span data-ttu-id="6409e-119">Legen Sie die Eigenschaft [**weeklyauslöst. endboundary**](trigger-endboundary.md)auf fest, wenn der-Fehler deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="6409e-119">Set the [**WeeklyTrigger.EndBoundary**](trigger-endboundary.md)property to specify when the trigger is deactivated.</span></span> <span data-ttu-id="6409e-120">In diesem Beispiel wird der-Wert am 1. Januar 2015 deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6409e-120">In this example the trigger is deactivated on January 1, 2015.</span></span>

    <span data-ttu-id="6409e-121">Legen Sie die Eigenschaft [**weeklytrigger\daysofweek**](weeklytrigger-daysofweek.md) fest, um die Tage der Woche anzugeben, an denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6409e-121">Set the [**WeeklyTrigger.DaysOfWeek**](weeklytrigger-daysofweek.md) property to specify the days of the week on which the task runs.</span></span> <span data-ttu-id="6409e-122">In diesem Beispiel wird die Aufgabe am Montag ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6409e-122">In this example the task is run on Monday.</span></span>

    <span data-ttu-id="6409e-123">Legen Sie die Eigenschaft " [**weeklyauth. weeksinterval**](weeklytrigger-weeksinterval.md)" fest, um das Intervall zwischen den Wochen im Zeitplan anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6409e-123">Set the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md)property to specify the interval between the weeks in the schedule.</span></span> <span data-ttu-id="6409e-124">In diesem Beispiel wird die Aufgabe wöchentlich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6409e-124">In this example the task runs every week.</span></span>

5.  <span data-ttu-id="6409e-125">Erstellen Sie eine Aktion für die Ausführung der Aufgabe, indem Sie die [**Task Definition. Actions**](taskdefinition-actions.md) -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="6409e-125">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="6409e-126">Diese Eigenschaft ermöglicht den Zugriff auf das " [**Action Collection**](actioncollection.md) "-Objekt, das zum Erstellen der Aktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6409e-126">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="6409e-127">Verwenden Sie die [**Action Collection. Create**](actioncollection-create.md) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="6409e-127">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="6409e-128">In diesem Beispiel wird ein [**execaction**](execaction.md) -Objekt verwendet, das eine Aktion darstellt, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="6409e-128">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="6409e-129">Registrieren Sie die Aufgabe mit der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6409e-129">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="6409e-130">In diesem Beispiel startet der Task Notepad um 8:00 Uhr am Montag jeder Woche.</span><span class="sxs-lookup"><span data-stu-id="6409e-130">For this example the task will start Notepad at 8:00 AM on Monday of every week.</span></span>

<span data-ttu-id="6409e-131">Im folgenden VBScript-Beispiel wird gezeigt, wie ein Task zum Ausführen von Notepad jeden Tag um 8:00 Uhr geplant wird.</span><span class="sxs-lookup"><span data-stu-id="6409e-131">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6409e-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6409e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6409e-133">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="6409e-133">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




