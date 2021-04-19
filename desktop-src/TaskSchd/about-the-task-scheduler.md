---
title: Informationen zum Taskplaner
description: Mit dem Taskplaner-Dienst können Sie automatisierte Aufgaben auf einem ausgewählten Computer ausführen.
ms.assetid: 13816b8b-3090-4d17-86bb-8e632ca0cd37
keywords:
- Taskplaner Taskplaner, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6022546550efe32504dd0a3d12c94163e78214f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341868"
---
# <a name="about-the-task-scheduler"></a><span data-ttu-id="c3c46-104">Informationen zum Taskplaner</span><span class="sxs-lookup"><span data-stu-id="c3c46-104">About the Task Scheduler</span></span>

<span data-ttu-id="c3c46-105">Mit dem Taskplaner-Dienst können Sie automatisierte Aufgaben auf einem ausgewählten Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3c46-105">The Task Scheduler service allows you to perform automated tasks on a chosen computer.</span></span> <span data-ttu-id="c3c46-106">Mit diesem Dienst können Sie ein beliebiges Programm so planen, dass es zu einem geeigneten Zeitpunkt ausgeführt wird oder wenn ein bestimmtes Ereignis eintritt.</span><span class="sxs-lookup"><span data-stu-id="c3c46-106">With this service, you can schedule any program to run at a convenient time for you or when a specific event occurs.</span></span> <span data-ttu-id="c3c46-107">Der Taskplaner überwacht die Zeit-oder Ereignis Kriterien, die Sie auswählen, und führt dann die Aufgabe aus, wenn diese Kriterien erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="c3c46-107">The Task Scheduler monitors the time or event criteria that you choose and then executes the task when those criteria are met.</span></span>

## <a name="where-task-scheduler-is-installed"></a><span data-ttu-id="c3c46-108">Installation von Taskplaner</span><span class="sxs-lookup"><span data-stu-id="c3c46-108">Where Task Scheduler is Installed</span></span>

<span data-ttu-id="c3c46-109">Der Taskplaner wird automatisch mit mehreren Microsoft-Betriebssystemen installiert.</span><span class="sxs-lookup"><span data-stu-id="c3c46-109">The Task Scheduler is automatically installed with several Microsoft operating systems.</span></span>

<span data-ttu-id="c3c46-110">Taskplaner 1,0 wird mit den Betriebssystemen Windows Server 2003, Windows XP und Windows 2000 installiert.</span><span class="sxs-lookup"><span data-stu-id="c3c46-110">Task Scheduler 1.0 is installed with the Windows Server 2003, Windows XP, and Windows 2000 operating systems.</span></span>

<span data-ttu-id="c3c46-111">Taskplaner 2,0 wird mit Windows Vista und Windows Server 2008 installiert.</span><span class="sxs-lookup"><span data-stu-id="c3c46-111">Task Scheduler 2.0 is installed with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="c3c46-112">Die Taskplaner 2,0-API sollte zum Entwickeln von Anwendungen verwendet werden, die den Taskplaner-Dienst unter Windows Vista verwenden.</span><span class="sxs-lookup"><span data-stu-id="c3c46-112">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="c3c46-113">Weitere Informationen finden Sie unter [Taskplaner Referenz](task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c3c46-113">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="c3c46-114">Taskplaner wird jedes Mal gestartet, wenn das Betriebssystem gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c3c46-114">Task Scheduler is started each time the operating system is started.</span></span> <span data-ttu-id="c3c46-115">Sie kann entweder über die grafische Benutzeroberfläche Taskplaner (GUI) oder über die in diesem SDK beschriebene Taskplaner-API ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c3c46-115">It can be run either through the Task Scheduler graphical user interface (GUI) or through the Task Scheduler API described in this SDK.</span></span>

## <a name="information-about-tasks"></a><span data-ttu-id="c3c46-116">Informationen zu Aufgaben</span><span class="sxs-lookup"><span data-stu-id="c3c46-116">Information about Tasks</span></span>

<span data-ttu-id="c3c46-117">Tasks sind die Hauptkomponente des Taskplaner.</span><span class="sxs-lookup"><span data-stu-id="c3c46-117">Tasks are the main component of the Task Scheduler.</span></span> <span data-ttu-id="c3c46-118">Informationen zu den Aufgaben und deren Komponenten finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c3c46-118">For information on what tasks are and what their components are, see the following topics:</span></span>

-   [<span data-ttu-id="c3c46-119">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="c3c46-119">Tasks</span></span>](tasks.md)
-   [<span data-ttu-id="c3c46-120">Task Aktionen</span><span class="sxs-lookup"><span data-stu-id="c3c46-120">Task Actions</span></span>](task-actions.md)
-   [<span data-ttu-id="c3c46-121">Task Trigger</span><span class="sxs-lookup"><span data-stu-id="c3c46-121">Task Triggers</span></span>](task-triggers.md)
-   [<span data-ttu-id="c3c46-122">Aufgaben Registrierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="c3c46-122">Task Registration Information</span></span>](task-registration-information.md)
-   [<span data-ttu-id="c3c46-123">Aufgaben im Leerlauf</span><span class="sxs-lookup"><span data-stu-id="c3c46-123">Task Idle Conditions</span></span>](task-idle-conditions.md)
-   [<span data-ttu-id="c3c46-124">Sicherheits Kontexte für Tasks</span><span class="sxs-lookup"><span data-stu-id="c3c46-124">Security Contexts for Tasks</span></span>](security-contexts-for-running-tasks.md)
-   [<span data-ttu-id="c3c46-125">Wiederholen einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="c3c46-125">Repeating A Task</span></span>](repeating-a-task.md)
-   [<span data-ttu-id="c3c46-126">Automatische Wartung</span><span class="sxs-lookup"><span data-stu-id="c3c46-126">Automatic Maintenance</span></span>](task-maintenence.md)

<span data-ttu-id="c3c46-127">Weitere Informationen und Beispiele zur Verwendung der Taskplaner Schnittstellen, Skript Objekte und XML finden [Sie unter Verwenden der Taskplaner](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="c3c46-127">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3c46-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c3c46-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3c46-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="c3c46-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




