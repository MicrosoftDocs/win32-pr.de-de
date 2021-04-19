---
title: Leerlauf Trigger für Taskplaner 1,0
description: Ein im Leerlauf befindlich ausgelöster Triggertyp ist ein ereignisbasierter-Triggertyp, der nach dem Ausfall des Computers nach dem Leerlauf ausgelöst wird. Es gibt mehrere Bedingungen, die definieren, wann ein Computer in den Leerlauf wechselt, z. b. wenn keine Tastatur-oder Maus Eingaben auftritt.
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a19f3f6d474a9463667316e353a4803ab8fa9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342253"
---
# <a name="idle-triggers-for-task-scheduler-10"></a><span data-ttu-id="153cd-104">Leerlauf Trigger für Taskplaner 1,0</span><span class="sxs-lookup"><span data-stu-id="153cd-104">Idle Triggers for Task Scheduler 1.0</span></span>

<span data-ttu-id="153cd-105">Ein im Leerlauf befindlich ausgelöster Triggertyp ist ein ereignisbasierter-Triggertyp, der nach dem Ausfall des Computers nach dem Leerlauf ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="153cd-105">An idle trigger is an event-based trigger that is fired a specific number of times after the computer becomes idle.</span></span> <span data-ttu-id="153cd-106">Es gibt mehrere Bedingungen, die definieren, wann ein Computer in den Leerlauf wechselt, z. b. wenn keine Tastatur-oder Maus Eingaben auftritt.</span><span class="sxs-lookup"><span data-stu-id="153cd-106">There are multiple conditions that define when a computer becomes idle, such as when no keyboard or mouse input occurs.</span></span>

<span data-ttu-id="153cd-107">Leerlauf Trigger werden erstellt, indem ein \_ Task \_ Ereignis \_ Trigger \_ im Leerlauf im Member des [**\_ tasktriggertyps \_**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) der [**Task \_ triggerstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="153cd-107">Idle triggers are created by specifying TASK\_EVENT\_TRIGGER\_ON\_IDLE in the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="153cd-108">Der Leerlauf-Triggervorgang wird ausgelöst, wenn das System für den Zeitraum, der durch die Leerlauf Wartezeit der Arbeitsaufgabe angegeben wird, in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="153cd-108">The idle trigger is fired when the system becomes idle for the amount of time that is specified by the idle wait time of the work item.</span></span>

> [!Note]  
> <span data-ttu-id="153cd-109">Wenn ein Task Ereignis-Auslösung \_ \_ \_ im \_ Leerlauf angegeben wird, werden die **Member wstarthour**, **wstartminute** und Type der [**Task \_ auslöserstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) ignoriert. </span><span class="sxs-lookup"><span data-stu-id="153cd-109">When TASK\_EVENT\_TRIGGER\_ON\_IDLE is specified, the **wStartHour**, **wStartMinute**, and **Type** members of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure are ignored.</span></span>

 

<span data-ttu-id="153cd-110">Sie können die Leerlauf Wartezeit eines Arbeits Elements festlegen, indem Sie die [**ischeduledworkitem:: setidlewait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="153cd-110">You can set the idle wait time of a work item by calling the [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) method.</span></span> <span data-ttu-id="153cd-111">Mit dieser Methode wird die Zeitspanne (in Minuten) festgelegt, in der sich das System im Leerlauf befinden muss, bevor der-auslösen ausgelöst und die Arbeitsaufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="153cd-111">This method sets the amount of time (in minutes) that the system must remain idle before the trigger is fired and the work item is executed.</span></span>

<span data-ttu-id="153cd-112">Um die Leerlaufzeit einer Aufgabe abzurufen, rufen Sie die [**ischeduledworkitem:: getidlewait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="153cd-112">To retrieve the idle time of a task, call the [**IScheduledWorkItem::GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="153cd-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="153cd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="153cd-114">Task Trigger</span><span class="sxs-lookup"><span data-stu-id="153cd-114">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




