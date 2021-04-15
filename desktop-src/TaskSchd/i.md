---
title: I (Taskplaner)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8492f707a171c6811b4702d2a07de47d29482a8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517258"
---
# <a name="i-task-scheduler"></a><span data-ttu-id="16d24-103">I (Taskplaner)</span><span class="sxs-lookup"><span data-stu-id="16d24-103">I (Task Scheduler)</span></span>

<span data-ttu-id="16d24-104">a B C D [E](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="16d24-104">A B C D [E](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="16d24-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**Leerlauf Bedingungen**</span><span class="sxs-lookup"><span data-stu-id="16d24-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**idle conditions**</span></span>
</dt> <dd>

<span data-ttu-id="16d24-106">Ein Zeitraum, in dem keine Benutzereingabe auf dem Computer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="16d24-106">A period of time in which there is no user input on the computer.</span></span> <span data-ttu-id="16d24-107">Leerlauf Bedingungen werden der geplanten Startzeit für den Task zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="16d24-107">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="16d24-108">Diese Bedingungen werden durch Aufrufen von [**ischeduledworkitem:: setFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16d24-108">These conditions are set by calling [**IScheduledWorkItem::SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).</span></span>

</dd> <dt>

<span data-ttu-id="16d24-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**Leerlauf Trigger**</span><span class="sxs-lookup"><span data-stu-id="16d24-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**idle triggers**</span></span>
</dt> <dd>

<span data-ttu-id="16d24-110">Ein ereignisbasierter-Triggertyp, der ausgelöst wird, wenn sich der Computer für einen bestimmten Zeitraum im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="16d24-110">An event-based trigger that is fired when the computer becomes idle for a specific amount of time.</span></span>

<span data-ttu-id="16d24-111">Leerlauf Trigger werden erstellt, indem der \_ tasktriggertypmember \_ der [**Task \_ triggerstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) auf Task \_ Ereignis \_ Trigger \_ im \_ Leerlauf festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="16d24-111">Idle triggers are created by setting the TASK\_TRIGGER\_TYPE member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure to TASK\_EVENT\_TRIGGER\_ON\_IDLE.</span></span>

</dd> <dt>

<span data-ttu-id="16d24-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**Wartezeit im Leerlauf**</span><span class="sxs-lookup"><span data-stu-id="16d24-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**idle wait time**</span></span>
</dt> <dd>

<span data-ttu-id="16d24-113">Das Zeitintervall (in Minuten), das von einem Leerlauf-oder Leerlaufzustand verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16d24-113">The time interval (in minutes) used by an idle trigger or idle condition.</span></span> <span data-ttu-id="16d24-114">Im Leerlauf befindliche Trigger sind ereignisbasierte Trigger, die keiner geplanten Zeit zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="16d24-114">Idle triggers are event-based triggers that are not associated with a scheduled time.</span></span> <span data-ttu-id="16d24-115">Leerlauf Bedingungen werden der geplanten Startzeit für den Task zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="16d24-115">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="16d24-116">Die Leerlaufzeit wird durch einen Aufruf von [**ischeduledworkitem:: setidlewait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16d24-116">The idle time is set by a call to [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).</span></span>

</dd> </dl>

 

 




