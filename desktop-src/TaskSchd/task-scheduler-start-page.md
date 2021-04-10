---
title: Taskplaner für Entwickler
description: Der Taskplaner ermöglicht Ihnen das automatische Ausführen von Routineaufgaben auf einem ausgewählten Computer. Taskplaner dies durch die Überwachung der von Ihnen gewählten Kriterien (als Trigger bezeichnet) und anschließendes Ausführen der Aufgaben, wenn diese Kriterien erfüllt sind.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- Taskplaner für Entwickler
- Taskplaner für die Entwicklung
- Entwickeln mit Taskplaner
- Taskplaner, Portalseite
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: dfbfb76145e38003e7c501b98c817f4aaca3ff09
ms.sourcegitcommit: 087843ef08ddcd8bce9ed647b610035925da2b3e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/19/2019
ms.locfileid: "104100826"
---
# <a name="task-scheduler-for-developers"></a><span data-ttu-id="c5be5-108">Taskplaner für Entwickler</span><span class="sxs-lookup"><span data-stu-id="c5be5-108">Task Scheduler for developers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5be5-109">Dieses Thema und die anderen Themen in diesem Abschnitt sind für eine Entwicklergruppe.</span><span class="sxs-lookup"><span data-stu-id="c5be5-109">This topic and the other topics in this section are for a developer audience.</span></span> <span data-ttu-id="c5be5-110">Wenn Sie die Taskplaner Komponente in ihrer Kapazität als Administrator oder als IT-Experte verwenden möchten, finden Sie weitere Informationen unter [Taskplaner](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).</span><span class="sxs-lookup"><span data-stu-id="c5be5-110">If you're wishing to use the the Task Scheduler component in your capacity as an administrator, or an IT Professional, then see [Task Scheduler](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).</span></span>

## <a name="about-the-task-scheduler"></a><span data-ttu-id="c5be5-111">Informationen zum Taskplaner</span><span class="sxs-lookup"><span data-stu-id="c5be5-111">About the Task Scheduler</span></span>

<span data-ttu-id="c5be5-112">Der Taskplaner ermöglicht Ihnen das automatische Ausführen von Routineaufgaben auf einem ausgewählten Computer.</span><span class="sxs-lookup"><span data-stu-id="c5be5-112">The Task Scheduler enables you to automatically perform routine tasks on a chosen computer.</span></span> <span data-ttu-id="c5be5-113">Taskplaner dies durch die Überwachung der von Ihnen gewählten Kriterien (als Trigger bezeichnet) und anschließendes Ausführen der Aufgaben, wenn diese Kriterien erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="c5be5-113">Task Scheduler does this by monitoring whatever criteria you choose (referred to as triggers) and then executing the tasks when those criteria are met.</span></span>

<span data-ttu-id="c5be5-114">Sie können den Taskplaner verwenden, um Aufgaben wie das Starten einer Anwendung, das Senden einer e-Mail-Nachricht oder das zeigen eines Meldungs Felds auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c5be5-114">You can use the Task Scheduler to execute tasks such as starting an application, sending an email message, or showing a message box.</span></span> <span data-ttu-id="c5be5-115">Aufgaben können so geplant werden, dass Sie als Reaktion auf diese Ereignisse oder Trigger ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c5be5-115">Tasks can be scheduled to execute in response to these events, or triggers.</span></span> 

- <span data-ttu-id="c5be5-116">Wenn ein bestimmtes System Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="c5be5-116">When a specific system event occurs.</span></span>
- <span data-ttu-id="c5be5-117">Zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="c5be5-117">At a specific time.</span></span>
- <span data-ttu-id="c5be5-118">Zu einem bestimmten Zeitpunkt nach einem täglichen Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="c5be5-118">At a specific time on a daily schedule.</span></span>
- <span data-ttu-id="c5be5-119">Zu einer bestimmten Zeit in einem wöchentlichen Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="c5be5-119">At a specific time on a weekly schedule.</span></span>
- <span data-ttu-id="c5be5-120">Zu einem bestimmten Zeitpunkt nach einem monatlichen Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="c5be5-120">At a specific time on a monthly schedule.</span></span>
- <span data-ttu-id="c5be5-121">Zu einem bestimmten Zeitpunkt an einem monatlichen Wochentag.</span><span class="sxs-lookup"><span data-stu-id="c5be5-121">At a specific time on a monthly day-of-week schedule.</span></span>
- <span data-ttu-id="c5be5-122">Wenn der Computer in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="c5be5-122">When the computer enters an idle state.</span></span>
- <span data-ttu-id="c5be5-123">Wenn die Aufgabe registriert ist.</span><span class="sxs-lookup"><span data-stu-id="c5be5-123">When the task is registered.</span></span>
- <span data-ttu-id="c5be5-124">Wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c5be5-124">When the system is booted.</span></span>
- <span data-ttu-id="c5be5-125">Wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="c5be5-125">When a user logs on.</span></span>
- <span data-ttu-id="c5be5-126">Wenn sich der Status einer Terminal Server Sitzung ändert.</span><span class="sxs-lookup"><span data-stu-id="c5be5-126">When a Terminal Server session changes state.</span></span>

