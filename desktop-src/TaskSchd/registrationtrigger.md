---
title: Registration-Auslöserobjekt
description: Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn der Task registriert oder aktualisiert wird.
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- Taskplaner des Registrierungs Auslösers, Objekt
- Registration-Auslöserobjekt Taskplaner
- Registration-Auslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08bf84fa92b1736b2989c1920abb8f0af2c0b97c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518080"
---
# <a name="registrationtrigger-object"></a><span data-ttu-id="08dfd-106">Registration-Auslöserobjekt</span><span class="sxs-lookup"><span data-stu-id="08dfd-106">RegistrationTrigger object</span></span>

<span data-ttu-id="08dfd-107">Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn der Task registriert oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="08dfd-107">Scripting object that represents a trigger that starts a task when the task is registered or updated.</span></span>

## <a name="members"></a><span data-ttu-id="08dfd-108">Member</span><span class="sxs-lookup"><span data-stu-id="08dfd-108">Members</span></span>

<span data-ttu-id="08dfd-109">Das **Registration-Auslöserobjekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="08dfd-109">The **RegistrationTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="08dfd-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08dfd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08dfd-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08dfd-111">Properties</span></span>

<span data-ttu-id="08dfd-112">Das **Registration-Auslöserobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08dfd-112">The **RegistrationTrigger** object has these properties.</span></span>



| <span data-ttu-id="08dfd-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="08dfd-113">Property</span></span>                                                            | <span data-ttu-id="08dfd-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="08dfd-114">Access type</span></span>           | <span data-ttu-id="08dfd-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08dfd-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08dfd-116">**Verzögern**</span><span class="sxs-lookup"><span data-stu-id="08dfd-116">**Delay**</span></span>](registrationtrigger-delay.md)<br/>               | <span data-ttu-id="08dfd-117">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08dfd-117">Read/write</span></span><br/> | <span data-ttu-id="08dfd-118">Ruft die Zeitspanne zwischen dem Registrieren der Aufgabe und dem Start der Aufgabe ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="08dfd-118">Gets or sets the amount of time between when the task is registered and when the task is started.</span></span><br/>                                                                                |
| [<span data-ttu-id="08dfd-119">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="08dfd-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="08dfd-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08dfd-120">Read/write</span></span><br/> | <span data-ttu-id="08dfd-121">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="08dfd-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="08dfd-122">Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="08dfd-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="08dfd-123">**Endgrenze**</span><span class="sxs-lookup"><span data-stu-id="08dfd-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="08dfd-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08dfd-124">Read/write</span></span><br/> | <span data-ttu-id="08dfd-125">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="08dfd-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="08dfd-126">Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="08dfd-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="08dfd-127">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="08dfd-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="08dfd-128">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="08dfd-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="08dfd-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08dfd-129">Read/write</span></span><br/> | <span data-ttu-id="08dfd-130">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="08dfd-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="08dfd-131">Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="08dfd-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="08dfd-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="08dfd-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="08dfd-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08dfd-133">Read/write</span></span><br/> | <span data-ttu-id="08dfd-134">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="08dfd-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="08dfd-135">Ruft den Bezeichner für den-Typ ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="08dfd-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="08dfd-136">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="08dfd-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="08dfd-137">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08dfd-137">Read/write</span></span><br/> | <span data-ttu-id="08dfd-138">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="08dfd-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="08dfd-139">Ruft ab oder legt fest, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="08dfd-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="08dfd-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="08dfd-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="08dfd-141">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08dfd-141">Read/write</span></span><br/> | <span data-ttu-id="08dfd-142">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="08dfd-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="08dfd-143">Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="08dfd-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="08dfd-144">**type**</span><span class="sxs-lookup"><span data-stu-id="08dfd-144">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="08dfd-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08dfd-145">Read-only</span></span><br/>  | <span data-ttu-id="08dfd-146">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="08dfd-146">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="08dfd-147">Ruft den Typ des Auslösers ab.</span><span class="sxs-lookup"><span data-stu-id="08dfd-147">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="08dfd-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08dfd-148">Remarks</span></span>

<span data-ttu-id="08dfd-149">Wenn Sie einen eigenen XML-Code für eine Aufgabe erstellen, wird mit dem [**Registration-Auslöserelement**](taskschedulerschema-registrationtrigger-triggergroup-element.md) des Taskplaner Schemas ein Registrierungs--Vorgang angegeben.</span><span class="sxs-lookup"><span data-stu-id="08dfd-149">When creating your own XML for a task, a registration trigger is specified using the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="08dfd-150">Wenn eine Aufgabe mit einem verzögerten Registrierungs Ausfall registriert ist und der Computer, auf dem der Task registriert ist, während der Verzögerung heruntergefahren oder neu gestartet wird, bevor der Task ausgeführt wird, wird der Task nicht ausgeführt, und die Verzögerung geht verloren.</span><span class="sxs-lookup"><span data-stu-id="08dfd-150">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="examples"></a><span data-ttu-id="08dfd-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08dfd-151">Examples</span></span>

<span data-ttu-id="08dfd-152">Weitere Informationen und ein Codebeispiel für dieses Skript Objekt finden Sie unter [Beispiel für Registrierungs Beispiel (Skripterstellung)](registration-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="08dfd-152">For more information and a code example for this scripting object, see [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="08dfd-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08dfd-153">Requirements</span></span>



| <span data-ttu-id="08dfd-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08dfd-154">Requirement</span></span> | <span data-ttu-id="08dfd-155">Wert</span><span class="sxs-lookup"><span data-stu-id="08dfd-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08dfd-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08dfd-156">Minimum supported client</span></span><br/> | <span data-ttu-id="08dfd-157">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08dfd-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="08dfd-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08dfd-158">Minimum supported server</span></span><br/> | <span data-ttu-id="08dfd-159">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08dfd-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08dfd-160">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="08dfd-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="08dfd-161"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="08dfd-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="08dfd-162">DLL</span><span class="sxs-lookup"><span data-stu-id="08dfd-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08dfd-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08dfd-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08dfd-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08dfd-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08dfd-165">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="08dfd-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="08dfd-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="08dfd-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="08dfd-167">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="08dfd-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





