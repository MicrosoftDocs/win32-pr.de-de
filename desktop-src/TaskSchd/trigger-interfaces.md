---
title: Auslöse Schnittstellen
description: Die APIs, die zum Verwalten von Triggern verwendet werden, variieren je nach Version der Taskplaner. In beiden Fällen können Sie mit diesen APIs jedoch neue Trigger erstellen, vorhandene Trigger abrufen und aktualisieren sowie nicht mehr benötigte Trigger löschen.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- Trigger Taskplaner, Schnittstellen
- Trigger Taskplaner, Schnittstellen, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5357bb745b43c51707d9571c7582a44c9225a7fe
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316815"
---
# <a name="trigger-interfaces"></a><span data-ttu-id="cb23b-106">Auslöse Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="cb23b-106">Trigger Interfaces</span></span>

<span data-ttu-id="cb23b-107">Die APIs, die zum Verwalten von Triggern verwendet werden, variieren je nach Version der Taskplaner.</span><span class="sxs-lookup"><span data-stu-id="cb23b-107">The APIs that are used to manage triggers vary depending on the version of the Task Scheduler.</span></span> <span data-ttu-id="cb23b-108">In beiden Fällen können Sie mit diesen APIs jedoch neue Trigger erstellen, vorhandene Trigger abrufen und aktualisieren sowie nicht mehr benötigte Trigger löschen.</span><span class="sxs-lookup"><span data-stu-id="cb23b-108">However, in both cases these APIs enable you to create new triggers, retrieve and update existing triggers, and delete triggers that are no longer required.</span></span>


<span data-ttu-id="cb23b-109">Anwendungen, die mit Taskplaner 2,0 entwickelt wurden, können-Objekte und-Schnittstellen verwenden, um die Trigger für eine Aufgabe zu erstellen, abzurufen, zu ändern und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="cb23b-109">Applications that are developed using Task Scheduler 2.0 can use objects and interfaces to create, retrieve, modify, and delete the triggers for a task.</span></span>

<span data-ttu-id="cb23b-110">In der folgenden Abbildung gibt eine Aufgabe eine Auflistung von Triggern mithilfe der Triggers-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="cb23b-110">In the following illustration, a task specifies a collection of triggers using its Triggers property.</span></span> <span data-ttu-id="cb23b-111">Diese Sammlung enthält eine oder mehrere individuelle auslöserapis, wobei jede API einen bestimmten auslösertyp angibt.</span><span class="sxs-lookup"><span data-stu-id="cb23b-111">This collection contains one or more individual trigger APIs with each API specifying a specific trigger type.</span></span> <span data-ttu-id="cb23b-112">Beispielsweise enthält die Auflistung in der Abbildung unten einen Start-und einen LOGON-und einen täglichen-Auslösers.</span><span class="sxs-lookup"><span data-stu-id="cb23b-112">For example, in the illustration below the trigger collection contains a boot trigger, logon trigger, and a daily trigger.</span></span>

