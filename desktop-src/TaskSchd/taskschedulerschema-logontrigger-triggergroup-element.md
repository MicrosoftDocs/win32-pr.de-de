---
title: Logontrigger-Element (triggergroup)
description: Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.
ms.assetid: c3edee50-e053-4813-a1b2-bf1e7b575ff7
keywords:
- Logon-, XML-Element
- Logon-Auslöserelement Taskplaner
topic_type:
- apiref
api_name:
- LogonTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89d0e593277f1c854850017412b49c22d8ac436
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340547"
---
# <a name="logontrigger-triggergroup-element"></a><span data-ttu-id="05efd-105">Logontrigger-Element (triggergroup)</span><span class="sxs-lookup"><span data-stu-id="05efd-105">LogonTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="05efd-106">Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="05efd-106">Specifies a trigger that starts a task when a user logs on.</span></span>

``` syntax
<xs:element name="LogonTrigger"
    type="logonTriggerType"
 />
```

<span data-ttu-id="05efd-107">Das **logontrigger** -Element wird von [**triggergroup**](taskschedulerschema-triggergroup-group.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="05efd-107">The **LogonTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="05efd-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="05efd-108">Parent element</span></span>



| <span data-ttu-id="05efd-109">Element</span><span class="sxs-lookup"><span data-stu-id="05efd-109">Element</span></span>                                                           | <span data-ttu-id="05efd-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="05efd-110">Derived from</span></span>                                                         | <span data-ttu-id="05efd-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05efd-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="05efd-112">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="05efd-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="05efd-113">**triggerstype**</span><span class="sxs-lookup"><span data-stu-id="05efd-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="05efd-114">Gibt die Trigger an, die den Task starten.</span><span class="sxs-lookup"><span data-stu-id="05efd-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="05efd-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05efd-115">Child elements</span></span>



| <span data-ttu-id="05efd-116">Element</span><span class="sxs-lookup"><span data-stu-id="05efd-116">Element</span></span>                                                                                                        | <span data-ttu-id="05efd-117">type</span><span class="sxs-lookup"><span data-stu-id="05efd-117">Type</span></span>                                                                     | <span data-ttu-id="05efd-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05efd-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05efd-119">**Delay (logontriggertype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-119">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)                         | <span data-ttu-id="05efd-120">duration</span><span class="sxs-lookup"><span data-stu-id="05efd-120">duration</span></span>                                                                 | <span data-ttu-id="05efd-121">Zeitraum zwischen dem Zeitpunkt, an dem sich der Benutzer anmeldet, und dem Start der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="05efd-121">Amount of time between when the user logs on and when the task is started.</span></span><br/>                                              |
| [<span data-ttu-id="05efd-122">**Aktiviert (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="05efd-123">boolean</span><span class="sxs-lookup"><span data-stu-id="05efd-123">boolean</span></span>                                                                  | <span data-ttu-id="05efd-124">Gibt an, dass der-Wert aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="05efd-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="05efd-125">**Endboundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="05efd-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="05efd-126">dateTime</span></span>                                                                 | <span data-ttu-id="05efd-127">Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="05efd-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="05efd-128">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="05efd-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="05efd-129">**Executiontimelimit (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="05efd-130">duration</span><span class="sxs-lookup"><span data-stu-id="05efd-130">duration</span></span>                                                                 | <span data-ttu-id="05efd-131">Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="05efd-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="05efd-132">**Wiederholung (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="05efd-133">**Wiederholungstyp**</span><span class="sxs-lookup"><span data-stu-id="05efd-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="05efd-134">Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="05efd-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="05efd-135">**StartBoundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="05efd-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="05efd-136">dateTime</span></span>                                                                 | <span data-ttu-id="05efd-137">Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="05efd-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="05efd-138">**UserID (logontriggertype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-138">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)                       | <span data-ttu-id="05efd-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="05efd-139">string</span></span>                                                                   | <span data-ttu-id="05efd-140">Der Bezeichner des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="05efd-140">Identifier of the user.</span></span> <span data-ttu-id="05efd-141">Der Task wird gestartet, wenn sich dieser Benutzer auf dem Computer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="05efd-141">The task is started when this user logs onto the computer.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="05efd-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05efd-142">Remarks</span></span>

<span data-ttu-id="05efd-143">Bei der Skripterstellung wird ein LOGON-Ereignis mithilfe des [**Logon-auslöserobjekts**](logontrigger.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="05efd-143">For scripting development, a logon trigger is specified using the [**LogonTrigger**](logontrigger.md) object.</span></span>

<span data-ttu-id="05efd-144">Bei der C++-Entwicklung wird ein LOGON-Ereignis mithilfe der [**iLogon-**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) Schnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="05efd-144">For C++ development, a logon trigger is specified using the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface.</span></span>

<span data-ttu-id="05efd-145">Die oben aufgeführten untergeordneten Elemente werden von den komplexen Elementtypen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) und [**logontriggertype**](taskschedulerschema-logontriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="05efd-145">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="05efd-146">Diese Elemente müssen in der unten gezeigten Sequenz hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="05efd-146">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="05efd-147">**StartBoundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-147">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="05efd-148">**Endboundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-148">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="05efd-149">**Aktiviert (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-149">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="05efd-150">**Wiederholung (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-150">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="05efd-151">**Executiontimelimit (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-151">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="05efd-152">**UserID (logontriggertype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-152">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)
-   [<span data-ttu-id="05efd-153">**Delay (logontriggertype)**</span><span class="sxs-lookup"><span data-stu-id="05efd-153">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)

### <a name="attributes"></a><span data-ttu-id="05efd-154">Attribute</span><span class="sxs-lookup"><span data-stu-id="05efd-154">Attributes</span></span>

<span data-ttu-id="05efd-155">Das unten aufgeführte Attribut wird von den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Elementtypen definiert.</span><span class="sxs-lookup"><span data-stu-id="05efd-155">The attribute listed below is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span>

-   <span data-ttu-id="05efd-156">ID: der Bezeichner des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="05efd-156">Id: Identifier of the trigger.</span></span>

## <a name="examples"></a><span data-ttu-id="05efd-157">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05efd-157">Examples</span></span>

<span data-ttu-id="05efd-158">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Logon-Auslösers verwendet, finden Sie unter [Logon-Beispiel Beispiel (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="05efd-158">For a complete example of the XML for a task that uses a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05efd-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05efd-159">Requirements</span></span>



| <span data-ttu-id="05efd-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05efd-160">Requirement</span></span> | <span data-ttu-id="05efd-161">Wert</span><span class="sxs-lookup"><span data-stu-id="05efd-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05efd-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05efd-162">Minimum supported client</span></span><br/> | <span data-ttu-id="05efd-163">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05efd-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05efd-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05efd-164">Minimum supported server</span></span><br/> | <span data-ttu-id="05efd-165">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05efd-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05efd-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05efd-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05efd-167">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="05efd-167">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





