---
title: Enumerationstypen Taskplaner
description: Listet die von den Taskplaner-APIs verwendeten Enumerationen auf.
ms.assetid: 9779d32b-0142-41bb-88e2-df79a3b0c1b2
keywords:
- Taskplaner Taskplaner, Verweis, enumerierte Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a70c4a939d176516d47f6af8bc0825b414bf1de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104517228"
---
# <a name="task-scheduler-enumerated-types"></a><span data-ttu-id="5c85f-104">Enumerationstypen Taskplaner</span><span class="sxs-lookup"><span data-stu-id="5c85f-104">Task Scheduler Enumerated Types</span></span>

<span data-ttu-id="5c85f-105">Beschreibt die Enumerationstypen, die die Konstanten definieren, die von den Taskplaner-APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c85f-105">Describes the enumerated types that define the constants that are used by the Task Scheduler APIs.</span></span>


<span data-ttu-id="5c85f-106">Die folgenden Enumerationstypen werden in Taskplaner 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5c85f-106">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="5c85f-107">Enumeration</span><span class="sxs-lookup"><span data-stu-id="5c85f-107">Enumeration</span></span>                                                                  | <span data-ttu-id="5c85f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c85f-108">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c85f-109">**Task \_ \_ Aktionstyp**</span><span class="sxs-lookup"><span data-stu-id="5c85f-109">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="5c85f-110">Definiert die Art von Aktionen, die von einer Aufgabe durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="5c85f-110">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="5c85f-111">**Aufgaben \_ Kompatibilität**</span><span class="sxs-lookup"><span data-stu-id="5c85f-111">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="5c85f-112">Definiert, welche Versionen von Taskplaner oder den at-Befehl, mit dem die Aufgabe kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="5c85f-112">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="5c85f-113">**Task \_ Erstellung**</span><span class="sxs-lookup"><span data-stu-id="5c85f-113">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="5c85f-114">Definiert, wie der Taskplaner-Dienst die Aufgabe erstellt, aktualisiert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5c85f-114">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="5c85f-115">**\_taskaufgabenflags \_**</span><span class="sxs-lookup"><span data-stu-id="5c85f-115">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="5c85f-116">Definiert, wie die Taskplaner durch registrierte Tasks aufzählt.</span><span class="sxs-lookup"><span data-stu-id="5c85f-116">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="5c85f-117">**Task \_ Instanzen \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="5c85f-117">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="5c85f-118">Definiert, wie die Taskplaner vorhandene Instanzen der Aufgabe behandelt, wenn eine neue Instanz der Aufgabe gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5c85f-118">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="5c85f-119">**Task \_ Anmeldetyp**</span><span class="sxs-lookup"><span data-stu-id="5c85f-119">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="5c85f-120">Definiert, welche Anmelde Methode zum Ausführen einer Aufgabe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5c85f-120">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="5c85f-121">**Task \_ processtokensid-Typ**</span><span class="sxs-lookup"><span data-stu-id="5c85f-121">**TASK\_PROCESSTOKENSID TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)              | <span data-ttu-id="5c85f-122">Definiert die Typen der Prozess-sid, die von Tasks verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5c85f-122">Defines the types of process SID that can used by tasks.</span></span>                                                         |
| [<span data-ttu-id="5c85f-123">**\_ \_ tasktestflags**</span><span class="sxs-lookup"><span data-stu-id="5c85f-123">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="5c85f-124">Definiert, wie eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c85f-124">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="5c85f-125">**\_taskrunlevel- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="5c85f-125">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="5c85f-126">Definiert Lua-Erweiterungs Flags, die angeben, welche Berechtigungsebene für die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c85f-126">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="5c85f-127">**\_ \_ Status \_ \_ Änderungstyp für Task Sitzung**</span><span class="sxs-lookup"><span data-stu-id="5c85f-127">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="5c85f-128">Definiert, welche Arten von Terminal Server-Sitzungs Statusänderungen Sie verwenden können, um einen Task zu starten.</span><span class="sxs-lookup"><span data-stu-id="5c85f-128">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="5c85f-129">**Task \_ Status**</span><span class="sxs-lookup"><span data-stu-id="5c85f-129">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="5c85f-130">Definiert die verschiedenen Zustände, in denen sich eine registrierte Aufgabe befinden kann.</span><span class="sxs-lookup"><span data-stu-id="5c85f-130">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="5c85f-131">**Task \_ - \_ Typ2**</span><span class="sxs-lookup"><span data-stu-id="5c85f-131">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="5c85f-132">Definiert den Typ der Trigger, die von Tasks verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5c85f-132">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 


> [!WARNING]
> <span data-ttu-id="5c85f-133">Die Taskplaner 1,0-Enumerationen sind nur in den Betriebssystemen Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5c85f-133">The Task Scheduler 1.0 enumerations are available only in Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5c85f-134">Sie sind ab Windows Vista veraltet und werden möglicherweise in der Zukunft vollständig entfernt.</span><span class="sxs-lookup"><span data-stu-id="5c85f-134">They are deprecated as of Windows Vista and may be removed completely in the future.</span></span> <span data-ttu-id="5c85f-135">Verwenden Sie stattdessen die oben aufgeführten Taskplaner 2,0-Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="5c85f-135">Please use the Task Scheduler 2.0 enumerations listed above instead.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5c85f-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c85f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c85f-137">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="5c85f-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="5c85f-138">Taskplaner Referenz</span><span class="sxs-lookup"><span data-stu-id="5c85f-138">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




