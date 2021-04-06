---
title: Auslöse Objekt
description: Skript Objekt, das die allgemeinen Eigenschaften bereitstellt, die von allen auslöserobjekten geerbt werden.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- Trigger Taskplaner, Triggerobjekt
- Auslöse Objekt Taskplaner
- Taskplaner des Auslösers Objekts, beschrieben
topic_type:
- apiref
api_name:
- Trigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4a7edc6eff0bb04c81ba3bff3bb86ec0455b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858766"
---
# <a name="trigger-object"></a><span data-ttu-id="4933b-106">Auslöse Objekt</span><span class="sxs-lookup"><span data-stu-id="4933b-106">Trigger object</span></span>

<span data-ttu-id="4933b-107">Skript Objekt, das die allgemeinen Eigenschaften bereitstellt, die von allen auslöserobjekten geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="4933b-107">Scripting object that provides the common properties that are inherited by all trigger objects.</span></span>

## <a name="members"></a><span data-ttu-id="4933b-108">Member</span><span class="sxs-lookup"><span data-stu-id="4933b-108">Members</span></span>

<span data-ttu-id="4933b-109">Das **Auslöserobjekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4933b-109">The **Trigger** object has these types of members:</span></span>

-   [<span data-ttu-id="4933b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4933b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4933b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4933b-111">Properties</span></span>

<span data-ttu-id="4933b-112">Das **Auslöserobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4933b-112">The **Trigger** object has these properties.</span></span>



| <span data-ttu-id="4933b-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4933b-113">Property</span></span>                                                            | <span data-ttu-id="4933b-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="4933b-114">Access type</span></span>           | <span data-ttu-id="4933b-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4933b-115">Description</span></span>                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4933b-116">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="4933b-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="4933b-117">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4933b-117">Read/write</span></span><br/> | <span data-ttu-id="4933b-118">Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="4933b-118">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="4933b-119">**Endgrenze**</span><span class="sxs-lookup"><span data-stu-id="4933b-119">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="4933b-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4933b-120">Read/write</span></span><br/> | <span data-ttu-id="4933b-121">Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="4933b-121">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="4933b-122">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="4933b-122">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="4933b-123">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="4933b-123">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="4933b-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4933b-124">Read/write</span></span><br/> | <span data-ttu-id="4933b-125">Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="4933b-125">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="4933b-126">**Name**</span><span class="sxs-lookup"><span data-stu-id="4933b-126">**Id**</span></span>](trigger-id.md)<br/>                                 | <span data-ttu-id="4933b-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4933b-127">Read/write</span></span><br/> | <span data-ttu-id="4933b-128">Ruft den Bezeichner für den-Typ ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="4933b-128">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="4933b-129">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="4933b-129">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="4933b-130">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4933b-130">Read/write</span></span><br/> | <span data-ttu-id="4933b-131">Ruft einen Wert ab, der angibt, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird, oder legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="4933b-131">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="4933b-132">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="4933b-132">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="4933b-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4933b-133">Read/write</span></span><br/> | <span data-ttu-id="4933b-134">Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="4933b-134">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="4933b-135">Der-Vorgang kann die Aufgabe starten, nachdem der-Vorgang aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="4933b-135">The trigger can start the task after the trigger is activated.</span></span><br/>             |
| [<span data-ttu-id="4933b-136">**type**</span><span class="sxs-lookup"><span data-stu-id="4933b-136">**Type**</span></span>](trigger-type.md)<br/>                             |                       | <span data-ttu-id="4933b-137">Ruft den Typ des Auslösers ab.</span><span class="sxs-lookup"><span data-stu-id="4933b-137">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="4933b-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4933b-138">Remarks</span></span>

<span data-ttu-id="4933b-139">Der Taskplaner stellt die folgenden einzelnen Objekte für die verschiedenen Trigger bereit, die von einem Task verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="4933b-139">The Task Scheduler provides the following individual objects for the different triggers that a task can use:</span></span>

-   [<span data-ttu-id="4933b-140">**Boottrigger**</span><span class="sxs-lookup"><span data-stu-id="4933b-140">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="4933b-141">**Dailylöst**</span><span class="sxs-lookup"><span data-stu-id="4933b-141">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="4933b-142">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="4933b-142">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="4933b-143">**Idle-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="4933b-143">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="4933b-144">**Logonauslöst**</span><span class="sxs-lookup"><span data-stu-id="4933b-144">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="4933b-145">**Monthlydowlöst**</span><span class="sxs-lookup"><span data-stu-id="4933b-145">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="4933b-146">**Monthly-auslöst**</span><span class="sxs-lookup"><span data-stu-id="4933b-146">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="4933b-147">**Registration-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="4933b-147">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="4933b-148">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="4933b-148">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="4933b-149">**Weeklyauslösers**</span><span class="sxs-lookup"><span data-stu-id="4933b-149">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="4933b-150">**Sessionstatechange-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="4933b-150">**SessionStateChangeTrigger**</span></span>](sessionstatechangetrigger.md)

<span data-ttu-id="4933b-151">Beim Lesen oder Schreiben von XML werden die Trigger einer Aufgabe im [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) -Element des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="4933b-151">When reading or writing XML, the triggers of a task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="4933b-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4933b-152">Examples</span></span>

<span data-ttu-id="4933b-153">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="4933b-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4933b-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4933b-154">Requirements</span></span>



| <span data-ttu-id="4933b-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4933b-155">Requirement</span></span> | <span data-ttu-id="4933b-156">Wert</span><span class="sxs-lookup"><span data-stu-id="4933b-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4933b-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4933b-157">Minimum supported client</span></span><br/> | <span data-ttu-id="4933b-158">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4933b-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4933b-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4933b-159">Minimum supported server</span></span><br/> | <span data-ttu-id="4933b-160">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4933b-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4933b-161">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4933b-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="4933b-162"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4933b-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4933b-163">DLL</span><span class="sxs-lookup"><span data-stu-id="4933b-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4933b-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4933b-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4933b-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4933b-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4933b-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="4933b-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> </dl>

 

 





