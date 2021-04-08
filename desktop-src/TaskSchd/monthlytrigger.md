---
title: Monthly-Auslöserobjekt
description: Skript Objekt, das einen-Auslösers darstellt, der einen Task auf der Grundlage eines monatlichen Zeitplans startet.
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- Monatlicher auslöserTaskplaner, Objekt
- Monthly-Auslöserobjekt Taskplaner
- Monthly-Auslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- MonthlyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce433f626fbe45e209f881c00787495cc6343bc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741881"
---
# <a name="monthlytrigger-object"></a><span data-ttu-id="0ecdb-106">Monthly-Auslöserobjekt</span><span class="sxs-lookup"><span data-stu-id="0ecdb-106">MonthlyTrigger object</span></span>

<span data-ttu-id="0ecdb-107">Skript Objekt, das einen-Auslösers darstellt, der einen Task auf der Grundlage eines monatlichen Zeitplans startet.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-107">Scripting object that represents a trigger that starts a task based on a monthly schedule.</span></span> <span data-ttu-id="0ecdb-108">Beispielsweise wird die Aufgabe an bestimmten Tagen eines bestimmten Monats gestartet.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-108">For example, the task starts on specific days of specific months.</span></span>

## <a name="members"></a><span data-ttu-id="0ecdb-109">Member</span><span class="sxs-lookup"><span data-stu-id="0ecdb-109">Members</span></span>

<span data-ttu-id="0ecdb-110">Das **Monthly-Auslöserobjekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0ecdb-110">The **MonthlyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="0ecdb-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ecdb-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ecdb-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ecdb-112">Properties</span></span>

<span data-ttu-id="0ecdb-113">Das **Monthly-Auslöserobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-113">The **MonthlyTrigger** object has these properties.</span></span>



| <span data-ttu-id="0ecdb-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0ecdb-114">Property</span></span>                                                                     | <span data-ttu-id="0ecdb-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="0ecdb-115">Access type</span></span>           | <span data-ttu-id="0ecdb-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ecdb-116">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ecdb-117">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="0ecdb-117">**DaysOfMonth**</span></span>](monthlytrigger-daysofmonth.md)<br/>                 | <span data-ttu-id="0ecdb-118">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0ecdb-118">Read/write</span></span><br/> | <span data-ttu-id="0ecdb-119">Ruft die Tage des Monats ab, in denen die Aufgabe ausgeführt wird, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-119">Gets or sets the days of the month during which the task runs.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="0ecdb-120">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="0ecdb-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                | <span data-ttu-id="0ecdb-121">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0ecdb-121">Read/write</span></span><br/> | <span data-ttu-id="0ecdb-122">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0ecdb-123">Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="0ecdb-124">Endgrenze</span><span class="sxs-lookup"><span data-stu-id="0ecdb-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                            | <span data-ttu-id="0ecdb-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0ecdb-125">Read/write</span></span><br/> | <span data-ttu-id="0ecdb-126">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0ecdb-127">Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="0ecdb-128">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="0ecdb-129">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="0ecdb-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>          | <span data-ttu-id="0ecdb-130">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0ecdb-130">Read/write</span></span><br/> | <span data-ttu-id="0ecdb-131">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0ecdb-132">Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="0ecdb-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="0ecdb-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | <span data-ttu-id="0ecdb-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0ecdb-134">Read/write</span></span><br/> | <span data-ttu-id="0ecdb-135">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0ecdb-136">Ruft den Bezeichner für den-Typ ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="0ecdb-137">**MONTHSOFYEAR**</span><span class="sxs-lookup"><span data-stu-id="0ecdb-137">**MonthsOfYear**</span></span>](monthlytrigger-monthsofyear.md)<br/>               | <span data-ttu-id="0ecdb-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0ecdb-138">Read/write</span></span><br/> | <span data-ttu-id="0ecdb-139">Ruft die Monate des Jahres ab, in denen die Aufgabe ausgeführt wird, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="0ecdb-140">**Randomdelay**</span><span class="sxs-lookup"><span data-stu-id="0ecdb-140">**RandomDelay**</span></span>](monthlytrigger-randomdelay.md)<br/>                 | <span data-ttu-id="0ecdb-141">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0ecdb-141">Read/write</span></span><br/> | <span data-ttu-id="0ecdb-142">Ruft eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="0ecdb-143">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="0ecdb-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                          | <span data-ttu-id="0ecdb-144">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0ecdb-144">Read/write</span></span><br/> | <span data-ttu-id="0ecdb-145">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0ecdb-146">Ruft ab oder legt fest, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="0ecdb-147">**Runonlastdayosmonth**</span><span class="sxs-lookup"><span data-stu-id="0ecdb-147">**RunOnLastDayOfMonth**</span></span>](monthlytrigger-runonlastdayofmonth.md)<br/> | <span data-ttu-id="0ecdb-148">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0ecdb-148">Read/write</span></span><br/> | <span data-ttu-id="0ecdb-149">Ruft einen booleschen Wert ab, der angibt, dass der Task am letzten Tag des Monats ausgeführt wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-149">Gets or sets a Boolean value that indicates that the task runs on the last day of the month.</span></span><br/>                                                                                     |
| [<span data-ttu-id="0ecdb-150">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="0ecdb-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                    | <span data-ttu-id="0ecdb-151">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0ecdb-151">Read/write</span></span><br/> | <span data-ttu-id="0ecdb-152">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0ecdb-153">Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="0ecdb-154">**type**</span><span class="sxs-lookup"><span data-stu-id="0ecdb-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | <span data-ttu-id="0ecdb-155">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0ecdb-155">Read-only</span></span><br/>  | <span data-ttu-id="0ecdb-156">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0ecdb-157">Ruft den Typ des Auslösers ab.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-157">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="0ecdb-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ecdb-158">Remarks</span></span>

<span data-ttu-id="0ecdb-159">Die Uhrzeit, zu der die Aufgabe gestartet wird, wird von der [**StartBoundary**](trigger-startboundary.md) -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-159">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="0ecdb-160">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird ein monatlicher-Auslösers mit dem [**schedulebymonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="0ecdb-160">When reading or writing your own XML for a task, a monthly trigger is specified using the [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ecdb-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ecdb-161">Requirements</span></span>



| <span data-ttu-id="0ecdb-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ecdb-162">Requirement</span></span> | <span data-ttu-id="0ecdb-163">Wert</span><span class="sxs-lookup"><span data-stu-id="0ecdb-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ecdb-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ecdb-164">Minimum supported client</span></span><br/> | <span data-ttu-id="0ecdb-165">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ecdb-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0ecdb-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ecdb-166">Minimum supported server</span></span><br/> | <span data-ttu-id="0ecdb-167">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ecdb-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0ecdb-168">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0ecdb-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="0ecdb-169"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0ecdb-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0ecdb-170">DLL</span><span class="sxs-lookup"><span data-stu-id="0ecdb-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ecdb-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ecdb-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ecdb-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ecdb-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ecdb-173">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="0ecdb-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="0ecdb-174">Taskplaner Objekte</span><span class="sxs-lookup"><span data-stu-id="0ecdb-174">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="0ecdb-175">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="0ecdb-175">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="0ecdb-176">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="0ecdb-176">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="0ecdb-177">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="0ecdb-177">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





