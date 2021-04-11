---
title: Taskplaner 2,0-Enumerationstypen
description: Beschreibt die Enumerationstypen, die die Konstanten definieren, die von den Taskplaner 2,0-APIs verwendet werden.
ms.assetid: d59f017e-df32-4826-954d-9ba338282d0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db410564ab97f0477ecac8aeda2b54b8fd655d62
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316851"
---
# <a name="task-scheduler-20-enumerated-types"></a><span data-ttu-id="0cee6-103">Taskplaner 2,0-Enumerationstypen</span><span class="sxs-lookup"><span data-stu-id="0cee6-103">Task Scheduler 2.0 Enumerated Types</span></span>

<span data-ttu-id="0cee6-104">Beschreibt die Enumerationstypen, die die Konstanten definieren, die von den Taskplaner 2,0-APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0cee6-104">Describes the enumerated types that define the constants that are used by the Task Scheduler 2.0 APIs.</span></span>


<span data-ttu-id="0cee6-105">Die folgenden Enumerationstypen werden in Taskplaner 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0cee6-105">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="0cee6-106">Enumeration</span><span class="sxs-lookup"><span data-stu-id="0cee6-106">Enumeration</span></span>                                                                  | <span data-ttu-id="0cee6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0cee6-107">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0cee6-108">**Task \_ \_ Aktionstyp**</span><span class="sxs-lookup"><span data-stu-id="0cee6-108">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="0cee6-109">Definiert die Art von Aktionen, die von einer Aufgabe durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="0cee6-109">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="0cee6-110">**Aufgaben \_ Kompatibilität**</span><span class="sxs-lookup"><span data-stu-id="0cee6-110">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="0cee6-111">Definiert, welche Versionen von Taskplaner oder den at-Befehl, mit dem die Aufgabe kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="0cee6-111">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="0cee6-112">**Task \_ Erstellung**</span><span class="sxs-lookup"><span data-stu-id="0cee6-112">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="0cee6-113">Definiert, wie der Taskplaner-Dienst die Aufgabe erstellt, aktualisiert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0cee6-113">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="0cee6-114">**\_taskaufgabenflags \_**</span><span class="sxs-lookup"><span data-stu-id="0cee6-114">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="0cee6-115">Definiert, wie die Taskplaner durch registrierte Tasks aufzählt.</span><span class="sxs-lookup"><span data-stu-id="0cee6-115">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="0cee6-116">**Task \_ Instanzen \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="0cee6-116">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="0cee6-117">Definiert, wie die Taskplaner vorhandene Instanzen der Aufgabe behandelt, wenn eine neue Instanz der Aufgabe gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0cee6-117">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="0cee6-118">**Task \_ Anmeldetyp**</span><span class="sxs-lookup"><span data-stu-id="0cee6-118">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="0cee6-119">Definiert, welche Anmelde Methode zum Ausführen einer Aufgabe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0cee6-119">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="0cee6-120">**Task \_ processtokensid- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="0cee6-120">**TASK\_PROCESSTOKENSID\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)             | <span data-ttu-id="0cee6-121">Definiert die Typen der Prozess-sid, die von Tasks verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0cee6-121">Defines the types of process SID that can be used by tasks.</span></span>                                                      |
| [<span data-ttu-id="0cee6-122">**\_ \_ tasktestflags**</span><span class="sxs-lookup"><span data-stu-id="0cee6-122">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="0cee6-123">Definiert, wie eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0cee6-123">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="0cee6-124">**\_taskrunlevel- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="0cee6-124">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="0cee6-125">Definiert Lua-Erweiterungs Flags, die angeben, welche Berechtigungsebene für die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0cee6-125">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="0cee6-126">**\_ \_ Status \_ \_ Änderungstyp für Task Sitzung**</span><span class="sxs-lookup"><span data-stu-id="0cee6-126">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="0cee6-127">Definiert, welche Arten von Terminal Server-Sitzungs Statusänderungen Sie verwenden können, um einen Task zu starten.</span><span class="sxs-lookup"><span data-stu-id="0cee6-127">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="0cee6-128">**Task \_ Status**</span><span class="sxs-lookup"><span data-stu-id="0cee6-128">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="0cee6-129">Definiert die verschiedenen Zustände, in denen sich eine registrierte Aufgabe befinden kann.</span><span class="sxs-lookup"><span data-stu-id="0cee6-129">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="0cee6-130">**Task \_ - \_ Typ2**</span><span class="sxs-lookup"><span data-stu-id="0cee6-130">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="0cee6-131">Definiert den Typ der Trigger, die von Tasks verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0cee6-131">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="0cee6-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0cee6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cee6-133">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="0cee6-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="0cee6-134">Taskplaner Referenz</span><span class="sxs-lookup"><span data-stu-id="0cee6-134">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




