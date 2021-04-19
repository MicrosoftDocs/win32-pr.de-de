---
title: Beispiel für Zeit Auslösung (Skripterstellung)
description: In diesem Skript Beispiel wird gezeigt, wie eine Aufgabe erstellt wird, die den Editor zu einem bestimmten Zeitpunkt ausführt.
ms.assetid: 8511ffcd-166f-4c63-9cd2-ead53dde9ed8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77cbf9eab12f5ca027fbb6c48ade37a9f57d9beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339397"
---
# <a name="time-trigger-example-scripting"></a><span data-ttu-id="7ffa3-103">Beispiel für Zeit Auslösung (Skripterstellung)</span><span class="sxs-lookup"><span data-stu-id="7ffa3-103">Time Trigger Example (Scripting)</span></span>

<span data-ttu-id="7ffa3-104">In diesem Skript Beispiel wird gezeigt, wie eine Aufgabe erstellt wird, die den Editor zu einem bestimmten Zeitpunkt ausführt.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-104">This scripting example shows how to create a task that runs Notepad at a specific time.</span></span> <span data-ttu-id="7ffa3-105">Der Task enthält einen zeitbasierten-Triggerwert, der eine Start Grenze zum Aktivieren des Tasks, eine ausführbare Aktion, die den Editor ausführt, und eine endbegrenzung zum Deaktivieren der Aufgabe angibt.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-105">The task contains a time-based trigger that specifies a start boundary to activate the task, an executable action that runs Notepad, and an end boundary that deactivates the task.</span></span>

<span data-ttu-id="7ffa3-106">Im folgenden Verfahren wird beschrieben, wie eine Aufgabe zum Starten einer ausführbaren Datei zu einem bestimmten Zeitpunkt geplant wird.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-106">The following procedure describes how to schedule a task to start an executable at a specific time.</span></span>

<span data-ttu-id="7ffa3-107">**So planen Sie den Start von Notepad zu einem bestimmten Zeitpunkt**</span><span class="sxs-lookup"><span data-stu-id="7ffa3-107">**To Schedule Notepad to start at a Specific Time**</span></span>

1.  <span data-ttu-id="7ffa3-108">Erstellen Sie ein [**TaskService**](taskservice.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-108">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="7ffa3-109">Mit diesem Objekt können Sie die Aufgabe in einem angegebenen Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-109">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="7ffa3-110">Rufen Sie einen Aufgaben Ordner ab, und erstellen Sie eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-110">Get a task folder and create a task.</span></span> <span data-ttu-id="7ffa3-111">Verwenden Sie die [**TaskService. GetFolder**](taskservice-getfolder.md) -Methode, um den Ordner zu erhalten, in dem die Aufgabe gespeichert ist, und die [**TaskService. newtask**](taskservice-newtask.md) -Methode zum Erstellen des [**Task Definition**](taskdefinition.md) -Objekts, das die Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-111">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="7ffa3-112">Definieren von Informationen über den Task mithilfe des [**Taskdefinition**](taskdefinition.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-112">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="7ffa3-113">Verwenden Sie die [**Task Definition. Settings**](taskdefinition-settings.md) -Eigenschaft, um die Einstellungen zu definieren, die bestimmen, wie der Taskplaner Dienst den Task ausführt, und die [**Taskdefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) -Eigenschaft, um die Informationen zu definieren, die die Aufgabe beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-113">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="7ffa3-114">Erstellen Sie einen zeitbasierten Trigger mithilfe der [**Task Definition.**](taskdefinition-triggers.md) Triggers-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-114">Create a time-based trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="7ffa3-115">Diese Eigenschaft ermöglicht den Zugriff auf das [**TriggerCollection**](triggercollection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-115">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="7ffa3-116">Verwenden Sie die [**TriggerCollection. Create**](triggercollection-create.md) -Methode (gibt den Typ des zu erstellenden Auslösers an), um einen zeitbasierten Trigger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-116">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a time-based trigger.</span></span> <span data-ttu-id="7ffa3-117">Beim Erstellen des Auslösers legen Sie die Start-und die Endgrenze des Auslösers zum Aktivieren und Deaktivieren des-Auslösers fest.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-117">As you create the trigger, set the start boundary and end boundary of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="7ffa3-118">Die Start Grenze gibt an, wann die Aktion der Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-118">The start boundary specifies when the task's action will be performed.</span></span>
5.  <span data-ttu-id="7ffa3-119">Erstellen Sie eine Aktion für die Ausführung der Aufgabe, indem Sie die [**Task Definition. Actions**](taskdefinition-actions.md) -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-119">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="7ffa3-120">Diese Eigenschaft ermöglicht den Zugriff auf das Objekt " [**Aktions Sammlung**](actioncollection.md) ".</span><span class="sxs-lookup"><span data-stu-id="7ffa3-120">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="7ffa3-121">Verwenden Sie die [**Action Collection. Create**](actioncollection-create.md) -Methode, um den Typ der Aktion anzugeben, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-121">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="7ffa3-122">In diesem Beispiel wird ein [**execaction**](execaction.md) -Objekt verwendet, das eine Aktion darstellt, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-122">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="7ffa3-123">Registrieren Sie die Aufgabe mit der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-123">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="7ffa3-124">In diesem Beispiel startet der Task Notepad zum aktuellen Zeitpunkt plus 30 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-124">For this example the task will start Notepad at the current time plus 30 seconds.</span></span>

<span data-ttu-id="7ffa3-125">Im folgenden VBScript-Beispiel wird veranschaulicht, wie Sie einen Task zum Ausführen von Notepad 30 Sekunden nach dem Registrieren der Aufgabe planen.</span><span class="sxs-lookup"><span data-stu-id="7ffa3-125">The following VBScript example shows how to schedule a task to execute Notepad 30 seconds after the task is registered.</span></span>


```VB
'------------------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds
' from the time the task is registered.
'------------------------------------------------------------------

' A constant that specifies a time-based trigger.
const TriggerTypeTime = 1
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
regInfo.Description = "Start notepad at a certain time"
regInfo.Author = "Author Name"

'********************************************************
' Set the principal for the task
Dim principal
Set principal = taskDefinition.Principal

' Set the logon type to interactive logon
principal.LogonType = 3


' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a time-based trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeTime)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime

Dim time
time = DateAdd("s", 30, Now)  'start time = 30 seconds from now
startTime = XmlTime(time)

time = DateAdd("n", 5, Now) 'end time = 5 minutes from now
endTime = XmlTime(time)

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "TimeTriggerId"
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
    "Test TimeTrigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."



'------------------------------------------------------------------
' Used to get the time for the trigger 
' startBoundary and endBoundary.
' Return the time in the correct format: 
' YYYY-MM-DDTHH:MM:SS. 
'------------------------------------------------------------------
Function XmlTime(t)
    Dim cSecond, cMinute, CHour, cDay, cMonth, cYear
    Dim tTime, tDate

    cSecond = "0" & Second(t)
    cMinute = "0" & Minute(t)
    cHour = "0" & Hour(t)
    cDay = "0" & Day(t)
    cMonth = "0" & Month(t)
    cYear = Year(t)

    tTime = Right(cHour, 2) & ":" & Right(cMinute, 2) & _
        ":" & Right(cSecond, 2)
    tDate = cYear & "-" & Right(cMonth, 2) & "-" & Right(cDay, 2)
    XmlTime = tDate & "T" & tTime 
End Function

```



## <a name="related-topics"></a><span data-ttu-id="7ffa3-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7ffa3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ffa3-127">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="7ffa3-127">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




