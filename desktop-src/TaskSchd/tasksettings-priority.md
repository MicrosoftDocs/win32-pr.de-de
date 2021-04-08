---
title: Tasksettings. Priority (Eigenschaft)
description: Ruft bei der Skripterstellung die Prioritätsstufe der Aufgabe ab oder legt diese fest.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Prioritäts Eigenschaft Taskplaner
- Prioritäts Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, Priority-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282c688d63bb21f2dc0bab43acde7f089fa960b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949513"
---
# <a name="tasksettingspriority-property"></a><span data-ttu-id="52a92-106">Tasksettings. Priority (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="52a92-106">TaskSettings.Priority property</span></span>

<span data-ttu-id="52a92-107">Ruft bei der Skripterstellung die Prioritätsstufe der Aufgabe ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="52a92-107">For scripting, gets or sets the priority level of the task.</span></span>

<span data-ttu-id="52a92-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="52a92-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="52a92-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="52a92-109">Syntax</span></span>


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a><span data-ttu-id="52a92-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="52a92-110">Property value</span></span>

<span data-ttu-id="52a92-111">Die Prioritäts Ebene (0-10) der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="52a92-111">The priority level (0-10) of the task.</span></span> <span data-ttu-id="52a92-112">Der Standard ist 7.</span><span class="sxs-lookup"><span data-stu-id="52a92-112">The default is 7.</span></span>

## <a name="remarks"></a><span data-ttu-id="52a92-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52a92-113">Remarks</span></span>

