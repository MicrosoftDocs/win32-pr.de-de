---
title: Boottrigger-Objekt
description: Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn das System gestartet wird.
ms.assetid: 9d5a7cf6-2e1d-44ae-bb45-66424770d61b
keywords:
- Taskplaner des Start Auslösers, Objekt
- Boottrigger-Objekt Taskplaner
- Boottrigger-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- BootTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346a4bc7b20606f59c26b131590b92593d40d07e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479242"
---
# <a name="boottrigger-object"></a><span data-ttu-id="b6afc-106">Boottrigger-Objekt</span><span class="sxs-lookup"><span data-stu-id="b6afc-106">BootTrigger object</span></span>

<span data-ttu-id="b6afc-107">Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b6afc-107">Scripting object that represents a trigger that starts a task when the system is booted.</span></span>

## <a name="members"></a><span data-ttu-id="b6afc-108">Member</span><span class="sxs-lookup"><span data-stu-id="b6afc-108">Members</span></span>

<span data-ttu-id="b6afc-109">Das **boottrigger** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b6afc-109">The **BootTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="b6afc-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6afc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6afc-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6afc-111">Properties</span></span>

<span data-ttu-id="b6afc-112">Das **boottrigger** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b6afc-112">The **BootTrigger** object has these properties.</span></span>



| <span data-ttu-id="b6afc-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b6afc-113">Property</span></span>                                                            | <span data-ttu-id="b6afc-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="b6afc-114">Access type</span></span>           | <span data-ttu-id="b6afc-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6afc-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6afc-116">**Verzögern**</span><span class="sxs-lookup"><span data-stu-id="b6afc-116">**Delay**</span></span>](boottrigger-delay.md)<br/>                       |                       | <span data-ttu-id="b6afc-117">Ruft einen Wert ab oder legt einen Wert fest, der die Zeitspanne zwischen dem Start des Systems und dem Start der Aufgabe angibt.</span><span class="sxs-lookup"><span data-stu-id="b6afc-117">Gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.</span></span><br/>                                                           |
| [<span data-ttu-id="b6afc-118">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="b6afc-118">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="b6afc-119">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b6afc-119">Read/write</span></span><br/> | <span data-ttu-id="b6afc-120">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6afc-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6afc-121">Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="b6afc-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="b6afc-122">**Endgrenze**</span><span class="sxs-lookup"><span data-stu-id="b6afc-122">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="b6afc-123">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b6afc-123">Read/write</span></span><br/> | <span data-ttu-id="b6afc-124">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6afc-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6afc-125">Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="b6afc-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="b6afc-126">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="b6afc-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="b6afc-127">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="b6afc-127">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="b6afc-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b6afc-128">Read/write</span></span><br/> | <span data-ttu-id="b6afc-129">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6afc-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6afc-130">Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="b6afc-130">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="b6afc-131">**Name**</span><span class="sxs-lookup"><span data-stu-id="b6afc-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="b6afc-132">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b6afc-132">Read/write</span></span><br/> | <span data-ttu-id="b6afc-133">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6afc-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6afc-134">Ruft den Bezeichner für den-Typ ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="b6afc-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="b6afc-135">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="b6afc-135">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="b6afc-136">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b6afc-136">Read/write</span></span><br/> | <span data-ttu-id="b6afc-137">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6afc-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6afc-138">Ruft ab oder legt fest, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="b6afc-138">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="b6afc-139">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="b6afc-139">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="b6afc-140">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b6afc-140">Read/write</span></span><br/> | <span data-ttu-id="b6afc-141">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6afc-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6afc-142">Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="b6afc-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="b6afc-143">**type**</span><span class="sxs-lookup"><span data-stu-id="b6afc-143">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="b6afc-144">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6afc-144">Read-only</span></span><br/>  | <span data-ttu-id="b6afc-145">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6afc-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="b6afc-146">Ruft den Typ des Auslösers ab.</span><span class="sxs-lookup"><span data-stu-id="b6afc-146">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="b6afc-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6afc-147">Remarks</span></span>

<span data-ttu-id="b6afc-148">Der Taskplaner-Dienst wird gestartet, wenn das Betriebssystem gestartet wird, und Start auslösertasks werden festgelegt, wenn der Taskplaner Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b6afc-148">The Task Scheduler service is started when the operating system is booted, and boot trigger tasks are set to start when the Task Scheduler service starts.</span></span>

<span data-ttu-id="b6afc-149">Nur ein Mitglied der Gruppe "Administratoren" kann eine Aufgabe mit einem Start--Vorgang erstellen.</span><span class="sxs-lookup"><span data-stu-id="b6afc-149">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="b6afc-150">Beim Erstellen eines eigenen XML-Codes für eine Aufgabe wird ein Start--Befehl mit dem [**boottrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="b6afc-150">When creating your own XML for a task, a boot trigger is specified using the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="b6afc-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6afc-151">Examples</span></span>

<span data-ttu-id="b6afc-152">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [Beispiel für den Start-Beispiel (Skripterstellung)](boot-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="b6afc-152">For more information and example code for this scripting object, see [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6afc-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6afc-153">Requirements</span></span>



| <span data-ttu-id="b6afc-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6afc-154">Requirement</span></span> | <span data-ttu-id="b6afc-155">Wert</span><span class="sxs-lookup"><span data-stu-id="b6afc-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6afc-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6afc-156">Minimum supported client</span></span><br/> | <span data-ttu-id="b6afc-157">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6afc-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b6afc-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6afc-158">Minimum supported server</span></span><br/> | <span data-ttu-id="b6afc-159">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6afc-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b6afc-160">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b6afc-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6afc-161"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b6afc-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b6afc-162">DLL</span><span class="sxs-lookup"><span data-stu-id="b6afc-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6afc-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6afc-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6afc-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6afc-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6afc-165">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="b6afc-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="b6afc-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="b6afc-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="b6afc-167">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="b6afc-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





