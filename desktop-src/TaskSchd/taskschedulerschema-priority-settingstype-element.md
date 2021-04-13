---
title: Priority (settingstype)-Element
description: Gibt die Prioritätsstufe für den Task an.
ms.assetid: 4885fffa-b7d9-4f5e-b6e8-6f18b01c2427
keywords:
- Priority-Element Taskplaner
topic_type:
- apiref
api_name:
- Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecda59ecbbe23550363fb30706d73bca54fcd925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391632"
---
# <a name="priority-settingstype-element"></a><span data-ttu-id="a5ffa-104">Priority (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="a5ffa-104">Priority (settingsType) Element</span></span>

<span data-ttu-id="a5ffa-105">Gibt die Prioritätsstufe für den Task an.</span><span class="sxs-lookup"><span data-stu-id="a5ffa-105">Specifies the priority level for the task.</span></span>

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

<span data-ttu-id="a5ffa-106">Das **Priority** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="a5ffa-106">The **Priority** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a5ffa-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="a5ffa-107">Parent element</span></span>



| <span data-ttu-id="a5ffa-108">Element</span><span class="sxs-lookup"><span data-stu-id="a5ffa-108">Element</span></span>                                                           | <span data-ttu-id="a5ffa-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="a5ffa-109">Derived from</span></span>                                                         | <span data-ttu-id="a5ffa-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5ffa-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5ffa-111">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="a5ffa-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="a5ffa-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="a5ffa-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="a5ffa-113">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a5ffa-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a5ffa-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5ffa-114">Remarks</span></span>