<span data-ttu-id="52a92-114">Prioritätsstufe 0 ist die höchste Priorität, und Prioritätsstufe 10 ist die niedrigste Priorität.</span><span class="sxs-lookup"><span data-stu-id="52a92-114">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="52a92-115">Der Standardwert ist 7.</span><span class="sxs-lookup"><span data-stu-id="52a92-115">The default value is 7.</span></span> <span data-ttu-id="52a92-116">Die Prioritätsstufen 7 und 8 werden für Hintergrundaufgaben verwendet, und die Prioritätsstufen 4, 5 und 6 werden für interaktive Aufgaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="52a92-116">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="52a92-117">Die Aktion der Aufgabe wird in einem Prozess mit einer Priorität gestartet, die auf einem Prioritäts Klassen Wert basiert.</span><span class="sxs-lookup"><span data-stu-id="52a92-117">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="52a92-118">Ein Wert für die Prioritätsstufe (Thread Priorität) wird für com-Handler-, Meldungs-und e-Mail-Aufgaben Aktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="52a92-118">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="52a92-119">Weitere Informationen zu den Werten für die Prioritäts Klasse und Prioritätsstufen finden Sie unter [Planungs Prioritäten](/windows/desktop/ProcThread/scheduling-priorities).</span><span class="sxs-lookup"><span data-stu-id="52a92-119">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="52a92-120">In der folgenden Tabelle sind die möglichen Werte für den *Prioritäts* Parameter sowie die entsprechenden Werte für die Prioritäts Klasse und die Prioritäts Ebene aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="52a92-120">The following table lists the possible values for the *priority* parameter, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="52a92-121">Aufgaben *Priorität*</span><span class="sxs-lookup"><span data-stu-id="52a92-121">Task *priority*</span></span> | <span data-ttu-id="52a92-122">Prioritäts Klasse</span><span class="sxs-lookup"><span data-stu-id="52a92-122">Priority Class</span></span>                 | <span data-ttu-id="52a92-123">Prioritätsstufe</span><span class="sxs-lookup"><span data-stu-id="52a92-123">Priority Level</span></span>                   |
|-----------------|--------------------------------|----------------------------------|
| <span data-ttu-id="52a92-124">0</span><span class="sxs-lookup"><span data-stu-id="52a92-124">0</span></span>               | <span data-ttu-id="52a92-125">Realtime \_ priority- \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="52a92-125">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="52a92-126">Thread \_ Prioritäts \_ Zeit \_ kritisch</span><span class="sxs-lookup"><span data-stu-id="52a92-126">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="52a92-127">1</span><span class="sxs-lookup"><span data-stu-id="52a92-127">1</span></span>               | <span data-ttu-id="52a92-128">Klasse mit hoher \_ Priorität \_</span><span class="sxs-lookup"><span data-stu-id="52a92-128">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="52a92-129">Thread \_ Priorität \_ höchste</span><span class="sxs-lookup"><span data-stu-id="52a92-129">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="52a92-130">2</span><span class="sxs-lookup"><span data-stu-id="52a92-130">2</span></span>               | <span data-ttu-id="52a92-131">oberhalb der \_ normalen \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="52a92-131">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="52a92-132">Thread \_ Priorität \_ oberhalb des \_ normalen</span><span class="sxs-lookup"><span data-stu-id="52a92-132">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="52a92-133">3</span><span class="sxs-lookup"><span data-stu-id="52a92-133">3</span></span>               | <span data-ttu-id="52a92-134">oberhalb der \_ normalen \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="52a92-134">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="52a92-135">Thread \_ Priorität \_ oberhalb des \_ normalen</span><span class="sxs-lookup"><span data-stu-id="52a92-135">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="52a92-136">4</span><span class="sxs-lookup"><span data-stu-id="52a92-136">4</span></span>               | <span data-ttu-id="52a92-137">Klasse der normalen \_ Priorität \_</span><span class="sxs-lookup"><span data-stu-id="52a92-137">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="52a92-138">Thread \_ Priorität \_ Normal</span><span class="sxs-lookup"><span data-stu-id="52a92-138">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="52a92-139">5</span><span class="sxs-lookup"><span data-stu-id="52a92-139">5</span></span>               | <span data-ttu-id="52a92-140">Klasse der normalen \_ Priorität \_</span><span class="sxs-lookup"><span data-stu-id="52a92-140">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="52a92-141">Thread \_ Priorität \_ Normal</span><span class="sxs-lookup"><span data-stu-id="52a92-141">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="52a92-142">6</span><span class="sxs-lookup"><span data-stu-id="52a92-142">6</span></span>               | <span data-ttu-id="52a92-143">Klasse der normalen \_ Priorität \_</span><span class="sxs-lookup"><span data-stu-id="52a92-143">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="52a92-144">Thread \_ Priorität \_ Normal</span><span class="sxs-lookup"><span data-stu-id="52a92-144">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="52a92-145">7</span><span class="sxs-lookup"><span data-stu-id="52a92-145">7</span></span>               | <span data-ttu-id="52a92-146">unterhalb der \_ normalen \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="52a92-146">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="52a92-147">Thread \_ Priorität \_ unterhalb von \_ Normal</span><span class="sxs-lookup"><span data-stu-id="52a92-147">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="52a92-148">8</span><span class="sxs-lookup"><span data-stu-id="52a92-148">8</span></span>               | <span data-ttu-id="52a92-149">unterhalb der \_ normalen \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="52a92-149">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="52a92-150">Thread \_ Priorität \_ unterhalb von \_ Normal</span><span class="sxs-lookup"><span data-stu-id="52a92-150">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="52a92-151">9</span><span class="sxs-lookup"><span data-stu-id="52a92-151">9</span></span>               | <span data-ttu-id="52a92-152">inaktive \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="52a92-152">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="52a92-153">Thread \_ Priorität \_ niedrigste</span><span class="sxs-lookup"><span data-stu-id="52a92-153">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="52a92-154">10</span><span class="sxs-lookup"><span data-stu-id="52a92-154">10</span></span>              | <span data-ttu-id="52a92-155">inaktive \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="52a92-155">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="52a92-156">Thread \_ Priorität im \_ Leerlauf</span><span class="sxs-lookup"><span data-stu-id="52a92-156">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="52a92-157">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im Priority-Element [**(settingstype)**](taskschedulerschema-priority-settingstype-element.md) des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="52a92-157">When reading or writing XML for a task, this setting is specified in the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="52a92-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52a92-158">Requirements</span></span>



| <span data-ttu-id="52a92-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52a92-159">Requirement</span></span> | <span data-ttu-id="52a92-160">Wert</span><span class="sxs-lookup"><span data-stu-id="52a92-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52a92-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52a92-161">Minimum supported client</span></span><br/> | <span data-ttu-id="52a92-162">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52a92-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="52a92-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52a92-163">Minimum supported server</span></span><br/> | <span data-ttu-id="52a92-164">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52a92-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="52a92-165">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="52a92-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="52a92-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="52a92-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="52a92-167">DLL</span><span class="sxs-lookup"><span data-stu-id="52a92-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52a92-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52a92-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52a92-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52a92-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a92-170">**Tasksettings**</span><span class="sxs-lookup"><span data-stu-id="52a92-170">**TaskSettings**</span></span>](tasksettings.md)
</dt> </dl>

 

