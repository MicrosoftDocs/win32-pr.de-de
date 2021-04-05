---
title: Auslöse Strukturen für Taskplaner 1,0
description: Taskplaner 1,0 verwendet mehrere Strukturen, um die Kriterien eines Auslösers zu definieren.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a03f28f85782d87ee3349582929babe6f907e8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037094"
---
# <a name="trigger-structures-for-task-scheduler-10"></a><span data-ttu-id="27ecb-103">Auslöse Strukturen für Taskplaner 1,0</span><span class="sxs-lookup"><span data-stu-id="27ecb-103">Trigger Structures for Task Scheduler 1.0</span></span>

<span data-ttu-id="27ecb-104">Taskplaner 1,0 verwendet mehrere Strukturen, um die Kriterien eines Auslösers zu definieren.</span><span class="sxs-lookup"><span data-stu-id="27ecb-104">Task Scheduler 1.0 uses several structures to define the criteria of a trigger.</span></span>

> [!Note]  
> <span data-ttu-id="27ecb-105">Weitere Informationen zu Taskplaner 2,0-Triggern finden Sie unter [triggerschnittstellen](trigger-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="27ecb-105">For more information about Task Scheduler 2.0 triggers, see [Trigger Interfaces](trigger-interfaces.md).</span></span>

 

## <a name="task-scheduler-10-structures"></a><span data-ttu-id="27ecb-106">Taskplaner 1,0-Strukturen</span><span class="sxs-lookup"><span data-stu-id="27ecb-106">Task Scheduler 1.0 Structures</span></span>

<span data-ttu-id="27ecb-107">In der folgenden Abbildung ist die Struktur des [**Task \_ Auslösers**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="27ecb-107">The following illustration shows the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="27ecb-108">Er verfügt über drei erforderliche Mitglieder (**wbeginyear**, **wbeginmonth** und **wbeginday**), die beim Erstellen eines neuen-Auslösers festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="27ecb-108">It has three required members (**wBeginYear**, **wBeginMonth**, and **wBeginDay**) that must be set when creating a new trigger.</span></span> <span data-ttu-id="27ecb-109">(Um zur Referenzseite für diese Struktur zu springen, klicken Sie in der Abbildung auf den Struktur Namen.)</span><span class="sxs-lookup"><span data-stu-id="27ecb-109">(To jump to the reference page for this structure, click the structure name in the illustration.)</span></span>

![Task auslöserstruktur](images/tsktri1.png)

<span data-ttu-id="27ecb-111">Beachten Sie, dass **der TriggerType** -Member die Enumeration des [**\_ tasktriggertyps \_**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) verwendet und der **Typmember** eine **Aufgaben \_ Trigger- \_ Union** -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="27ecb-111">Be aware that the **TriggerType** member uses the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the **Type** member uses a **TASK\_TRIGGER\_UNION** structure.</span></span> <span data-ttu-id="27ecb-112">Die Enumeration des **\_ taskauslösers \_** wird verwendet, um den Typ des Auslösers anzugeben (Ereignis-und zeitbasierte Auslösertypen).</span><span class="sxs-lookup"><span data-stu-id="27ecb-112">The **TASK\_TRIGGER\_TYPE** enumeration is used to specify the type of trigger (event and time-based trigger types).</span></span> <span data-ttu-id="27ecb-113">Die Union-Struktur des [**\_ triggertyps \_**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) wird verwendet, um die Strukturen [**täglich**](/windows/desktop/api/Mstask/ns-mstask-daily), [**wöchentlich**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**monthlydate**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (Tag of month) und [**monthlydow**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (Day of week) zu kombinieren, mit denen angegeben wird, wann ein zeitbasierter Trigger ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="27ecb-113">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used to combine the [**DAILY**](/windows/desktop/api/Mstask/ns-mstask-daily), [**WEEKLY**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (day of month), and [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (day of week) structures that are used to specify when a time-based trigger will fire.</span></span>

<span data-ttu-id="27ecb-114">Wenn **TriggerType** einen einmaligen zeitbasierten Trigger oder einen ereignisbasierten Trigger angibt, wird der **Typmember** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="27ecb-114">If **TriggerType** specifies a one-time time-based trigger or an event-based trigger, the **Type** member is ignored.</span></span> <span data-ttu-id="27ecb-115">Die Union-Struktur des [**\_ triggertyps \_**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) wird nur verwendet, wenn der **TriggerType** -Member einen Tages-, Wochen-, Monats-oder Monats Tags-zeitbasierten Trigger angibt.</span><span class="sxs-lookup"><span data-stu-id="27ecb-115">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used only if the **TriggerType** member specifies a daily, weekly, day-of-month, or monthly day-of-week time-based trigger.</span></span>

<span data-ttu-id="27ecb-116">Außerdem gibt die Einstellung des **Typmembers** an, welcher Member der [**\_ auslösertyp- \_ Union**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) -Struktur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27ecb-116">In addition, the setting of the **Type** member indicates which member of the [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used.</span></span> <span data-ttu-id="27ecb-117">In der folgenden Abbildung wird die Beziehung zwischen den Werten der [**\_ \_ Aufgabentyp**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) -Enumeration des Tasks und den Membern der **Struktur der \_ auslösertyp \_ Struktur** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="27ecb-117">The following illustration shows the relationship between the values of the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the members of the **TRIGGER\_TYPE\_STRUCTURE** structure.</span></span> <span data-ttu-id="27ecb-118">(Um zu den Referenzseiten für diese Strukturen zu springen, klicken Sie in der Abbildung auf den Struktur Namen.)</span><span class="sxs-lookup"><span data-stu-id="27ecb-118">(To jump to the reference pages for these structures click the structure name in the illustration.)</span></span>

![Beziehung zwischen den Enumerationswerten des Task Auslösers und Membern der auslösertyp-Struktur Struktur](images/tsktri3.png)

## <a name="related-topics"></a><span data-ttu-id="27ecb-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="27ecb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27ecb-121">Task Trigger</span><span class="sxs-lookup"><span data-stu-id="27ecb-121">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="27ecb-122">Auslösertypen</span><span class="sxs-lookup"><span data-stu-id="27ecb-122">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="27ecb-123">Auslöse Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="27ecb-123">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> </dl>

 

 




