---
title: Task Trigger
description: Ein-Triggersatz besteht aus einer Reihe von Kriterien, die die Ausführung einer Aufgabe starten, wenn diese erfüllt ist.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- Erstellen von Triggern Taskplaner
- Trigger Taskplaner
- Trigger Taskplaner, beschrieben
- Trigger Taskplaner, Zeit basiert
- Trigger Taskplaner, Ereignis basiert
- ereignisbasierte Trigger Taskplaner
- Zeitbasierte Trigger Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465dfa015be19ff220a77d3c85f0cbb223c4899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206403"
---
# <a name="task-triggers"></a><span data-ttu-id="b71ba-110">Task Trigger</span><span class="sxs-lookup"><span data-stu-id="b71ba-110">Task Triggers</span></span>

<span data-ttu-id="b71ba-111">Ein-Triggersatz besteht aus einer Reihe von Kriterien, die die Ausführung einer Aufgabe starten, wenn diese erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="b71ba-111">A trigger is a set of criteria that, when met, starts the execution of a task.</span></span> <span data-ttu-id="b71ba-112">Taskplaner bietet zeitbasierte und ereignisbasierte Trigger, die eine Aufgabe auf verschiedene Arten starten können.</span><span class="sxs-lookup"><span data-stu-id="b71ba-112">Task Scheduler provides both time-based and event-based triggers that can start a task in several different ways.</span></span> <span data-ttu-id="b71ba-113">Eine bestimmte Aufgabe kann von einem oder mehreren Triggern gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="b71ba-113">A given task can be started by one or more triggers.</span></span> <span data-ttu-id="b71ba-114">Eine Aufgabe kann maximal 48 Trigger aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b71ba-114">A task can have a maximum of 48 triggers.</span></span>

## <a name="time-based-triggers"></a><span data-ttu-id="b71ba-115">Zeitbasierte Trigger</span><span class="sxs-lookup"><span data-stu-id="b71ba-115">Time-based Triggers</span></span>

<span data-ttu-id="b71ba-116">Zeitbasierte Trigger starten Tasks zu bestimmten Zeiten.</span><span class="sxs-lookup"><span data-stu-id="b71ba-116">Time-based triggers start tasks at specified times.</span></span> <span data-ttu-id="b71ba-117">Dies umfasst das einmalige Starten der Aufgabe zu einem bestimmten Zeitpunkt oder das mehrfache Starten der Aufgabe an einem täglichen, wöchentlichen, monatlichen oder monatlichen Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="b71ba-117">This includes starting the task once at a specific time or starting the task multiple times on a daily, weekly, monthly, or monthly day-of-week schedule.</span></span>

## <a name="event-based-triggers"></a><span data-ttu-id="b71ba-118">Ereignisbasierte Trigger</span><span class="sxs-lookup"><span data-stu-id="b71ba-118">Event-based Triggers</span></span>

<span data-ttu-id="b71ba-119">Ereignisbasierte Trigger starten eine Aufgabe als Reaktion auf bestimmte Systemereignisse.</span><span class="sxs-lookup"><span data-stu-id="b71ba-119">Event-based triggers start a task in response to certain system events.</span></span> <span data-ttu-id="b71ba-120">Ereignisbasierte Trigger können z. b. so festgelegt werden, dass eine Aufgabe gestartet wird, wenn das System gestartet wird, wenn sich ein Benutzer am lokalen Computer anmeldet oder wenn sich das System im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="b71ba-120">For example, event-based triggers can be set to start a task when the system starts up, when a user logs on to the local computer, or when the system becomes idle.</span></span>

## <a name="multiple-triggers"></a><span data-ttu-id="b71ba-121">Mehrere Trigger</span><span class="sxs-lookup"><span data-stu-id="b71ba-121">Multiple Triggers</span></span>

<span data-ttu-id="b71ba-122">Jeder Task kann von einem oder mehreren Triggern gestartet werden, sodass die Aufgabe auf eine beliebige Anzahl von Arten gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b71ba-122">Each task can be started by one or more triggers, allowing the task to be started in any number of ways.</span></span> <span data-ttu-id="b71ba-123">In Taskplaner 1,0 und Taskplaner 2,0 werden jedoch mehrere Trigger anders implementiert.</span><span class="sxs-lookup"><span data-stu-id="b71ba-123">However, multiple triggers are implemented differently in Task Scheduler 1.0 and Task Scheduler 2.0.</span></span>

<span data-ttu-id="b71ba-124">In Taskplaner 2,0 wird jeder-Vorgang durch eine separate-auslöserapi definiert, die mit der-Aufgabe über die-auslöserauflistung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="b71ba-124">In Task Scheduler 2.0, each trigger is defined by a separate trigger API that is associated with the task through the trigger collection.</span></span>

<span data-ttu-id="b71ba-125">In Taskplaner 1,0 können mehrere Trigger als Zeitplan betrachtet werden. Dies ist ein Satz von Uhrzeiten, zu denen die Aufgabe gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b71ba-125">In Task Scheduler 1.0, multiple triggers can be thought of as a schedule, a set of times at which the task starts.</span></span> <span data-ttu-id="b71ba-126">In diesem Fall ist der Zeitplan der Satz von Uhrzeiten (angegeben durch die Vereinigung aller Trigger, die mit dem Arbeits Element verknüpft sind), bei denen ein Arbeits Element ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b71ba-126">In this case, the schedule is the set of times (specified by the union of all of the triggers associated with the work item) at which a work item will execute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b71ba-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b71ba-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b71ba-128">Wiederholen einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="b71ba-128">Repeating A Task</span></span>](repeating-a-task.md)
</dt> <dt>

[<span data-ttu-id="b71ba-129">Auslösertypen</span><span class="sxs-lookup"><span data-stu-id="b71ba-129">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="b71ba-130">Auslöse Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b71ba-130">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> <dt>

[<span data-ttu-id="b71ba-131">Informationen zum Taskplaner</span><span class="sxs-lookup"><span data-stu-id="b71ba-131">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




