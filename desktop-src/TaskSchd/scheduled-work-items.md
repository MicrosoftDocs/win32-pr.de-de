---
title: Geplante Arbeitselemente
description: In der Taskplaner werden zwei Begriffe verwendet, um zu beschreiben, wie Arbeitsaufgaben und Aufgaben geplant werden können.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- Arbeitselemente Taskplaner
- Arbeitsaufgaben Taskplaner im Vergleich zu Aufgaben
- Aufgaben Taskplaner
- Aufgaben Taskplaner im Vergleich zu Arbeits Elementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586747e4049529dcfe747959aae994360a7b1485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309704"
---
# <a name="scheduled-work-items"></a><span data-ttu-id="ce612-107">Geplante Arbeitselemente</span><span class="sxs-lookup"><span data-stu-id="ce612-107">Scheduled Work Items</span></span>

<span data-ttu-id="ce612-108">Der Taskplaner verwendet zwei Begriffe, um zu beschreiben, was er planen kann: Arbeitsaufgaben und Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="ce612-108">The Task Scheduler uses two terms to describe what it can schedule: work items and tasks.</span></span> <span data-ttu-id="ce612-109">In diesen beiden Begriffen ist das [*Arbeits Element*](w.md) ein allgemeinerer Begriff, der jeden Typ von Element beschreibt, der geplant werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce612-109">Of these two terms, [*work item*](w.md) is a more general term that describes any type of item that can be scheduled.</span></span> <span data-ttu-id="ce612-110">Bei einem *Arbeits Element* kann es sich um ein beliebiges Element handeln, das der Taskplaner-Dienst zu einem bestimmten Zeitpunkt ausführt, der durch die Elemente des-Elements angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ce612-110">A *work item* can be any item that the Task Scheduler service runs at a time that is specified by the item's trigger(s).</span></span>

<span data-ttu-id="ce612-111">Im Gegensatz dazu ist eine [*Aufgabe*](t.md) ein bestimmter Typ von Arbeits Element.</span><span class="sxs-lookup"><span data-stu-id="ce612-111">In contrast, a [*task*](t.md) is a specific type of work item.</span></span> <span data-ttu-id="ce612-112">Derzeit ist die einzige Art von geplanter Arbeitsaufgabe, die unterstützt wird, eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="ce612-112">Currently, the only type of scheduled work item that is supported is a task.</span></span>

<span data-ttu-id="ce612-113">Die [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle enthält Methoden, die von allen Typen geplanter Arbeitselemente unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ce612-113">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface contains methods that are supported by all types of scheduled work items.</span></span> <span data-ttu-id="ce612-114">Kontoinformationen, Laufzeiten und Anwendungs definierte Kommentare sind z. b. Eigenschaften, die für alle Typen von Arbeits Elementen gelten können.</span><span class="sxs-lookup"><span data-stu-id="ce612-114">For example, account information, run times, and application-defined comments are properties that may apply to all types of work items.</span></span> <span data-ttu-id="ce612-115">Diese Eigenschaften können über die **ischeduledworkitem** -Schnittstelle festgelegt und abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ce612-115">These properties can be set and retrieved through the **IScheduledWorkItem** interface.</span></span>

<span data-ttu-id="ce612-116">Die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle enthält Methoden, die nur von Tasks unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ce612-116">The [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface contains methods that are supported only by tasks.</span></span>

<span data-ttu-id="ce612-117">Die Methoden der [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle werden zurzeit von der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle geerbt und in der Zukunft von anderen Arbeits Element Schnittstellen geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce612-117">The methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface are currently inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface and in the future will be inherited by other work item interfaces.</span></span>

| <span data-ttu-id="ce612-118">Beispiele für</span><span class="sxs-lookup"><span data-stu-id="ce612-118">For examples of</span></span>                                              | <span data-ttu-id="ce612-119">Siehe</span><span class="sxs-lookup"><span data-stu-id="ce612-119">See</span></span>                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce612-120">Erstellen einer neuen Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="ce612-120">Creating a new task.</span></span>                                         | [<span data-ttu-id="ce612-121">Erstellen einer Aufgabe mit NewWorkItem-Beispiel</span><span class="sxs-lookup"><span data-stu-id="ce612-121">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |
| <span data-ttu-id="ce612-122">Ausführen einer vorhandenen Aufgabe</span><span class="sxs-lookup"><span data-stu-id="ce612-122">Running an existing task.</span></span>                                    | [<span data-ttu-id="ce612-123">Beispiel für das Starten einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="ce612-123">Starting a Task Example</span></span>](starting-a-task-example.md)                                     |
| <span data-ttu-id="ce612-124">Abrufen von Eigenschaften, die für alle Typen von Arbeitsaufgaben gelten.</span><span class="sxs-lookup"><span data-stu-id="ce612-124">Retrieving properties that apply to all types of work items.</span></span> | [<span data-ttu-id="ce612-125">Abrufen von Beispielen für Arbeits Element Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce612-125">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="ce612-126">Festlegen von Eigenschaften, die für alle Arbeits Elementtypen gelten.</span><span class="sxs-lookup"><span data-stu-id="ce612-126">Setting properties that apply to all types of work items.</span></span>    | [<span data-ttu-id="ce612-127">Festlegen von Beispielen für Arbeits Element Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce612-127">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |



 

 

 




