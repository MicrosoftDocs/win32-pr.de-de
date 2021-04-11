---
title: Monthlydowauslöserobjekt
description: Skript Objekt, das einen-Auslösers darstellt, der einen Task an einem monatlichen Wochentag startet.
ms.assetid: 18607189-295f-4f7d-bf72-f0ac8d5067cf
keywords:
- Monatlicher Dow-auslöserTaskplaner, Objekt
- Monthlydowauslöserobjekt Taskplaner
- Monthlydowauslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7e43925c6ebe27933a39fe5e25f37ffe6cf72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040398"
---
# <a name="monthlydowtrigger-object"></a><span data-ttu-id="3f16c-106">Monthlydowauslöserobjekt</span><span class="sxs-lookup"><span data-stu-id="3f16c-106">MonthlyDOWTrigger object</span></span>

<span data-ttu-id="3f16c-107">Skript Objekt, das einen-Auslösers darstellt, der einen Task an einem monatlichen Wochentag startet.</span><span class="sxs-lookup"><span data-stu-id="3f16c-107">Scripting object that represents a trigger that starts a task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="3f16c-108">Beispielsweise wird die Aufgabe an jedem ersten Donnerstag (Mai bis Oktober) gestartet.</span><span class="sxs-lookup"><span data-stu-id="3f16c-108">For example, the task starts on every first Thursday, May through October.</span></span>

## <a name="members"></a><span data-ttu-id="3f16c-109">Member</span><span class="sxs-lookup"><span data-stu-id="3f16c-109">Members</span></span>

<span data-ttu-id="3f16c-110">Das **monthlydowauslöserobjekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3f16c-110">The **MonthlyDOWTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="3f16c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3f16c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f16c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3f16c-112">Properties</span></span>

<span data-ttu-id="3f16c-113">Das **monthlydowauslöserobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3f16c-113">The **MonthlyDOWTrigger** object has these properties.</span></span>



