---
title: Taskplaner 1,0-Schnittstellen
description: Die in den folgenden Themen beschriebenen Schnittstellen ermöglichen den programmgesteuerten Zugriff auf die Funktionalität, die in der Taskplaner verfügbar ist, die in den Betriebssystemen Windows 2000, Windows XP und Windows Server 2003 verwendet wird.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bab12b59d4b4561ecbe46c09a76c69209574c9d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104213082"
---
# <a name="task-scheduler-10-interfaces"></a><span data-ttu-id="11b96-103">Taskplaner 1,0-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="11b96-103">Task Scheduler 1.0 Interfaces</span></span>

<span data-ttu-id="11b96-104">\[\[Diese API kann in nachfolgenden Versionen des Betriebssystems oder des Produkts geändert werden oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="11b96-104">\[\[This API may be altered or unavailable in subsequent versions of the operating system or product.</span></span> <span data-ttu-id="11b96-105">Verwenden Sie stattdessen die [Taskplaner 2,0-Schnittstellen](task-scheduler-2-0-interfaces.md) oder die [Taskplaner 2,0-Enumerationstypen](task-scheduler-2-0-enumerated-types.md) . \]\]</span><span class="sxs-lookup"><span data-stu-id="11b96-105">Please use the [Task Scheduler 2.0 Interfaces](task-scheduler-2-0-interfaces.md) or [Task Scheduler 2.0 Enumerated Types](task-scheduler-2-0-enumerated-types.md) instead.\] \]</span></span>

<span data-ttu-id="11b96-106">Die in den folgenden Themen beschriebenen Schnittstellen ermöglichen den programmgesteuerten Zugriff auf die Funktionalität, die in der Taskplaner verfügbar ist, die in den Betriebssystemen Windows 2000, Windows XP und Windows Server 2003 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="11b96-106">The interfaces that are described in the following topics provide programmatic access to the functionality that is available within the Task Scheduler that is used in the Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="11b96-107">Diese Themen enthalten eine Beschreibung der-Schnittstelle, eine Liste der Eigenschaften und Methoden, die von der-Schnittstelle definiert werden, sowie Hinweise zu allen besonderen Umständen, die bei der Verwendung der-Schnittstelle zu beachten sind.</span><span class="sxs-lookup"><span data-stu-id="11b96-107">These topics contain a description of the interface, a list of the properties and methods defined by the interface, and remarks about any special circumstances that should be noted when using the interface.</span></span>


<span data-ttu-id="11b96-108">Die folgenden Schnittstellen werden von Taskplaner 1,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="11b96-108">The following interfaces are introduced by Task Scheduler 1.0.</span></span>



| <span data-ttu-id="11b96-109">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="11b96-109">Interface</span></span>                                        | <span data-ttu-id="11b96-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11b96-110">Description</span></span>                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11b96-111">**Ienumworkitems**</span><span class="sxs-lookup"><span data-stu-id="11b96-111">**IEnumWorkItems**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | <span data-ttu-id="11b96-112">Stellt die Methoden zum Auflisten der Aufgaben im [*Ordner "geplante Aufgaben*](s.md)" bereit.</span><span class="sxs-lookup"><span data-stu-id="11b96-112">Provides the methods for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>                                                                                                              |
| [<span data-ttu-id="11b96-113">**Iprovidetaskpage**</span><span class="sxs-lookup"><span data-stu-id="11b96-113">**IProvideTaskPage**</span></span>](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | <span data-ttu-id="11b96-114">Stellt die Methoden für den Zugriff auf die Eigenschaften Blatt Einstellungen einer Aufgabe bereit.</span><span class="sxs-lookup"><span data-stu-id="11b96-114">Provides the methods to access the property sheet settings of a task.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="11b96-115">**Ischeduledworkitem**</span><span class="sxs-lookup"><span data-stu-id="11b96-115">**IScheduledWorkItem**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | <span data-ttu-id="11b96-116">Stellt die Methoden zum Verwalten bestimmter [*Arbeitsaufgaben*](w.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="11b96-116">Provides the methods for managing specific [*work items*](w.md).</span></span>                                                                                                                                                 |
| [<span data-ttu-id="11b96-117">**ITask**</span><span class="sxs-lookup"><span data-stu-id="11b96-117">**ITask**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itask)                           | <span data-ttu-id="11b96-118">Stellt die Methoden zum Ausführen von Aufgaben, zum erhalten oder Festlegen von Aufgabeninformationen und zum Beenden von Aufgaben bereit.</span><span class="sxs-lookup"><span data-stu-id="11b96-118">Provides the methods for running tasks, getting or setting task information, and terminating tasks.</span></span> <span data-ttu-id="11b96-119">Sie wird von der [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle abgeleitet und erbt alle Methoden dieser Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="11b96-119">It is derived from the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface and inherits all the methods of that interface.</span></span> |
| [<span data-ttu-id="11b96-120">**Itaskscheduler**</span><span class="sxs-lookup"><span data-stu-id="11b96-120">**ITaskScheduler**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | <span data-ttu-id="11b96-121">Stellt die Methoden zum Planen von Aufgaben bereit.</span><span class="sxs-lookup"><span data-stu-id="11b96-121">Provides the methods for scheduling tasks.</span></span>                                                                                                                                                                                            |
| [<span data-ttu-id="11b96-122">**Itaskauslöst**</span><span class="sxs-lookup"><span data-stu-id="11b96-122">**ITaskTrigger**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | <span data-ttu-id="11b96-123">Stellt die Methoden für den Zugriff auf und das Festlegen von Triggern für eine Aufgabe bereit.</span><span class="sxs-lookup"><span data-stu-id="11b96-123">Provides the methods for accessing and setting triggers for a task.</span></span> <span data-ttu-id="11b96-124">Trigger geben Task Startzeiten, Wiederholungs Kriterien und andere Parameter an, die Steuern, wann eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11b96-124">Triggers specify task start times, repetition criteria, and other parameters that control when a task is run.</span></span>                                                     |



 

 

 




