---
title: Idletrigger-Element (triggergroup)
description: Gibt einen-Auslösers an, der einen Task startet, wenn der Computer in den Leerlauf wechselt.
ms.assetid: c3e317b5-d1a7-46de-ace5-e066452583d3
keywords:
- Leerlauf-, XML-Element
- Idle-Auslöserelement Taskplaner
topic_type:
- apiref
api_name:
- IdleTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 221d272145670b9514cde5ffbe8b02e5ddcd6e0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040282"
---
# <a name="idletrigger-triggergroup-element"></a><span data-ttu-id="f1ff7-105">Idletrigger-Element (triggergroup)</span><span class="sxs-lookup"><span data-stu-id="f1ff7-105">IdleTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="f1ff7-106">Gibt einen-Auslösers an, der einen Task startet, wenn der Computer in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-106">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span> <span data-ttu-id="f1ff7-107">Informationen zu Bedingungen im Leerlauf finden Sie unter [Aufgaben im Leerlauf](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="f1ff7-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleTrigger"
    type="idleTriggerType"
 />
```

<span data-ttu-id="f1ff7-108">Das **idletrigger** -Element wird von [**triggergroup**](taskschedulerschema-triggergroup-group.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-108">The **IdleTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="f1ff7-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f1ff7-109">Parent element</span></span>



| <span data-ttu-id="f1ff7-110">Element</span><span class="sxs-lookup"><span data-stu-id="f1ff7-110">Element</span></span>                                                           | <span data-ttu-id="f1ff7-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="f1ff7-111">Derived from</span></span>                                                         | <span data-ttu-id="f1ff7-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1ff7-112">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f1ff7-113">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="f1ff7-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="f1ff7-114">**triggerstype**</span><span class="sxs-lookup"><span data-stu-id="f1ff7-114">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="f1ff7-115">Gibt die Trigger an, die den Task starten.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-115">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f1ff7-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1ff7-116">Child elements</span></span>



| <span data-ttu-id="f1ff7-117">Element</span><span class="sxs-lookup"><span data-stu-id="f1ff7-117">Element</span></span>                                                                                                        | <span data-ttu-id="f1ff7-118">type</span><span class="sxs-lookup"><span data-stu-id="f1ff7-118">Type</span></span>                                                                     | <span data-ttu-id="f1ff7-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1ff7-119">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1ff7-120">**Aktiviert (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="f1ff7-120">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="f1ff7-121">boolean</span><span class="sxs-lookup"><span data-stu-id="f1ff7-121">boolean</span></span>                                                                  | <span data-ttu-id="f1ff7-122">Gibt an, dass der-Wert aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-122">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="f1ff7-123">**Endboundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="f1ff7-123">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="f1ff7-124">dateTime</span><span class="sxs-lookup"><span data-stu-id="f1ff7-124">dateTime</span></span>                                                                 | <span data-ttu-id="f1ff7-125">Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-125">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="f1ff7-126">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="f1ff7-127">**Executiontimelimit (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="f1ff7-127">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="f1ff7-128">duration</span><span class="sxs-lookup"><span data-stu-id="f1ff7-128">duration</span></span>                                                                 | <span data-ttu-id="f1ff7-129">Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-129">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="f1ff7-130">**Wiederholung (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="f1ff7-130">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="f1ff7-131">**Wiederholungstyp**</span><span class="sxs-lookup"><span data-stu-id="f1ff7-131">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="f1ff7-132">Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-132">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="f1ff7-133">**StartBoundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="f1ff7-133">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="f1ff7-134">dateTime</span><span class="sxs-lookup"><span data-stu-id="f1ff7-134">dateTime</span></span>                                                                 | <span data-ttu-id="f1ff7-135">Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-135">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="f1ff7-136">Attributes</span><span class="sxs-lookup"><span data-stu-id="f1ff7-136">Attributes</span></span>



| <span data-ttu-id="f1ff7-137">Name</span><span class="sxs-lookup"><span data-stu-id="f1ff7-137">Name</span></span> | <span data-ttu-id="f1ff7-138">type</span><span class="sxs-lookup"><span data-stu-id="f1ff7-138">Type</span></span>   | <span data-ttu-id="f1ff7-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1ff7-139">Description</span></span>                               |
|------|--------|-------------------------------------------|
| <span data-ttu-id="f1ff7-140">Id</span><span class="sxs-lookup"><span data-stu-id="f1ff7-140">Id</span></span>   | <span data-ttu-id="f1ff7-141">string</span><span class="sxs-lookup"><span data-stu-id="f1ff7-141">string</span></span> | <span data-ttu-id="f1ff7-142">Der Bezeichner des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-142">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f1ff7-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1ff7-143">Remarks</span></span>

<span data-ttu-id="f1ff7-144">Bei der Skripterstellung wird ein Leerlauf--Auslösung mithilfe des [**Idle-auslöserobjekts**](idletrigger.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-144">For scripting development, an idle trigger is specified using the [**IdleTrigger**](idletrigger.md) object.</span></span>

<span data-ttu-id="f1ff7-145">Bei der C++-Entwicklung wird mithilfe der [**iidletimeout**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) -Schnittstelle ein Leerlauf-Auslösers angegeben.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-145">For C++ development, an idle trigger is specified using the [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) interface.</span></span>

<span data-ttu-id="f1ff7-146">Die oben aufgeführten untergeordneten Elemente werden von den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Elementtypen definiert.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="f1ff7-147">Diese Elemente müssen in der unten gezeigten Sequenz hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="f1ff7-148">**StartBoundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="f1ff7-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="f1ff7-149">**Endboundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="f1ff7-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="f1ff7-150">**Aktiviert (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="f1ff7-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="f1ff7-151">**Wiederholung (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="f1ff7-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="f1ff7-152">**Executiontimelimit (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="f1ff7-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="f1ff7-153">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1ff7-153">Examples</span></span>

<span data-ttu-id="f1ff7-154">Der folgende XML-Code definiert einen Leerlauf-Auslösung.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-154">The following XML defines an idle trigger.</span></span>


```XML
<IdleTrigger>
    <StartBoundary>2005-01-01T00:08:00</StartBoundary>
    <EndBounadry>2007-01-01T00:08:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
</IdleTrigger>
```



## <a name="requirements"></a><span data-ttu-id="f1ff7-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1ff7-155">Requirements</span></span>



| <span data-ttu-id="f1ff7-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1ff7-156">Requirement</span></span> | <span data-ttu-id="f1ff7-157">Wert</span><span class="sxs-lookup"><span data-stu-id="f1ff7-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1ff7-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1ff7-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f1ff7-159">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1ff7-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f1ff7-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1ff7-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f1ff7-161">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1ff7-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1ff7-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1ff7-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ff7-163">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="f1ff7-163">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f1ff7-164">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="f1ff7-164">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

