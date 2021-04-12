---
title: Event Trigger-Element (triggergroup)
description: Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- Taskplaner des Ereignis Auslösers, Element
- EventTrigger-Element Taskplaner
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cecf46250fface0f716adbf287cda3269b86f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478180"
---
# <a name="eventtrigger-triggergroup-element"></a><span data-ttu-id="27e42-105">Event Trigger-Element (triggergroup)</span><span class="sxs-lookup"><span data-stu-id="27e42-105">EventTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="27e42-106">Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="27e42-106">Specifies a trigger that starts a task when a system event occurs.</span></span>

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

<span data-ttu-id="27e42-107">Das **EventTrigger** -Element wird von [**triggergroup**](taskschedulerschema-triggergroup-group.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="27e42-107">The **EventTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="27e42-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="27e42-108">Parent element</span></span>



| <span data-ttu-id="27e42-109">Element</span><span class="sxs-lookup"><span data-stu-id="27e42-109">Element</span></span>                                                           | <span data-ttu-id="27e42-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="27e42-110">Derived from</span></span>                                                         | <span data-ttu-id="27e42-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27e42-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="27e42-112">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="27e42-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="27e42-113">**triggerstype**</span><span class="sxs-lookup"><span data-stu-id="27e42-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="27e42-114">Gibt die Trigger an, die den Task starten.</span><span class="sxs-lookup"><span data-stu-id="27e42-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="27e42-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27e42-115">Child elements</span></span>



| <span data-ttu-id="27e42-116">Element</span><span class="sxs-lookup"><span data-stu-id="27e42-116">Element</span></span>                                                                                              | <span data-ttu-id="27e42-117">type</span><span class="sxs-lookup"><span data-stu-id="27e42-117">Type</span></span>                                                                     | <span data-ttu-id="27e42-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27e42-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27e42-119">**Delay (eventtriggertype)**</span><span class="sxs-lookup"><span data-stu-id="27e42-119">**Delay (eventTriggerType)**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="27e42-120">duration</span><span class="sxs-lookup"><span data-stu-id="27e42-120">duration</span></span>                                                                 | <span data-ttu-id="27e42-121">Gibt die Zeitspanne zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="27e42-121">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                |
| [<span data-ttu-id="27e42-122">**Aktiviert (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="27e42-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)             | <span data-ttu-id="27e42-123">boolean</span><span class="sxs-lookup"><span data-stu-id="27e42-123">boolean</span></span>                                                                  | <span data-ttu-id="27e42-124">Gibt an, dass der-Wert aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="27e42-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="27e42-125">**Endboundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="27e42-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)     | <span data-ttu-id="27e42-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="27e42-126">dateTime</span></span>                                                                 | <span data-ttu-id="27e42-127">Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="27e42-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="27e42-128">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="27e42-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="27e42-129">**Wiederholung (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="27e42-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)       | [<span data-ttu-id="27e42-130">**Wiederholungstyp**</span><span class="sxs-lookup"><span data-stu-id="27e42-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="27e42-131">Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="27e42-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="27e42-132">**StartBoundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="27e42-132">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md) | <span data-ttu-id="27e42-133">dateTime</span><span class="sxs-lookup"><span data-stu-id="27e42-133">dateTime</span></span>                                                                 | <span data-ttu-id="27e42-134">Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="27e42-134">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="27e42-135">**Abonnement (eventtriggertype)**</span><span class="sxs-lookup"><span data-stu-id="27e42-135">**Subscription (eventTriggerType)**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | <span data-ttu-id="27e42-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="27e42-136">string</span></span>                                                                   | <span data-ttu-id="27e42-137">Gibt die XPath-Abfrage an, die das Ereignis identifiziert, das den-Triggern auslöst.</span><span class="sxs-lookup"><span data-stu-id="27e42-137">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                             |



## <a name="attributes"></a><span data-ttu-id="27e42-138">Attributes</span><span class="sxs-lookup"><span data-stu-id="27e42-138">Attributes</span></span>



| <span data-ttu-id="27e42-139">Name</span><span class="sxs-lookup"><span data-stu-id="27e42-139">Name</span></span> | <span data-ttu-id="27e42-140">type</span><span class="sxs-lookup"><span data-stu-id="27e42-140">Type</span></span> | <span data-ttu-id="27e42-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27e42-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="27e42-142">Id</span><span class="sxs-lookup"><span data-stu-id="27e42-142">Id</span></span>   | <span data-ttu-id="27e42-143">id</span><span class="sxs-lookup"><span data-stu-id="27e42-143">ID</span></span>   | <span data-ttu-id="27e42-144">Der Bezeichner des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="27e42-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="27e42-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27e42-145">Remarks</span></span>

<span data-ttu-id="27e42-146">Es können maximal 500 Tasks mit Ereignis Abonnements erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="27e42-146">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="27e42-147">Ein Ereignis Abonnement, das Abfragen für eine Vielzahl von Ereignissen verwendet, kann verwendet werden, um eine Aufgabe zu initiieren, die dieselbe Aktion als Reaktion auf die protokollierten Ereignisse verwendet.</span><span class="sxs-lookup"><span data-stu-id="27e42-147">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="27e42-148">Bei der Skript Entwicklung wird ein Ereignis Trigger durch das [**EventTrigger**](eventtrigger.md) -Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="27e42-148">For script development, an event trigger is defined by the [**EventTrigger**](eventtrigger.md) object.</span></span>

<span data-ttu-id="27e42-149">Bei der C++-Entwicklung wird ein Ereignis-von der [**IEvent-auslöserschnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) definiert.</span><span class="sxs-lookup"><span data-stu-id="27e42-149">For C++ development, an event trigger is defined by the [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="27e42-150">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27e42-150">Examples</span></span>

<span data-ttu-id="27e42-151">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Ereignis Auslösers verwendet, finden Sie unter [Event-auslöserbeispiel (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="27e42-151">For a complete example of the XML for a task that uses an event trigger, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="27e42-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27e42-152">Requirements</span></span>



| <span data-ttu-id="27e42-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27e42-153">Requirement</span></span> | <span data-ttu-id="27e42-154">Wert</span><span class="sxs-lookup"><span data-stu-id="27e42-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="27e42-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27e42-155">Minimum supported client</span></span><br/> | <span data-ttu-id="27e42-156">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27e42-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="27e42-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27e42-157">Minimum supported server</span></span><br/> | <span data-ttu-id="27e42-158">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27e42-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27e42-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27e42-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27e42-160">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="27e42-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