![Taskplaner 2,0-Auslöse Schnittstellen](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a><span data-ttu-id="cb23b-114">Objekt-APIs für die Skript Entwicklung</span><span class="sxs-lookup"><span data-stu-id="cb23b-114">Object APIs for Scripting Development</span></span>

<span data-ttu-id="cb23b-115">Weitere Informationen zu den Methoden und Eigenschaften der Objekte, die zum Angeben von Triggern verwendet werden, finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="cb23b-115">For more information about the methods and properties of the objects that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="cb23b-116">**Task Definition**</span><span class="sxs-lookup"><span data-stu-id="cb23b-116">**TaskDefinition**</span></span>](taskdefinition.md)
-   [<span data-ttu-id="cb23b-117">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="cb23b-117">**TriggerCollection**</span></span>](triggercollection.md)
-   [<span data-ttu-id="cb23b-118">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="cb23b-118">**Trigger**</span></span>](trigger.md)
-   [<span data-ttu-id="cb23b-119">**Boottrigger**</span><span class="sxs-lookup"><span data-stu-id="cb23b-119">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="cb23b-120">**Dailylöst**</span><span class="sxs-lookup"><span data-stu-id="cb23b-120">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="cb23b-121">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="cb23b-121">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="cb23b-122">**Idle-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="cb23b-122">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="cb23b-123">**Logonauslöst**</span><span class="sxs-lookup"><span data-stu-id="cb23b-123">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="cb23b-124">**Monthlydowlöst**</span><span class="sxs-lookup"><span data-stu-id="cb23b-124">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="cb23b-125">**Monthly-auslöst**</span><span class="sxs-lookup"><span data-stu-id="cb23b-125">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="cb23b-126">**Registration-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="cb23b-126">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="cb23b-127">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="cb23b-127">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="cb23b-128">**Weeklyauslösers**</span><span class="sxs-lookup"><span data-stu-id="cb23b-128">**WeeklyTrigger**</span></span>](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a><span data-ttu-id="cb23b-129">Schnittstellen-APIs für die C++-Entwicklung</span><span class="sxs-lookup"><span data-stu-id="cb23b-129">Interfaces APIs for C++ Development</span></span>

<span data-ttu-id="cb23b-130">Weitere Informationen zu den Methoden und Eigenschaften der Schnittstellen, die zum Angeben von Triggern verwendet werden, finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="cb23b-130">For more information about the methods and properties of the interfaces that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="cb23b-131">**Itaskdefinition**</span><span class="sxs-lookup"><span data-stu-id="cb23b-131">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [<span data-ttu-id="cb23b-132">**ITriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="cb23b-132">**ITriggerCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [<span data-ttu-id="cb23b-133">**I-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="cb23b-133">**ITrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [<span data-ttu-id="cb23b-134">**Iboottrigger**</span><span class="sxs-lookup"><span data-stu-id="cb23b-134">**IBootTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [<span data-ttu-id="cb23b-135">**Idaily-Fehler**</span><span class="sxs-lookup"><span data-stu-id="cb23b-135">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="cb23b-136">**Ieventvent**</span><span class="sxs-lookup"><span data-stu-id="cb23b-136">**IEventTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [<span data-ttu-id="cb23b-137">**Iidle-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="cb23b-137">**IIdleTrigger**</span></span>](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [<span data-ttu-id="cb23b-138">**ILogon-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="cb23b-138">**ILogonTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [<span data-ttu-id="cb23b-139">**Imonthlydowlöst**</span><span class="sxs-lookup"><span data-stu-id="cb23b-139">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [<span data-ttu-id="cb23b-140">**Imonthly-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="cb23b-140">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="cb23b-141">**Iregistration-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="cb23b-141">**IRegistrationTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [<span data-ttu-id="cb23b-142">**Itimelöst**</span><span class="sxs-lookup"><span data-stu-id="cb23b-142">**ITimeTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [<span data-ttu-id="cb23b-143">**Iweeklylöst**</span><span class="sxs-lookup"><span data-stu-id="cb23b-143">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a><span data-ttu-id="cb23b-144">Taskplaner 1,0-auslöserschnittstellen</span><span class="sxs-lookup"><span data-stu-id="cb23b-144">Task Scheduler 1.0 Trigger Interfaces</span></span>

<span data-ttu-id="cb23b-145">Vorhandene Anwendungen, die mit Taskplaner 1,0 entwickelt wurden, können die Methoden verwenden, die über die Taskplaner 1,0-Schnittstellen verfügbar sind, um die Trigger für ein [*Arbeits Element*](w.md)zu erstellen, abzurufen, zu ändern und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="cb23b-145">Existing applications that are developed using Task Scheduler 1.0 can use the methods that are available from the Task Scheduler 1.0 interfaces to create, retrieve, modify, and delete the triggers for a [*work item*](w.md).</span></span> <span data-ttu-id="cb23b-146">Beachten Sie jedoch, dass alle Taskplaner 1,0-Schnittstellen, Enumerationen und Strukturen veraltet sind und nicht für die Entwicklung neuer Anwendungen verwendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="cb23b-146">However, note that all Task Scheduler 1.0 interfaces, enumerations, and structures are obsolete and should not be used for the development of new applications.</span></span>

<span data-ttu-id="cb23b-147">Die beiden Schnittstellen, die dazu verwendet werden, sind in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cb23b-147">The two interfaces that are used to do this are shown in the following illustration.</span></span> <span data-ttu-id="cb23b-148">Die [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle wird zum Verwalten aller Trigger verwendet, die mit einer Arbeitsaufgabe verknüpft sind (diese Verwaltung umfasst das Erstellen eines neuen Triggers für das Arbeits Element).</span><span class="sxs-lookup"><span data-stu-id="cb23b-148">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface is used to manage all the triggers that are associated with a work item (such management includes creating a new trigger for the work item).</span></span> <span data-ttu-id="cb23b-149">Die [**itaskauslöserschnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) wird zum Verwalten eines bestimmten Auslösers verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb23b-149">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface is used to manage a specific trigger.</span></span>

![Taskplaner 1,0-Auslöse Schnittstellen](images/tsktri2.png)

<span data-ttu-id="cb23b-151">Die [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle stellt Methoden zum Erstellen eines neuen Triggers für ein Arbeits Element, zum Abrufen der Anzahl von Triggern, die einer Arbeitsaufgabe zugeordnet sind, zum Abrufen der [*triggerstrukturen*](t.md) , die dem Arbeits Element zugeordnet sind, zum Abrufen der [*triggerzeichenfolgen*](t.md) , die der Arbeitsaufgabe zugeordnet sind, sowie zum Löschen von Triggern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="cb23b-151">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for creating a new trigger for a work item, retrieving the number of triggers that are associated with a work item, retrieving the [*trigger structures*](t.md) that are associated with the work item, retrieving [*trigger strings*](t.md) that are associated with the work item, and for deleting triggers.</span></span>

<span data-ttu-id="cb23b-152">Sobald das Triggerobjekt verfügbar ist, können Sie die [**itasktrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) -Schnittstelle verwenden, um die triggerstruktur und die Zeichenfolge des Auslösers abzurufen und die Kriterien festzulegen, mit denen der Trigger ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="cb23b-152">Once the trigger object is available, you can use the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger structure and the string of the trigger and to set the criteria that is used to fire the trigger.</span></span> <span data-ttu-id="cb23b-153">Diese Schnittstelle wird nur verwendet, wenn Sie mit einem [*taskauslöserobjekt*](t.md)arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cb23b-153">This interface is used only when you are working with a [*task trigger object*](t.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb23b-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cb23b-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb23b-155">Task Trigger</span><span class="sxs-lookup"><span data-stu-id="cb23b-155">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="cb23b-156">Auslösertypen</span><span class="sxs-lookup"><span data-stu-id="cb23b-156">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="cb23b-157">Auslöserstrukturen</span><span class="sxs-lookup"><span data-stu-id="cb23b-157">Trigger Structures</span></span>](trigger-structures.md)
</dt> </dl>

 

 