<span data-ttu-id="a5ffa-115">Prioritätsstufe 0 ist die höchste Priorität, und Prioritätsstufe 10 ist die niedrigste Priorität.</span><span class="sxs-lookup"><span data-stu-id="a5ffa-115">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="a5ffa-116">Der Standardwert ist 7.</span><span class="sxs-lookup"><span data-stu-id="a5ffa-116">The default value is 7.</span></span> <span data-ttu-id="a5ffa-117">Der minimale und der maximale Wert werden vom einfachen [**prioritytype**](taskschedulerschema-prioritytype-simpletype.md) -Typ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a5ffa-117">The minimum and maximum values are set by the [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) simple type.</span></span> <span data-ttu-id="a5ffa-118">Die Prioritätsstufen 7 und 8 werden für Hintergrundaufgaben verwendet, und die Prioritätsstufen 4, 5 und 6 werden für interaktive Aufgaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5ffa-118">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="a5ffa-119">Die Aktion der Aufgabe wird in einem Prozess mit einer Priorität gestartet, die auf einem Prioritäts Klassen Wert basiert.</span><span class="sxs-lookup"><span data-stu-id="a5ffa-119">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="a5ffa-120">Ein Wert für die Prioritätsstufe (Thread Priorität) wird für com-Handler-, Meldungs-und e-Mail-Aufgaben Aktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5ffa-120">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="a5ffa-121">Weitere Informationen zu den Werten für die Prioritäts Klasse und Prioritätsstufen finden Sie unter [Planungs Prioritäten](/windows/desktop/ProcThread/scheduling-priorities).</span><span class="sxs-lookup"><span data-stu-id="a5ffa-121">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="a5ffa-122">In der folgenden Tabelle sind die möglichen Werte für das **Prioritäts** Element sowie die entsprechenden Werte für die Prioritäts Klasse und die Prioritäts Ebene aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5ffa-122">The following table lists the possible values for the **Priority** element, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="a5ffa-123">Aufgaben Priorität</span><span class="sxs-lookup"><span data-stu-id="a5ffa-123">Task Priority</span></span> | <span data-ttu-id="a5ffa-124">Prioritäts Klasse</span><span class="sxs-lookup"><span data-stu-id="a5ffa-124">Priority Class</span></span>                 | <span data-ttu-id="a5ffa-125">Prioritätsstufe</span><span class="sxs-lookup"><span data-stu-id="a5ffa-125">Priority Level</span></span>                   |
|---------------|--------------------------------|----------------------------------|
| <span data-ttu-id="a5ffa-126">0</span><span class="sxs-lookup"><span data-stu-id="a5ffa-126">0</span></span>             | <span data-ttu-id="a5ffa-127">Realtime \_ priority- \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="a5ffa-127">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="a5ffa-128">Thread \_ Prioritäts \_ Zeit \_ kritisch</span><span class="sxs-lookup"><span data-stu-id="a5ffa-128">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="a5ffa-129">1</span><span class="sxs-lookup"><span data-stu-id="a5ffa-129">1</span></span>             | <span data-ttu-id="a5ffa-130">Klasse mit hoher \_ Priorität \_</span><span class="sxs-lookup"><span data-stu-id="a5ffa-130">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="a5ffa-131">Thread \_ Priorität \_ höchste</span><span class="sxs-lookup"><span data-stu-id="a5ffa-131">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="a5ffa-132">2</span><span class="sxs-lookup"><span data-stu-id="a5ffa-132">2</span></span>             | <span data-ttu-id="a5ffa-133">oberhalb der \_ normalen \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="a5ffa-133">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="a5ffa-134">Thread \_ Priorität \_ oberhalb des \_ normalen</span><span class="sxs-lookup"><span data-stu-id="a5ffa-134">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="a5ffa-135">3</span><span class="sxs-lookup"><span data-stu-id="a5ffa-135">3</span></span>             | <span data-ttu-id="a5ffa-136">oberhalb der \_ normalen \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="a5ffa-136">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="a5ffa-137">Thread \_ Priorität \_ oberhalb des \_ normalen</span><span class="sxs-lookup"><span data-stu-id="a5ffa-137">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="a5ffa-138">4</span><span class="sxs-lookup"><span data-stu-id="a5ffa-138">4</span></span>             | <span data-ttu-id="a5ffa-139">Klasse der normalen \_ Priorität \_</span><span class="sxs-lookup"><span data-stu-id="a5ffa-139">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="a5ffa-140">Thread \_ Priorität \_ Normal</span><span class="sxs-lookup"><span data-stu-id="a5ffa-140">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="a5ffa-141">5</span><span class="sxs-lookup"><span data-stu-id="a5ffa-141">5</span></span>             | <span data-ttu-id="a5ffa-142">Klasse der normalen \_ Priorität \_</span><span class="sxs-lookup"><span data-stu-id="a5ffa-142">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="a5ffa-143">Thread \_ Priorität \_ Normal</span><span class="sxs-lookup"><span data-stu-id="a5ffa-143">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="a5ffa-144">6</span><span class="sxs-lookup"><span data-stu-id="a5ffa-144">6</span></span>             | <span data-ttu-id="a5ffa-145">Klasse der normalen \_ Priorität \_</span><span class="sxs-lookup"><span data-stu-id="a5ffa-145">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="a5ffa-146">Thread \_ Priorität \_ Normal</span><span class="sxs-lookup"><span data-stu-id="a5ffa-146">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="a5ffa-147">7</span><span class="sxs-lookup"><span data-stu-id="a5ffa-147">7</span></span>             | <span data-ttu-id="a5ffa-148">unterhalb der \_ normalen \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="a5ffa-148">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="a5ffa-149">Thread \_ Priorität \_ unterhalb von \_ Normal</span><span class="sxs-lookup"><span data-stu-id="a5ffa-149">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="a5ffa-150">8</span><span class="sxs-lookup"><span data-stu-id="a5ffa-150">8</span></span>             | <span data-ttu-id="a5ffa-151">unterhalb der \_ normalen \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="a5ffa-151">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="a5ffa-152">Thread \_ Priorität \_ unterhalb von \_ Normal</span><span class="sxs-lookup"><span data-stu-id="a5ffa-152">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="a5ffa-153">9</span><span class="sxs-lookup"><span data-stu-id="a5ffa-153">9</span></span>             | <span data-ttu-id="a5ffa-154">inaktive \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="a5ffa-154">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="a5ffa-155">Thread \_ Priorität \_ niedrigste</span><span class="sxs-lookup"><span data-stu-id="a5ffa-155">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="a5ffa-156">10</span><span class="sxs-lookup"><span data-stu-id="a5ffa-156">10</span></span>            | <span data-ttu-id="a5ffa-157">inaktive \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="a5ffa-157">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="a5ffa-158">Thread \_ Priorität im \_ Leerlauf</span><span class="sxs-lookup"><span data-stu-id="a5ffa-158">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="a5ffa-159">Informationen zur C++-Entwicklung finden Sie unter [**Priority-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).</span><span class="sxs-lookup"><span data-stu-id="a5ffa-159">For C++ development, see [**Priority Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).</span></span>

<span data-ttu-id="a5ffa-160">Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. Priority**](tasksettings-priority.md).</span><span class="sxs-lookup"><span data-stu-id="a5ffa-160">For script development, see [**TaskSettings.Priority**](tasksettings-priority.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5ffa-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5ffa-161">Requirements</span></span>



| <span data-ttu-id="a5ffa-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5ffa-162">Requirement</span></span> | <span data-ttu-id="a5ffa-163">Wert</span><span class="sxs-lookup"><span data-stu-id="a5ffa-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a5ffa-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5ffa-164">Minimum supported client</span></span><br/> | <span data-ttu-id="a5ffa-165">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5ffa-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a5ffa-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5ffa-166">Minimum supported server</span></span><br/> | <span data-ttu-id="a5ffa-167">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5ffa-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5ffa-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5ffa-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5ffa-169">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="a5ffa-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

