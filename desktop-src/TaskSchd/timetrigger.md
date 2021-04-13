---
title: Time-Auslöserobjekt (Windows. applicationmodel. Background. h)
description: Skript Objekt, das einen-Auslösers darstellt, der eine Aufgabe zu einem bestimmten Datum und einer bestimmten Uhrzeit startet.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- Zeit Auslöse Taskplaner, Objekt
- Time-Auslöserobjekt Taskplaner
- Time-Auslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TimeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8403b93e1c5292ade9f6f402b7e41994339140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340878"
---
# <a name="timetrigger-object"></a><span data-ttu-id="4c610-106">Timeauslöserobjekt</span><span class="sxs-lookup"><span data-stu-id="4c610-106">TimeTrigger object</span></span>

<span data-ttu-id="4c610-107">Skript Objekt, das einen-Auslösers darstellt, der eine Aufgabe zu einem bestimmten Datum und einer bestimmten Uhrzeit startet.</span><span class="sxs-lookup"><span data-stu-id="4c610-107">Scripting object that represents a trigger that starts a task at a specific date and time.</span></span>

## <a name="members"></a><span data-ttu-id="4c610-108">Member</span><span class="sxs-lookup"><span data-stu-id="4c610-108">Members</span></span>

<span data-ttu-id="4c610-109">Das **time-Auslöserobjekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4c610-109">The **TimeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="4c610-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4c610-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c610-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4c610-111">Properties</span></span>

<span data-ttu-id="4c610-112">Das **time-Auslöserobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4c610-112">The **TimeTrigger** object has these properties.</span></span>



| <span data-ttu-id="4c610-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4c610-113">Property</span></span>                                                            | <span data-ttu-id="4c610-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="4c610-114">Access type</span></span>           | <span data-ttu-id="4c610-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c610-115">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c610-116">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="4c610-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="4c610-117">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c610-117">Read/write</span></span><br/> | <span data-ttu-id="4c610-118">Geerbt von [**einem**](trigger.md)-Auslösung.</span><span class="sxs-lookup"><span data-stu-id="4c610-118">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="4c610-119">Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="4c610-119">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="4c610-120">**Endgrenze**</span><span class="sxs-lookup"><span data-stu-id="4c610-120">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="4c610-121">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c610-121">Read/write</span></span><br/> | <span data-ttu-id="4c610-122">Geerbt von [**einem**](trigger.md)-Auslösung.</span><span class="sxs-lookup"><span data-stu-id="4c610-122">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="4c610-123">Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="4c610-123">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="4c610-124">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="4c610-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="4c610-125">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="4c610-125">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="4c610-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c610-126">Read/write</span></span><br/> | <span data-ttu-id="4c610-127">Geerbt von [**einem**](trigger.md)-Auslösung.</span><span class="sxs-lookup"><span data-stu-id="4c610-127">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="4c610-128">Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="4c610-128">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="4c610-129">**Name**</span><span class="sxs-lookup"><span data-stu-id="4c610-129">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="4c610-130">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c610-130">Read/write</span></span><br/> | <span data-ttu-id="4c610-131">Geerbt von [**einem**](trigger.md)-Auslösung.</span><span class="sxs-lookup"><span data-stu-id="4c610-131">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="4c610-132">Ruft den Bezeichner für den-Typ ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="4c610-132">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="4c610-133">**Randomdelay**</span><span class="sxs-lookup"><span data-stu-id="4c610-133">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="4c610-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c610-134">Read/write</span></span><br/> | <span data-ttu-id="4c610-135">Ruft eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="4c610-135">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                    |
| [<span data-ttu-id="4c610-136">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="4c610-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="4c610-137">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c610-137">Read/write</span></span><br/> | <span data-ttu-id="4c610-138">Geerbt von [**einem**](trigger.md)-Auslösung.</span><span class="sxs-lookup"><span data-stu-id="4c610-138">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="4c610-139">Ruft ab oder legt fest, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="4c610-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="4c610-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="4c610-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="4c610-141">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c610-141">Read/write</span></span><br/> | <span data-ttu-id="4c610-142">Geerbt von [**einem**](trigger.md)-Auslösung.</span><span class="sxs-lookup"><span data-stu-id="4c610-142">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="4c610-143">Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="4c610-143">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="4c610-144">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4c610-144">This element is required.</span></span><br/>                                    |
| [<span data-ttu-id="4c610-145">**type**</span><span class="sxs-lookup"><span data-stu-id="4c610-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="4c610-146">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4c610-146">Read-only</span></span><br/>  | <span data-ttu-id="4c610-147">Geerbt von [**einem**](trigger.md)-Auslösung.</span><span class="sxs-lookup"><span data-stu-id="4c610-147">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="4c610-148">Ruft den Typ des Auslösers ab.</span><span class="sxs-lookup"><span data-stu-id="4c610-148">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="4c610-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c610-149">Remarks</span></span>

<span data-ttu-id="4c610-150">Das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element ist ein erforderliches Element für Zeit-und Kalender Trigger ([**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) und [**calendartrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span><span class="sxs-lookup"><span data-stu-id="4c610-150">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="4c610-151">Beim Lesen oder Schreiben von XML für eine Aufgabe wird ein Leerlauf-Auslösung mithilfe des [**time-Auslöserelements**](taskschedulerschema-timetrigger-triggergroup-element.md) des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="4c610-151">When reading or writing XML for a task, an idle trigger is specified using the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="4c610-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c610-152">Examples</span></span>

<span data-ttu-id="4c610-153">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="4c610-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c610-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c610-154">Requirements</span></span>



| <span data-ttu-id="4c610-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c610-155">Requirement</span></span> | <span data-ttu-id="4c610-156">Wert</span><span class="sxs-lookup"><span data-stu-id="4c610-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c610-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c610-157">Minimum supported client</span></span><br/> | <span data-ttu-id="4c610-158">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c610-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="4c610-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c610-159">Minimum supported server</span></span><br/> | <span data-ttu-id="4c610-160">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c610-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="4c610-161">Header</span><span class="sxs-lookup"><span data-stu-id="4c610-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c610-162"><dt>Windows. applicationmodel. Background. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c610-162"><dt>Windows.applicationmodel.background.h</dt></span></span> </dl> |
| <span data-ttu-id="4c610-163">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4c610-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c610-164"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4c610-164"><dt>Taskschd.tlb</dt></span></span> </dl>                          |
| <span data-ttu-id="4c610-165">DLL</span><span class="sxs-lookup"><span data-stu-id="4c610-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c610-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c610-166"><dt>Taskschd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4c610-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c610-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c610-168">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="4c610-168">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="4c610-169">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="4c610-169">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="4c610-170">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="4c610-170">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





