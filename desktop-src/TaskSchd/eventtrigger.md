---
title: EventTrigger-Objekt (Windows. UI. XAML. h)
description: Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn ein System Ereignis auftritt.
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- Taskplaner des Ereignis Auslösers, Objekt
- EventTrigger-Objekt Taskplaner
- EventTrigger-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- EventTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b80bc8336c4756dfedc041aea40f79fd5f868e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518605"
---
# <a name="eventtrigger-object"></a><span data-ttu-id="a1369-106">EventTrigger-Objekt</span><span class="sxs-lookup"><span data-stu-id="a1369-106">EventTrigger object</span></span>

<span data-ttu-id="a1369-107">Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn ein System Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="a1369-107">Scripting object that represents a trigger that starts a task when a system event occurs.</span></span>

## <a name="members"></a><span data-ttu-id="a1369-108">Member</span><span class="sxs-lookup"><span data-stu-id="a1369-108">Members</span></span>

<span data-ttu-id="a1369-109">Das **EventTrigger** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a1369-109">The **EventTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="a1369-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1369-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1369-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1369-111">Properties</span></span>

<span data-ttu-id="a1369-112">Das **EventTrigger** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1369-112">The **EventTrigger** object has these properties.</span></span>



| <span data-ttu-id="a1369-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a1369-113">Property</span></span>                                                            | <span data-ttu-id="a1369-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="a1369-114">Access type</span></span>           | <span data-ttu-id="a1369-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1369-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1369-116">**Verzögern**</span><span class="sxs-lookup"><span data-stu-id="a1369-116">**Delay**</span></span>](eventtrigger-delay.md)<br/>                      | <span data-ttu-id="a1369-117">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a1369-117">Read/write</span></span><br/> | <span data-ttu-id="a1369-118">Ruft einen Wert ab oder legt einen Wert fest, der die Zeitspanne zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe angibt.</span><span class="sxs-lookup"><span data-stu-id="a1369-118">Gets or sets a value that indicates the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="a1369-119">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="a1369-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="a1369-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a1369-120">Read/write</span></span><br/> | <span data-ttu-id="a1369-121">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1369-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="a1369-122">Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="a1369-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="a1369-123">**Endgrenze**</span><span class="sxs-lookup"><span data-stu-id="a1369-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="a1369-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a1369-124">Read/write</span></span><br/> | <span data-ttu-id="a1369-125">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1369-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="a1369-126">Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="a1369-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="a1369-127">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="a1369-127">The trigger cannot start the task after it is deactivated.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="a1369-128">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="a1369-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="a1369-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a1369-129">Read/write</span></span><br/> | <span data-ttu-id="a1369-130">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1369-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="a1369-131">Ruft die maximale Zeitspanne ab, die der von diesem-Vorgang gestartete Task ausgeführt werden darf, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="a1369-131">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                                                                                                                                                                                                                       |
| [<span data-ttu-id="a1369-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="a1369-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="a1369-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a1369-133">Read/write</span></span><br/> | <span data-ttu-id="a1369-134">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1369-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="a1369-135">Ruft den Bezeichner für den-Typ ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="a1369-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="a1369-136">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="a1369-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="a1369-137">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a1369-137">Read/write</span></span><br/> | <span data-ttu-id="a1369-138">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1369-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="a1369-139">Ruft ab oder legt fest, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="a1369-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>                                                                                                                                                                                                       |
| [<span data-ttu-id="a1369-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="a1369-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="a1369-141">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a1369-141">Read/write</span></span><br/> | <span data-ttu-id="a1369-142">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1369-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="a1369-143">Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="a1369-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="a1369-144">**Abonnement**</span><span class="sxs-lookup"><span data-stu-id="a1369-144">**Subscription**</span></span>](eventtrigger-subscription.md)<br/>        | <span data-ttu-id="a1369-145">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a1369-145">Read/write</span></span><br/> | <span data-ttu-id="a1369-146">Ruft die XPath-Abfrage Zeichenfolge ab, die das Ereignis identifiziert, das den-Triggers auslöst</span><span class="sxs-lookup"><span data-stu-id="a1369-146">Gets or sets the XPath query string that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="a1369-147">**type**</span><span class="sxs-lookup"><span data-stu-id="a1369-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="a1369-148">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1369-148">Read-only</span></span><br/>  | <span data-ttu-id="a1369-149">Wird vom- [**Auslöserobjekt**](trigger.md) geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1369-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="a1369-150">Ruft den Typ des Auslösers ab.</span><span class="sxs-lookup"><span data-stu-id="a1369-150">Gets the type of the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="a1369-151">**Valuequeries**</span><span class="sxs-lookup"><span data-stu-id="a1369-151">**ValueQueries**</span></span>](eventtrigger-valuequeries.md)<br/>        | <span data-ttu-id="a1369-152">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a1369-152">Read/write</span></span><br/> | <span data-ttu-id="a1369-153">Ruft eine Auflistung von benannten XPath-Abfragen ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="a1369-153">Gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="a1369-154">Jede Abfrage in der Auflistung wird auf das letzte übereinstimmende Ereignis-XML angewendet, das von der Abonnement Abfrage zurückgegeben wird, die in der [**Abonnement**](eventtrigger-subscription.md) -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a1369-154">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span> <span data-ttu-id="a1369-155">Der Name der Abfrage kann als Variable in der Nachricht einer [**showmessageaction**](showmessageaction.md) -Aktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1369-155">The name of the query can be used as a variable in the message of a [**ShowMessageAction**](showmessageaction.md) action.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a1369-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1369-156">Remarks</span></span>

<span data-ttu-id="a1369-157">Es können maximal 500 Tasks mit Ereignis Abonnements erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a1369-157">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="a1369-158">Ein Ereignis Abonnement, das Abfragen für eine Vielzahl von Ereignissen verwendet, kann verwendet werden, um eine Aufgabe zu initiieren, die dieselbe Aktion als Reaktion auf die protokollierten Ereignisse verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1369-158">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="a1369-159">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird ein Ereignis Trigger mit dem [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="a1369-159">When reading or writing your own XML for a task, an event trigger is specified using the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="a1369-160">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1369-160">Examples</span></span>

<span data-ttu-id="a1369-161">Weitere Informationen und ein Codebeispiel für dieses Skript Objekt finden Sie unter [Event-auslöserbeispiel (Skripterstellung)](/previous-versions//aa446887(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a1369-161">For more information and a code example for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1369-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1369-162">Requirements</span></span>



| <span data-ttu-id="a1369-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1369-163">Requirement</span></span> | <span data-ttu-id="a1369-164">Wert</span><span class="sxs-lookup"><span data-stu-id="a1369-164">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1369-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1369-165">Minimum supported client</span></span><br/> | <span data-ttu-id="a1369-166">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1369-166">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a1369-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1369-167">Minimum supported server</span></span><br/> | <span data-ttu-id="a1369-168">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1369-168">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a1369-169">Header</span><span class="sxs-lookup"><span data-stu-id="a1369-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1369-170"><dt>Windows. UI. XAML. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1369-170"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="a1369-171">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a1369-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="a1369-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a1369-172"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="a1369-173">DLL</span><span class="sxs-lookup"><span data-stu-id="a1369-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1369-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1369-174"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="a1369-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1369-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1369-176">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="a1369-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="a1369-177">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="a1369-177">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="a1369-178">**TriggerCollection. Create**</span><span class="sxs-lookup"><span data-stu-id="a1369-178">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

