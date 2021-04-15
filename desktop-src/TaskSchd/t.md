---
title: T (Taskplaner)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517282"
---
# <a name="t-task-scheduler"></a><span data-ttu-id="ee3e3-103">T (Taskplaner)</span><span class="sxs-lookup"><span data-stu-id="ee3e3-103">T (Task Scheduler)</span></span>

<span data-ttu-id="ee3e3-104">a B C D [E](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="ee3e3-104">A B C D [E](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="ee3e3-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**Task Objekte**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**task objects**</span></span>
</dt> <dd>

<span data-ttu-id="ee3e3-106">Instanzen eines Objekts, das Methoden zum Verwalten von Aufgaben bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-106">Instances of an object that provides methods for managing tasks.</span></span> <span data-ttu-id="ee3e3-107">Dies schließt Methoden zum Festlegen und Abrufen von Eigenschaften ein. ausführen, beenden und Löschen von Aufgaben; und das Erstellen neuer Trigger und das Abrufen von alten Triggern.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-107">This includes methods for setting and retrieving properties; running, terminating, and deleting tasks; and creating new triggers and retrieving old triggers.</span></span>

<span data-ttu-id="ee3e3-108">Das Task-Objekt wird durch Aufrufe von [**ischeduledworkitem::**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) up-und [**ischeduledworkitem:: gettrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger)erstellt.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-108">The task object is created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

</dd> <dt>

<span data-ttu-id="ee3e3-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**Aufgabenplaner-Objekte**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**task scheduler objects**</span></span>
</dt> <dd>

<span data-ttu-id="ee3e3-110">Instanzen eines Objekts, das den Taskplaner Dienstanbieter darstellt.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-110">Instances of an object the represents the Task Scheduler service.</span></span> <span data-ttu-id="ee3e3-111">Dieses Objekt unterstützt zwei Schnittstellen: **IUnknown** und [**itaskscheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (zurzeit sind Tasks die einzigen Typen von Arbeits Elementen, die vom Taskplaner-Dienst unterstützt werden).</span><span class="sxs-lookup"><span data-stu-id="ee3e3-111">This object supports two interfaces: **IUnknown** and [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (currently tasks are the only type of work items supported by the Task Scheduler service).</span></span>

<span data-ttu-id="ee3e3-112">Aufgabenplaner-Objekte werden durch Aufrufe von **cokreatanstance** erstellt.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-112">Task scheduler objects are created by calls to **CoCreateInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="ee3e3-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**Aufgaben auslösende Objekte**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**task trigger objects**</span></span>
</dt> <dd>

<span data-ttu-id="ee3e3-114">Instanzen eines Objekts stellt Methoden zum Festlegen und Abrufen von Task Triggern bereit.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-114">Instances of an object the provides methods for setting and retrieving task triggers.</span></span> <span data-ttu-id="ee3e3-115">Dieses Objekt unterstützt zwei Schnittstellen: **IUnknown** und [**itaskauslöst**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).</span><span class="sxs-lookup"><span data-stu-id="ee3e3-115">This object supports two interfaces: **IUnknown** and [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).</span></span>

<span data-ttu-id="ee3e3-116">Taskauslöserobjekte werden durch Aufrufe von [**ischeduledworkitem::**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) up-und [**ischeduledworkitem:: gettrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger)erstellt.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-116">Task trigger objects are created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

<span data-ttu-id="ee3e3-117">Siehe auch: *Trigger*.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-117">See also: *triggers*.</span></span>

</dd> <dt>

<span data-ttu-id="ee3e3-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**erfüllen**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**tasks**</span></span>
</dt> <dd>

<span data-ttu-id="ee3e3-119">Ein beliebiges Element, das vom Taskplaner ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-119">Any item that the Task Scheduler can execute.</span></span> <span data-ttu-id="ee3e3-120">Diese Elemente können Folgendes enthalten (wie von dem Betriebssystem unterstützt, auf dem der Task ausgeführt wird): Win32-® Anwendungen, Win16-Anwendungen, OS/2-Anwendungen, MS-DOS® Anwendungen, Batch Dateien ( \* bat), Befehls Dateien ( \* . cmd) oder ein beliebiger ordnungsgemäß registrierter Dateityp.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-120">These items may include any of the following (as supported by the operating system on which the task will execute): Win32® applications, Win16 applications, OS/2 applications, MS-DOS® applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

</dd> <dt>

<span data-ttu-id="ee3e3-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Ordner "Tasks"**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Tasks folder**</span></span>
</dt> <dd>

<span data-ttu-id="ee3e3-122">Der Ordner, in dem alle Aufgaben Dateien aufgelistet werden (zurzeit sind Aufgaben die einzigen verfügbaren Arbeitselemente).</span><span class="sxs-lookup"><span data-stu-id="ee3e3-122">The folder that lists all task files (currently, tasks are the only work items available).</span></span> <span data-ttu-id="ee3e3-123">Diese Dateien enthalten die Informationen über den Task.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-123">These files contain the information about the task.</span></span> <span data-ttu-id="ee3e3-124">Der Name dieser Dateien gibt den Namen der Aufgabe wieder.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-124">The name of these files reflects the name of the task.</span></span>

<span data-ttu-id="ee3e3-125">Sie können den Speicherort des Ordners "Tasks" aus der Registrierung abrufen, indem Sie die Daten für den folgenden Wert abrufen:</span><span class="sxs-lookup"><span data-stu-id="ee3e3-125">You can retrieve the location of the Tasks folder from the registry by getting data for the following value:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span data-ttu-id="ee3e3-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**auslöst**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**triggers**</span></span>
</dt> <dd>

<span data-ttu-id="ee3e3-127">Eine Reihe von Kriterien, die die Ausführung einer Aufgabe bewirken, wenn diese erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-127">A set of criteria that, when met, will cause a task to be executed.</span></span> <span data-ttu-id="ee3e3-128">Taskplaner stellt zeitbasierte und ereignisbasierte Trigger bereit, die Task Startzeiten, Wiederholungs Kriterien und andere Parameter angeben können.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-128">Task Scheduler provides time-based and event-based triggers that can specify task start times, repetition criteria, and other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="ee3e3-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**Auslöse Zeichen folgen**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**trigger strings**</span></span>
</dt> <dd>

<span data-ttu-id="ee3e3-130">Eine Zeichenfolge, die den-Auslösers beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-130">A string that describes the trigger.</span></span> <span data-ttu-id="ee3e3-131">Diese Zeichenfolge wird vom Taskplaner-Dienst erstellt und in der Taskplaner-Benutzeroberfläche in einem Format angezeigt, das "täglich um 14 Uhr, beginnend 5/11/97" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-131">This string is created by the Task Scheduler service, and appears in the Task Scheduler user interface in a form similar to "At 2PM every day, starting 5/11/97."</span></span>

</dd> <dt>

<span data-ttu-id="ee3e3-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**auslöserstrukturen**</span><span class="sxs-lookup"><span data-stu-id="ee3e3-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**trigger structures**</span></span>
</dt> <dd>

<span data-ttu-id="ee3e3-133">Die [**\_ taskauslöserstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) , die verwendet wird, wenn die Kriterien festgelegt oder abgerufen werden, durch die der-</span><span class="sxs-lookup"><span data-stu-id="ee3e3-133">The [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure used when setting or retrieving the criteria that defines the trigger.</span></span> <span data-ttu-id="ee3e3-134">Die Kriterien umfassen, wann der Trigger ausgelöst wird, und den Typ des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="ee3e3-134">The criteria includes when the trigger will fire, and the type of the trigger.</span></span>

</dd> </dl>

 

 




