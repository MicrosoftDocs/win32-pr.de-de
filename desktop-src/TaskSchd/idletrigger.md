---
title: Idle-Auslöserobjekt
description: Skript Objekt, das einen-Fehler darstellt, der einen Task startet, wenn eine Leerlauf Bedingung auftritt.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- Leerlauf-auslöserTaskplaner, Objekt
- Idle-Auslöserobjekt Taskplaner
- Idle-Auslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72288827fec34257bf4f54a152031ef37068790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342877"
---
# <a name="idletrigger-object"></a><span data-ttu-id="57b6c-106">Idle-Auslöserobjekt</span><span class="sxs-lookup"><span data-stu-id="57b6c-106">IdleTrigger object</span></span>

<span data-ttu-id="57b6c-107">Skript Objekt, das einen-Fehler darstellt, der einen Task startet, wenn eine Leerlauf Bedingung auftritt.</span><span class="sxs-lookup"><span data-stu-id="57b6c-107">Scripting object that represents a trigger that starts a task when an idle condition occurs.</span></span> <span data-ttu-id="57b6c-108">Informationen zu Bedingungen im Leerlauf finden Sie unter [Aufgaben im Leerlauf](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="57b6c-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="57b6c-109">Member</span><span class="sxs-lookup"><span data-stu-id="57b6c-109">Members</span></span>

<span data-ttu-id="57b6c-110">Das **Idle-Auslöserobjekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="57b6c-110">The **IdleTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="57b6c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="57b6c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57b6c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="57b6c-112">Properties</span></span>

<span data-ttu-id="57b6c-113">Das **Idle-Auslöserobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="57b6c-113">The **IdleTrigger** object has these properties.</span></span>



| <span data-ttu-id="57b6c-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="57b6c-114">Property</span></span>                                                            | <span data-ttu-id="57b6c-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="57b6c-115">Access type</span></span>           | <span data-ttu-id="57b6c-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57b6c-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57b6c-117">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="57b6c-117">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="57b6c-118">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57b6c-118">Read/write</span></span><br/> | <span data-ttu-id="57b6c-119">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="57b6c-119">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="57b6c-120">Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="57b6c-120">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="57b6c-121">Endgrenze</span><span class="sxs-lookup"><span data-stu-id="57b6c-121">EndBoundary</span></span>](trigger-endboundary.md)<br/>                   | <span data-ttu-id="57b6c-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57b6c-122">Read/write</span></span><br/> | <span data-ttu-id="57b6c-123">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="57b6c-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="57b6c-124">Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="57b6c-124">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="57b6c-125">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="57b6c-125">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="57b6c-126">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="57b6c-126">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="57b6c-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57b6c-127">Read/write</span></span><br/> | <span data-ttu-id="57b6c-128">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="57b6c-128">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="57b6c-129">Ruft den maximalen Zeitraum ab, in dem der Task vom-Vorgang gestartet werden kann, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="57b6c-129">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="57b6c-130">**Name**</span><span class="sxs-lookup"><span data-stu-id="57b6c-130">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="57b6c-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57b6c-131">Read/write</span></span><br/> | <span data-ttu-id="57b6c-132">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="57b6c-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="57b6c-133">Ruft den Bezeichner für den-Typ ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="57b6c-133">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="57b6c-134">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="57b6c-134">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="57b6c-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57b6c-135">Read/write</span></span><br/> | <span data-ttu-id="57b6c-136">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="57b6c-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="57b6c-137">Ruft einen Wert ab, der angibt, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird, oder legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="57b6c-137">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="57b6c-138">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="57b6c-138">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="57b6c-139">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57b6c-139">Read/write</span></span><br/> | <span data-ttu-id="57b6c-140">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="57b6c-140">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="57b6c-141">Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="57b6c-141">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="57b6c-142">**type**</span><span class="sxs-lookup"><span data-stu-id="57b6c-142">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="57b6c-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="57b6c-143">Read-only</span></span><br/>  | <span data-ttu-id="57b6c-144">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="57b6c-144">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="57b6c-145">Ruft den Typ des Auslösers ab.</span><span class="sxs-lookup"><span data-stu-id="57b6c-145">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="57b6c-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57b6c-146">Remarks</span></span>

<span data-ttu-id="57b6c-147">Ein Leerlauf-Triggervorgang löst nur dann eine Task Aktion aus, wenn der Computer nach der Start Grenze des Auslösers in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="57b6c-147">An idle trigger will only trigger a task action if the computer goes into an idle state after the start boundary of the trigger.</span></span>

<span data-ttu-id="57b6c-148">Beim Lesen oder Schreiben von XML für eine Aufgabe wird mit dem [**Idle-Auslöserelement**](taskschedulerschema-idletrigger-triggergroup-element.md) des Taskplaner Schemas ein Leerlauf--Auslöserwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="57b6c-148">When reading or writing XML for a task, an idle trigger is specified using the [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="57b6c-149">Wenn eine Aufgabe durch einen Leerlauf Trigger ausgelöst wird, wird die [**idlesettings. WaitTimeout**](idlesettings-waittimeout.md) -Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="57b6c-149">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

<span data-ttu-id="57b6c-150">Wenn die anfängliche Instanz eines Tasks mit einem Leerlauf-ausgelöst wird, wird die Aufgabe nur einmal ohne Wiederholungen gestartet, auch wenn in der [**Wiederholungs**](trigger-repetition.md) Eigenschaft mehrfache Wiederholung definiert ist.</span><span class="sxs-lookup"><span data-stu-id="57b6c-150">If the initial instance of a task with an idle trigger is still running, then the task is only launched once with no repetitions, even if multiple repetition is defined in the [**Repetition**](trigger-repetition.md) property.</span></span> <span data-ttu-id="57b6c-151">Dieses Verhalten tritt nicht auf, wenn der Task von sich selbst beendet wird.</span><span class="sxs-lookup"><span data-stu-id="57b6c-151">This behavior does not occur if the task stops by itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="57b6c-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57b6c-152">Requirements</span></span>



| <span data-ttu-id="57b6c-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57b6c-153">Requirement</span></span> | <span data-ttu-id="57b6c-154">Wert</span><span class="sxs-lookup"><span data-stu-id="57b6c-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57b6c-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57b6c-155">Minimum supported client</span></span><br/> | <span data-ttu-id="57b6c-156">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57b6c-156">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="57b6c-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57b6c-157">Minimum supported server</span></span><br/> | <span data-ttu-id="57b6c-158">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57b6c-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="57b6c-159">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="57b6c-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="57b6c-160"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="57b6c-160"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="57b6c-161">DLL</span><span class="sxs-lookup"><span data-stu-id="57b6c-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57b6c-162"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57b6c-162"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57b6c-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57b6c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b6c-164">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="57b6c-164">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="57b6c-165">Taskplaner Objekte</span><span class="sxs-lookup"><span data-stu-id="57b6c-165">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="57b6c-166">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="57b6c-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





