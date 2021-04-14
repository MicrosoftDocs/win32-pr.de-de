---
title: Dailyauslöserobjekt
description: Skript Objekt, das einen-Auslösers darstellt, der eine Aufgabe auf Grundlage eines täglichen Zeitplans startet.
ms.assetid: f03f53a0-0060-4793-96c1-b47a96852579
keywords:
- täglicher Taskplaner des Auslösers, Objekt
- Dailyauslöserobjekt Taskplaner
- Dailyauslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- DailyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22203ecf7a421f07ccb823745e6619e05f84f550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475981"
---
# <a name="dailytrigger-object"></a><span data-ttu-id="cf3c1-106">Dailyauslöserobjekt</span><span class="sxs-lookup"><span data-stu-id="cf3c1-106">DailyTrigger object</span></span>

<span data-ttu-id="cf3c1-107">Skript Objekt, das einen-Auslösers darstellt, der eine Aufgabe auf Grundlage eines täglichen Zeitplans startet.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-107">Scripting object that represents a trigger that starts a task based on a daily schedule.</span></span>

## <a name="members"></a><span data-ttu-id="cf3c1-108">Member</span><span class="sxs-lookup"><span data-stu-id="cf3c1-108">Members</span></span>

<span data-ttu-id="cf3c1-109">Das **Daily-Auslöserobjekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cf3c1-109">The **DailyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="cf3c1-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cf3c1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf3c1-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cf3c1-111">Properties</span></span>

<span data-ttu-id="cf3c1-112">Das **Daily-Auslöserobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-112">The **DailyTrigger** object has these properties.</span></span>



| <span data-ttu-id="cf3c1-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cf3c1-113">Property</span></span>                                                            | <span data-ttu-id="cf3c1-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="cf3c1-114">Access type</span></span>           | <span data-ttu-id="cf3c1-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf3c1-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf3c1-116">**Daysinterval**</span><span class="sxs-lookup"><span data-stu-id="cf3c1-116">**DaysInterval**</span></span>](dailytrigger-daysinterval.md)<br/>        | <span data-ttu-id="cf3c1-117">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cf3c1-117">Read/write</span></span><br/> | <span data-ttu-id="cf3c1-118">Ruft das Intervall zwischen den Tagen im Zeitplan ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-118">Gets or sets the interval between the days in the schedule.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="cf3c1-119">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="cf3c1-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="cf3c1-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cf3c1-120">Read/write</span></span><br/> | <span data-ttu-id="cf3c1-121">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="cf3c1-122">Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="cf3c1-123">**Endgrenze**</span><span class="sxs-lookup"><span data-stu-id="cf3c1-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="cf3c1-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cf3c1-124">Read/write</span></span><br/> | <span data-ttu-id="cf3c1-125">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="cf3c1-126">Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="cf3c1-127">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="cf3c1-128">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="cf3c1-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="cf3c1-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cf3c1-129">Read/write</span></span><br/> | <span data-ttu-id="cf3c1-130">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="cf3c1-131">Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="cf3c1-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="cf3c1-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="cf3c1-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cf3c1-133">Read/write</span></span><br/> | <span data-ttu-id="cf3c1-134">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="cf3c1-135">Ruft den Bezeichner für den-Typ ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="cf3c1-136">**Randomdelay**</span><span class="sxs-lookup"><span data-stu-id="cf3c1-136">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="cf3c1-137">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cf3c1-137">Read/write</span></span><br/> | <span data-ttu-id="cf3c1-138">Ruft eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-138">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="cf3c1-139">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="cf3c1-139">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="cf3c1-140">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cf3c1-140">Read/write</span></span><br/> | <span data-ttu-id="cf3c1-141">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="cf3c1-142">Ruft ab oder legt fest, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-142">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="cf3c1-143">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="cf3c1-143">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="cf3c1-144">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cf3c1-144">Read/write</span></span><br/> | <span data-ttu-id="cf3c1-145">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="cf3c1-146">Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-146">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="cf3c1-147">**type**</span><span class="sxs-lookup"><span data-stu-id="cf3c1-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="cf3c1-148">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cf3c1-148">Read-only</span></span><br/>  | <span data-ttu-id="cf3c1-149">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="cf3c1-150">Ruft den Typ des Auslösers ab.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-150">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="cf3c1-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf3c1-151">Remarks</span></span>

<span data-ttu-id="cf3c1-152">Die Uhrzeit, zu der die Aufgabe gestartet wird, wird von der [**StartBoundary**](trigger-startboundary.md) -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-152">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="cf3c1-153">Ein Intervall von 1 erzeugt einen täglichen Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-153">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="cf3c1-154">Ein Intervall von 2 erzeugt einen Zeitplan für jeden anderen Tag usw.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-154">An interval of 2 produces an every other day schedule and so on.</span></span>

<span data-ttu-id="cf3c1-155">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird ein täglicher-Vorgang mit dem [**schedulebyday**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="cf3c1-155">When reading or writing your own XML for a task, a daily trigger is specified using the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="cf3c1-156">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf3c1-156">Examples</span></span>

<span data-ttu-id="cf3c1-157">Weitere Informationen und ein Codebeispiel für dieses Skript Objekt finden Sie unter [Beispiel für das tägliche Beispiel (Skripterstellung)](daily-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="cf3c1-157">For more information and a code example for this scripting object, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf3c1-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf3c1-158">Requirements</span></span>



| <span data-ttu-id="cf3c1-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf3c1-159">Requirement</span></span> | <span data-ttu-id="cf3c1-160">Wert</span><span class="sxs-lookup"><span data-stu-id="cf3c1-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf3c1-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf3c1-161">Minimum supported client</span></span><br/> | <span data-ttu-id="cf3c1-162">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf3c1-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cf3c1-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf3c1-163">Minimum supported server</span></span><br/> | <span data-ttu-id="cf3c1-164">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf3c1-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cf3c1-165">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="cf3c1-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="cf3c1-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cf3c1-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cf3c1-167">DLL</span><span class="sxs-lookup"><span data-stu-id="cf3c1-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf3c1-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf3c1-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf3c1-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf3c1-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf3c1-170">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="cf3c1-170">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="cf3c1-171">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="cf3c1-171">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="cf3c1-172">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="cf3c1-172">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





