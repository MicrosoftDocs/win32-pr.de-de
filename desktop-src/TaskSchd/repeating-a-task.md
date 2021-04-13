---
title: Wiederholen einer Aufgabe
description: Taskplaner können eine Aufgabe beliebig oft nach dem Auslösen eines Auslösers ausführen.
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- Wiederholungsmuster Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451b2c2cf7e48c40496ddba95728f435ab494ab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310655"
---
# <a name="repeating-a-task"></a><span data-ttu-id="a276c-104">Wiederholen einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a276c-104">Repeating A Task</span></span>

<span data-ttu-id="a276c-105">Taskplaner können eine Aufgabe beliebig oft nach dem Auslösen eines Auslösers ausführen.</span><span class="sxs-lookup"><span data-stu-id="a276c-105">Task Scheduler can run a task any number of times times after a trigger is fired.</span></span> <span data-ttu-id="a276c-106">Zu diesem Zweck definiert der-Vorgang ein Wiederholungsmuster, das angibt, Taskplaner wie lange die Aufgabe fortgesetzt werden soll, und das Zeitintervall zwischen den einzelnen Aufgaben Wiederholungen.</span><span class="sxs-lookup"><span data-stu-id="a276c-106">To do this, the trigger defines a repetition pattern that tells Task Scheduler how long it should continue to repeat the task and the time interval between each task repetition.</span></span>

## <a name="repetition-pattern"></a><span data-ttu-id="a276c-107">Wiederholungsmuster</span><span class="sxs-lookup"><span data-stu-id="a276c-107">Repetition Pattern</span></span>

<span data-ttu-id="a276c-108">Die folgende Abbildung zeigt ein Wiederholungsmuster mit einer Dauer von 60 Minuten und einem Intervall von 25 Minuten.</span><span class="sxs-lookup"><span data-stu-id="a276c-108">The following illustration shows a repetition pattern with a duration of 60 minutes and an interval of 25 minutes.</span></span> <span data-ttu-id="a276c-109">Beachten Sie, dass Taskplaner in diesem Fall die Aufgabe ausführt, wenn der Triggervorgang ausgelöst wird, die Aufgabe nach 25 Minuten erneut ausführt und dann die Aufgabe nach 50 Minuten erneut ausführt, abhängig von der Einstellung der [**stopatdurationend-Eigenschaft von irepetitionpattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**repetitionpattern. stopatdurationend**](repetitionpattern-stopatdurationend.md) für Scripting).</span><span class="sxs-lookup"><span data-stu-id="a276c-109">Be aware that in this case, Task Scheduler runs the task when the trigger is fired, it runs the task again after 25 minutes, then runs the task again after 50 minutes depending on the setting of the [**StopAtDurationEnd property of IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) for scripting).</span></span> <span data-ttu-id="a276c-110">Wenn die **stopatdurationend** -Eigenschaft auf true festgelegt ist, beendet Taskplaner die letzte Instanz der Aufgabe, wenn Sie noch nach 60 Minuten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a276c-110">If the **StopAtDurationEnd** property is set to True, Task Scheduler stops the last instance of the task if it is still running after 60 minutes.</span></span> <span data-ttu-id="a276c-111">Wenn die **stopatdurationend** -Eigenschaft auf false festgelegt ist, wird die letzte Instanz der Aufgabe unabhängig von der Dauer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a276c-111">If the **StopAtDurationEnd** property is set to False, the last instance of the task is run regardless of the duration.</span></span>

![Wiederholungsmuster für Wiederholung](images/repetition-pattern.png)

<span data-ttu-id="a276c-113">Wenn Sie eine Aufgabe registrieren, die einen-Auslösers mit einem Wiederholungsintervall von einer Minute und einer Wiederholungs Dauer von vier Minuten enthält, wird die Aufgabe fünfmal gestartet.</span><span class="sxs-lookup"><span data-stu-id="a276c-113">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started five times.</span></span> <span data-ttu-id="a276c-114">Die fünf Wiederholungen können mithilfe des folgenden Musters definiert werden:</span><span class="sxs-lookup"><span data-stu-id="a276c-114">The five repetitions can be defined by the following pattern:</span></span>

1.  <span data-ttu-id="a276c-115">Eine Aufgabe beginnt am Anfang der ersten Minute.</span><span class="sxs-lookup"><span data-stu-id="a276c-115">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="a276c-116">Die nächste Aufgabe beginnt am Ende der ersten Minute.</span><span class="sxs-lookup"><span data-stu-id="a276c-116">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="a276c-117">Die nächste Aufgabe beginnt am Ende der zweiten Minute.</span><span class="sxs-lookup"><span data-stu-id="a276c-117">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="a276c-118">Die nächste Aufgabe beginnt am Ende der dritten Minute.</span><span class="sxs-lookup"><span data-stu-id="a276c-118">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="a276c-119">Die nächste Aufgabe beginnt am Ende der vierten Minute.</span><span class="sxs-lookup"><span data-stu-id="a276c-119">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="a276c-120">**Windows Server 2003, Windows XP und Windows 2000:** Wenn Sie eine Aufgabe registrieren, die einen-Auslösers mit einem Wiederholungsintervall von einer Minute und einer Wiederholungs Dauer von vier Minuten enthält, wird die Aufgabe viermal gestartet.</span><span class="sxs-lookup"><span data-stu-id="a276c-120">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started four times.</span></span>

## <a name="objects-interfaces-and-xml-elements"></a><span data-ttu-id="a276c-121">Objekte, Schnittstellen und XML-Elemente</span><span class="sxs-lookup"><span data-stu-id="a276c-121">Objects, Interfaces, and XML Elements</span></span>

<span data-ttu-id="a276c-122">Bei der Skripterstellung wird das Wiederholungsmuster mithilfe des [**repetitionpattern**](repetitionpattern.md) -Objekts definiert.</span><span class="sxs-lookup"><span data-stu-id="a276c-122">For scripting development, the repetition pattern is defined using the [**RepetitionPattern**](repetitionpattern.md) object.</span></span>

<span data-ttu-id="a276c-123">Bei der C++-Entwicklung wird das Wiederholungsmuster durch die [**irepetitionpattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="a276c-123">For C++ development, the repetition pattern is defined by the [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) interface.</span></span>

<span data-ttu-id="a276c-124">Beim Lesen oder Schreiben von XML für eine Aufgabe wird das Wiederholungsmuster im [**Wiederholungs**](taskschedulerschema-repetition-triggerbasetype-element.md) Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="a276c-124">When reading or writing XML for a task, the repetition pattern is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a276c-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a276c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a276c-126">Task Trigger</span><span class="sxs-lookup"><span data-stu-id="a276c-126">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




