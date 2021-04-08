---
title: Weeklyauslöserobjekt
description: Skript Objekt, das einen-Auslösers darstellt, der einen Task auf der Grundlage eines wöchentlichen Zeitplans startet.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- wöchentlicher auslöserTaskplaner, Objekt
- Weeklyauslöserobjekt Taskplaner
- Weeklyauslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58dec9172d38b53f779f44a048b39bc709dbd54f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743849"
---
# <a name="weeklytrigger-object"></a><span data-ttu-id="007e4-106">Weeklyauslöserobjekt</span><span class="sxs-lookup"><span data-stu-id="007e4-106">WeeklyTrigger object</span></span>

<span data-ttu-id="007e4-107">Skript Objekt, das einen-Auslösers darstellt, der einen Task auf der Grundlage eines wöchentlichen Zeitplans startet.</span><span class="sxs-lookup"><span data-stu-id="007e4-107">Scripting object that represents a trigger that starts a task based on a weekly schedule.</span></span> <span data-ttu-id="007e4-108">Der Task beginnt beispielsweise um 8:00 Uhr.</span><span class="sxs-lookup"><span data-stu-id="007e4-108">For example, the task starts at 8:00 A.M.</span></span> <span data-ttu-id="007e4-109">an einem bestimmten Wochentag oder jeder anderen Woche.</span><span class="sxs-lookup"><span data-stu-id="007e4-109">on a specific day of the week every week or every other week.</span></span>

## <a name="members"></a><span data-ttu-id="007e4-110">Member</span><span class="sxs-lookup"><span data-stu-id="007e4-110">Members</span></span>

<span data-ttu-id="007e4-111">Das **Weekly-Auslöserobjekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="007e4-111">The **WeeklyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="007e4-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="007e4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="007e4-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="007e4-113">Properties</span></span>

<span data-ttu-id="007e4-114">Das **Weekly-Auslöserobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="007e4-114">The **WeeklyTrigger** object has these properties.</span></span>



| <span data-ttu-id="007e4-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="007e4-115">Property</span></span>                                                            | <span data-ttu-id="007e4-116">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="007e4-116">Access type</span></span>           | <span data-ttu-id="007e4-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="007e4-117">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="007e4-118">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="007e4-118">**DaysOfWeek**</span></span>](weeklytrigger-daysofweek.md)<br/>           | <span data-ttu-id="007e4-119">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="007e4-119">Read/write</span></span><br/> | <span data-ttu-id="007e4-120">Ruft die Wochentage ab, an denen der Task ausgeführt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="007e4-120">Gets or sets the days of the week on which the task runs.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="007e4-121">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="007e4-121">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="007e4-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="007e4-122">Read/write</span></span><br/> | <span data-ttu-id="007e4-123">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="007e4-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="007e4-124">Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="007e4-124">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="007e4-125">**Endgrenze**</span><span class="sxs-lookup"><span data-stu-id="007e4-125">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="007e4-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="007e4-126">Read/write</span></span><br/> | <span data-ttu-id="007e4-127">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="007e4-127">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="007e4-128">Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="007e4-128">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="007e4-129">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="007e4-129">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="007e4-130">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="007e4-130">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="007e4-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="007e4-131">Read/write</span></span><br/> | <span data-ttu-id="007e4-132">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="007e4-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="007e4-133">Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="007e4-133">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="007e4-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="007e4-134">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="007e4-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="007e4-135">Read/write</span></span><br/> | <span data-ttu-id="007e4-136">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="007e4-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="007e4-137">Ruft den Bezeichner für den-Typ ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="007e4-137">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="007e4-138">**Randomdelay**</span><span class="sxs-lookup"><span data-stu-id="007e4-138">**RandomDelay**</span></span>](weeklytrigger-randomdelay.md)<br/>         | <span data-ttu-id="007e4-139">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="007e4-139">Read/write</span></span><br/> | <span data-ttu-id="007e4-140">Ruft eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="007e4-140">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="007e4-141">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="007e4-141">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="007e4-142">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="007e4-142">Read/write</span></span><br/> | <span data-ttu-id="007e4-143">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="007e4-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="007e4-144">Ruft ab oder legt fest, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="007e4-144">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="007e4-145">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="007e4-145">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="007e4-146">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="007e4-146">Read/write</span></span><br/> | <span data-ttu-id="007e4-147">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="007e4-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="007e4-148">Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="007e4-148">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="007e4-149">**type**</span><span class="sxs-lookup"><span data-stu-id="007e4-149">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="007e4-150">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="007e4-150">Read-only</span></span><br/>  | <span data-ttu-id="007e4-151">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="007e4-151">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="007e4-152">Ruft den Typ des Auslösers ab.</span><span class="sxs-lookup"><span data-stu-id="007e4-152">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="007e4-153">**Weeksinterval**</span><span class="sxs-lookup"><span data-stu-id="007e4-153">**WeeksInterval**</span></span>](weeklytrigger-weeksinterval.md)<br/>     | <span data-ttu-id="007e4-154">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="007e4-154">Read/write</span></span><br/> | <span data-ttu-id="007e4-155">Ruft das Intervall zwischen den Wochen im Zeitplan ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="007e4-155">Gets or sets the interval between the weeks in the schedule.</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="007e4-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="007e4-156">Remarks</span></span>

<span data-ttu-id="007e4-157">Die Uhrzeit, zu der die Aufgabe gestartet wird, wird von der [**StartBoundary**](trigger-startboundary.md) -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="007e4-157">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="007e4-158">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird ein wöchentlicher-Auslösers mit dem [**schedulebyweek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="007e4-158">When reading or writing your own XML for a task, a weekly trigger is specified using the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="007e4-159">Beispiele</span><span class="sxs-lookup"><span data-stu-id="007e4-159">Examples</span></span>

<span data-ttu-id="007e4-160">Weitere Informationen und ein Codebeispiel für dieses Skript Objekt finden Sie unter [Beispiel für ein wöchentliches Beispiel (Skripterstellung)](weekly-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="007e4-160">For more information and a code example for this scripting object, see [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="007e4-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="007e4-161">Requirements</span></span>



| <span data-ttu-id="007e4-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="007e4-162">Requirement</span></span> | <span data-ttu-id="007e4-163">Wert</span><span class="sxs-lookup"><span data-stu-id="007e4-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="007e4-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="007e4-164">Minimum supported client</span></span><br/> | <span data-ttu-id="007e4-165">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="007e4-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="007e4-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="007e4-166">Minimum supported server</span></span><br/> | <span data-ttu-id="007e4-167">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="007e4-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="007e4-168">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="007e4-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="007e4-169"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="007e4-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="007e4-170">DLL</span><span class="sxs-lookup"><span data-stu-id="007e4-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="007e4-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="007e4-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="007e4-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="007e4-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="007e4-173">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="007e4-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="007e4-174">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="007e4-174">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="007e4-175">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="007e4-175">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