## <a name="developers"></a><span data-ttu-id="c5be5-127">Entwickler</span><span class="sxs-lookup"><span data-stu-id="c5be5-127">Developers</span></span>

<span data-ttu-id="c5be5-128">Der Taskplaner stellt APIs in diesen Formularen bereit.</span><span class="sxs-lookup"><span data-stu-id="c5be5-128">The Task Scheduler provides APIs in these forms.</span></span>

- <span data-ttu-id="c5be5-129">Taskplaner 2,0: Schnittstellen und Objekte werden für C++ und für die Skript Entwicklung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c5be5-129">Task Scheduler 2.0: interfaces and objects are provided for C++, and for scripting development, respectively.</span></span>
- <span data-ttu-id="c5be5-130">Taskplaner 1,0: für die C++-Entwicklung werden Schnittstellen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c5be5-130">Task Scheduler 1.0: interfaces are provided for C++ development.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c5be5-131">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="c5be5-131">Run-time requirements</span></span>

<span data-ttu-id="c5be5-132">Der Taskplaner erfordert die folgenden Betriebssysteme:</span><span class="sxs-lookup"><span data-stu-id="c5be5-132">The Task Scheduler requires the following operating systems.</span></span>

- <span data-ttu-id="c5be5-133">Taskplaner 2,0: für den Client ist Windows Vista oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c5be5-133">Task Scheduler 2.0: Client requires Windows Vista, or above.</span></span> <span data-ttu-id="c5be5-134">Der Server erfordert Windows Server 2008 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c5be5-134">Server requires Windows Server 2008, or above.</span></span>
- <span data-ttu-id="c5be5-135">Taskplaner 1,0: der Client erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5be5-135">Task Scheduler 1.0: Client requires Windows Vista, or Windows XP.</span></span> <span data-ttu-id="c5be5-136">Der Server erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c5be5-136">Server requires Windows Server 2008, or Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c5be5-137">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c5be5-137">In this section</span></span>

| <span data-ttu-id="c5be5-138">Thema</span><span class="sxs-lookup"><span data-stu-id="c5be5-138">Topic</span></span> | <span data-ttu-id="c5be5-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5be5-139">Description</span></span> |
|-|-|
| [<span data-ttu-id="c5be5-140">Neues in Taskplaner</span><span class="sxs-lookup"><span data-stu-id="c5be5-140">What's new in Task Scheduler</span></span>](what-s-new-in-task-scheduler.md) | <span data-ttu-id="c5be5-141">Zusammenfassung der neuen Funktionen, die von der Taskplaner eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="c5be5-141">Summary of new functionality introduced by the Task Scheduler.</span></span> |
| [<span data-ttu-id="c5be5-142">Informationen zum Taskplaner</span><span class="sxs-lookup"><span data-stu-id="c5be5-142">About the Task Scheduler</span></span>](about-the-task-scheduler.md) | <span data-ttu-id="c5be5-143">Allgemeine konzeptionelle Informationen zur Taskplaner-API.</span><span class="sxs-lookup"><span data-stu-id="c5be5-143">General conceptual information about the Task Scheduler API.</span></span> |
| [<span data-ttu-id="c5be5-144">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="c5be5-144">Using the Task Scheduler</span></span>](using-the-task-scheduler.md) | <span data-ttu-id="c5be5-145">Code Beispiele, die zeigen, wie die Taskplaner-APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5be5-145">Code examples that show how to use the Task Scheduler APIs.</span></span> |
| [<span data-ttu-id="c5be5-146">Taskplaner Referenz</span><span class="sxs-lookup"><span data-stu-id="c5be5-146">Task Scheduler reference</span></span>](task-scheduler-reference.md) | <span data-ttu-id="c5be5-147">Ausführliche Referenzinformationen für Taskplaner-APIs und das Taskplaner-Schema.</span><span class="sxs-lookup"><span data-stu-id="c5be5-147">Detailed reference information for Task Scheduler APIs and the Task Scheduler schema.</span></span> |