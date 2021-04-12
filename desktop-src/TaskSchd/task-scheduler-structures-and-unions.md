---
title: Taskplaner Strukturen und Unions
description: Listet die Strukturen und Unions auf, die von den Taskplaner 1,0-APIs verwendet werden.
ms.assetid: 37dc7818-7719-4975-b7bd-f8c2d5cc008b
keywords:
- Taskplaner Taskplaner, Referenz, Strukturen und Unions
- Trigger Taskplaner, Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdb73620ccd92eed3ce8aea9bf5a17c5734d926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206372"
---
# <a name="task-scheduler-structures-and-unions"></a><span data-ttu-id="01b10-105">Taskplaner Strukturen und Unions</span><span class="sxs-lookup"><span data-stu-id="01b10-105">Task Scheduler Structures and Unions</span></span>

<span data-ttu-id="01b10-106">In diesem Abschnitt werden die Strukturen und Unions beschrieben, die von den Taskplaner-APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01b10-106">This section describes the structures and unions used by the Task Scheduler APIs.</span></span>

<span data-ttu-id="01b10-107">Alle unten aufgeführten Strukturen und Unions werden von Taskplaner 1,0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="01b10-107">All the structures and unions below are used by Task Scheduler 1.0.</span></span>



| <span data-ttu-id="01b10-108">Name</span><span class="sxs-lookup"><span data-stu-id="01b10-108">Name</span></span>                                               | <span data-ttu-id="01b10-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01b10-109">Description</span></span>                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01b10-110">**Tä**</span><span class="sxs-lookup"><span data-stu-id="01b10-110">**DAILY**</span></span>](/windows/desktop/api/Mstask/ns-mstask-daily)                             | <span data-ttu-id="01b10-111">Definiert das Intervall (in Tagen), in dem eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01b10-111">Defines the interval, in days, at which a task is run.</span></span>                                                                          |
| [<span data-ttu-id="01b10-112">**Monthlydate**</span><span class="sxs-lookup"><span data-stu-id="01b10-112">**MONTHLYDATE**</span></span>](/windows/desktop/api/Mstask/ns-mstask-monthlydate)                 | <span data-ttu-id="01b10-113">Definiert den Tag des Monats, an dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01b10-113">Defines the day of the month the task will run.</span></span>                                                                                 |
| [<span data-ttu-id="01b10-114">**Monthlydow**</span><span class="sxs-lookup"><span data-stu-id="01b10-114">**MONTHLYDOW**</span></span>](/windows/desktop/api/Mstask/ns-mstask-monthlydow)                   | <span data-ttu-id="01b10-115">Definiert das Datum (n), an dem der Task nach Monat, Woche und Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01b10-115">Defines the date(s) that the task runs by month, week, and day of the week.</span></span>                                                     |
| [<span data-ttu-id="01b10-116">**Task-Auslösung \_**</span><span class="sxs-lookup"><span data-stu-id="01b10-116">**TASK\_TRIGGER**</span></span>](/windows/desktop/api/Mstask/ns-mstask-task_trigger)              | <span data-ttu-id="01b10-117">Definiert die Zeiten für die Ausführung eines geplanten [*Arbeits Elements*](w.md).</span><span class="sxs-lookup"><span data-stu-id="01b10-117">Defines the times to run a scheduled [*work item*](w.md).</span></span>                                                  |
| [<span data-ttu-id="01b10-118">**\_auslösertyp \_ Union**</span><span class="sxs-lookup"><span data-stu-id="01b10-118">**TRIGGER\_TYPE\_UNION**</span></span>](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) | <span data-ttu-id="01b10-119">Definiert den Aufruf Zeitplan des Auslösers innerhalb des **Typmembers** einer [**Task \_ triggerstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="01b10-119">Defines the invocation schedule of the trigger within the **Type** member of a [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> |
| [<span data-ttu-id="01b10-120">**Arbei**</span><span class="sxs-lookup"><span data-stu-id="01b10-120">**WEEKLY**</span></span>](/windows/desktop/api/Mstask/ns-mstask-weekly)                           | <span data-ttu-id="01b10-121">Definiert das Intervall (in Wochen) zwischen den Aufrufen einer Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="01b10-121">Defines the interval, in weeks, between invocations of a task.</span></span>                                                                  |



 

 

 