| <span data-ttu-id="3f16c-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3f16c-114">Property</span></span>                                                                          | <span data-ttu-id="3f16c-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="3f16c-115">Access type</span></span>           | <span data-ttu-id="3f16c-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f16c-116">Description</span></span>                                                                                                                                                                                 |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f16c-117">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="3f16c-117">**DaysOfWeek**</span></span>](monthlydowtrigger-daysofweek.md)<br/>                     | <span data-ttu-id="3f16c-118">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3f16c-118">Read/write</span></span><br/> | <span data-ttu-id="3f16c-119">Ruft die Wochentage ab, an denen die Aufgabe ausgeführt wird, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="3f16c-119">Gets or sets the days of the week during which the task runs.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="3f16c-120">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="3f16c-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                     | <span data-ttu-id="3f16c-121">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3f16c-121">Read/write</span></span><br/> | <span data-ttu-id="3f16c-122">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="3f16c-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="3f16c-123">Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="3f16c-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="3f16c-124">Endgrenze</span><span class="sxs-lookup"><span data-stu-id="3f16c-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                                 | <span data-ttu-id="3f16c-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3f16c-125">Read/write</span></span><br/> | <span data-ttu-id="3f16c-126">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="3f16c-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="3f16c-127">Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="3f16c-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="3f16c-128">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="3f16c-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="3f16c-129">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="3f16c-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>               | <span data-ttu-id="3f16c-130">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3f16c-130">Read/write</span></span><br/> | <span data-ttu-id="3f16c-131">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="3f16c-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="3f16c-132">Ruft die maximale Zeitspanne ab, die der von diesem-Vorgang gestartete Task ausgeführt werden darf, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="3f16c-132">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                          |
| [<span data-ttu-id="3f16c-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="3f16c-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                              | <span data-ttu-id="3f16c-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3f16c-134">Read/write</span></span><br/> | <span data-ttu-id="3f16c-135">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="3f16c-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="3f16c-136">Ruft den Bezeichner für den-Typ ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="3f16c-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="3f16c-137">**MONTHSOFYEAR**</span><span class="sxs-lookup"><span data-stu-id="3f16c-137">**MonthsOfYear**</span></span>](monthlydowtrigger-monthsofyear.md)<br/>                 | <span data-ttu-id="3f16c-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3f16c-138">Read/write</span></span><br/> | <span data-ttu-id="3f16c-139">Ruft die Monate des Jahres ab, in denen die Aufgabe ausgeführt wird, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="3f16c-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="3f16c-140">**Randomdelay**</span><span class="sxs-lookup"><span data-stu-id="3f16c-140">**RandomDelay**</span></span>](monthlydowtrigger-randomdelay.md)<br/>                   | <span data-ttu-id="3f16c-141">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3f16c-141">Read/write</span></span><br/> | <span data-ttu-id="3f16c-142">Ruft eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="3f16c-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="3f16c-143">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="3f16c-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                               | <span data-ttu-id="3f16c-144">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3f16c-144">Read/write</span></span><br/> | <span data-ttu-id="3f16c-145">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="3f16c-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="3f16c-146">Ruft ab oder legt fest, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="3f16c-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="3f16c-147">**Runonlastweekosmonth**</span><span class="sxs-lookup"><span data-stu-id="3f16c-147">**RunOnLastWeekOfMonth**</span></span>](monthlydowtrigger-runonlastweekofmonth.md)<br/> | <span data-ttu-id="3f16c-148">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3f16c-148">Read/write</span></span><br/> | <span data-ttu-id="3f16c-149">Ruft einen booleschen Wert ab, der angibt, dass der Task in der letzten Woche des Monats ausgeführt wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="3f16c-149">Gets or sets a Boolean value that indicates that the task runs on the last week of the month.</span></span><br/>                                                                                    |
| [<span data-ttu-id="3f16c-150">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="3f16c-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                         | <span data-ttu-id="3f16c-151">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3f16c-151">Read/write</span></span><br/> | <span data-ttu-id="3f16c-152">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="3f16c-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="3f16c-153">Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="3f16c-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="3f16c-154">**type**</span><span class="sxs-lookup"><span data-stu-id="3f16c-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                          | <span data-ttu-id="3f16c-155">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f16c-155">Read-only</span></span><br/>  | <span data-ttu-id="3f16c-156">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="3f16c-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="3f16c-157">Ruft den Typ des Auslösers ab.</span><span class="sxs-lookup"><span data-stu-id="3f16c-157">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="3f16c-158">**Weeksofmonth**</span><span class="sxs-lookup"><span data-stu-id="3f16c-158">**WeeksOfMonth**</span></span>](monthlydowtrigger-weeksofmonth.md)<br/>                 | <span data-ttu-id="3f16c-159">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3f16c-159">Read/write</span></span><br/> | <span data-ttu-id="3f16c-160">Ruft die Wochen des Monats ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="3f16c-160">Gets or sets the weeks of the month during which the task runs.</span></span><br/>                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="3f16c-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f16c-161">Remarks</span></span>

<span data-ttu-id="3f16c-162">Die Uhrzeit, zu der die Aufgabe gestartet wird, wird von der [**StartBoundary**](trigger-startboundary.md) -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3f16c-162">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="3f16c-163">Beim Lesen oder Schreiben von XML für eine Aufgabe wird ein monatlicher Day-of-week-Befehl mithilfe des [**schedulebymonthdayosweek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) -Elements des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="3f16c-163">When reading or writing XML for a task, a monthly day-of-week trigger is specified using the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f16c-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f16c-164">Requirements</span></span>



| <span data-ttu-id="3f16c-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f16c-165">Requirement</span></span> | <span data-ttu-id="3f16c-166">Wert</span><span class="sxs-lookup"><span data-stu-id="3f16c-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f16c-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f16c-167">Minimum supported client</span></span><br/> | <span data-ttu-id="3f16c-168">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f16c-168">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3f16c-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f16c-169">Minimum supported server</span></span><br/> | <span data-ttu-id="3f16c-170">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f16c-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f16c-171">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3f16c-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="3f16c-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3f16c-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3f16c-173">DLL</span><span class="sxs-lookup"><span data-stu-id="3f16c-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f16c-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f16c-174"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f16c-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f16c-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f16c-176">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="3f16c-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="3f16c-177">Taskplaner Objekte</span><span class="sxs-lookup"><span data-stu-id="3f16c-177">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="3f16c-178">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="3f16c-178">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="3f16c-179">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="3f16c-179">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="3f16c-180">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="3f16c-180">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





