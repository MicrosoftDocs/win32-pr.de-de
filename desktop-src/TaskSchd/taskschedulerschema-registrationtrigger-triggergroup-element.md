---
title: Registrationtrigger (triggergroup)-Element
description: Gibt einen-Typ an, der einen Task startet, wenn der Task registriert wird.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- Registrierungs-auslöserTaskplaner, XML-Element
- Registration-Auslöserelement Taskplaner
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90960f81d252b0b0a8d1de3ab5cc1465003467a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344688"
---
# <a name="registrationtrigger-triggergroup-element"></a><span data-ttu-id="c068d-105">Registrationtrigger (triggergroup)-Element</span><span class="sxs-lookup"><span data-stu-id="c068d-105">RegistrationTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="c068d-106">Gibt einen-Typ an, der einen Task startet, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="c068d-106">Specifies a trigger that starts a task when the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

<span data-ttu-id="c068d-107">Das **registrationtrigger** -Element wird durch den komplexen Typ [**registrationtriggertype**](taskschedulerschema-registrationtriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="c068d-107">The **RegistrationTrigger** element is defined by the [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c068d-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="c068d-108">Parent element</span></span>



| <span data-ttu-id="c068d-109">Element</span><span class="sxs-lookup"><span data-stu-id="c068d-109">Element</span></span>                                                           | <span data-ttu-id="c068d-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="c068d-110">Derived from</span></span>                                                         | <span data-ttu-id="c068d-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c068d-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="c068d-112">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="c068d-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="c068d-113">**triggerstype**</span><span class="sxs-lookup"><span data-stu-id="c068d-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="c068d-114">Gibt die Trigger an, die den Task starten.</span><span class="sxs-lookup"><span data-stu-id="c068d-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="c068d-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c068d-115">Child elements</span></span>



| <span data-ttu-id="c068d-116">Element</span><span class="sxs-lookup"><span data-stu-id="c068d-116">Element</span></span>                                                                                                        | <span data-ttu-id="c068d-117">type</span><span class="sxs-lookup"><span data-stu-id="c068d-117">Type</span></span>                                                                     | <span data-ttu-id="c068d-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c068d-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c068d-119">**Delay (registrationtriggertype)**</span><span class="sxs-lookup"><span data-stu-id="c068d-119">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                   | <span data-ttu-id="c068d-120">duration</span><span class="sxs-lookup"><span data-stu-id="c068d-120">duration</span></span>                                                                 | <span data-ttu-id="c068d-121">Gibt die Zeitspanne zwischen dem Registrieren der Aufgabe und dem Start der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="c068d-121">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/>                          |
| [<span data-ttu-id="c068d-122">**Aktiviert (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="c068d-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="c068d-123">boolean</span><span class="sxs-lookup"><span data-stu-id="c068d-123">boolean</span></span>                                                                  | <span data-ttu-id="c068d-124">Gibt an, dass der-Wert aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c068d-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="c068d-125">**Endboundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="c068d-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="c068d-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="c068d-126">dateTime</span></span>                                                                 | <span data-ttu-id="c068d-127">Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="c068d-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="c068d-128">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="c068d-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="c068d-129">**Executiontimelimit (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="c068d-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="c068d-130">duration</span><span class="sxs-lookup"><span data-stu-id="c068d-130">duration</span></span>                                                                 | <span data-ttu-id="c068d-131">Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c068d-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="c068d-132">**Wiederholung (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="c068d-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="c068d-133">**Wiederholungstyp**</span><span class="sxs-lookup"><span data-stu-id="c068d-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="c068d-134">Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="c068d-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="c068d-135">**StartBoundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="c068d-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="c068d-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="c068d-136">dateTime</span></span>                                                                 | <span data-ttu-id="c068d-137">Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="c068d-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="c068d-138">Attributes</span><span class="sxs-lookup"><span data-stu-id="c068d-138">Attributes</span></span>



| <span data-ttu-id="c068d-139">Name</span><span class="sxs-lookup"><span data-stu-id="c068d-139">Name</span></span> | <span data-ttu-id="c068d-140">type</span><span class="sxs-lookup"><span data-stu-id="c068d-140">Type</span></span> | <span data-ttu-id="c068d-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c068d-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="c068d-142">Id</span><span class="sxs-lookup"><span data-stu-id="c068d-142">Id</span></span>   | <span data-ttu-id="c068d-143">id</span><span class="sxs-lookup"><span data-stu-id="c068d-143">ID</span></span>   | <span data-ttu-id="c068d-144">Der Bezeichner des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="c068d-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c068d-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c068d-145">Remarks</span></span>

<span data-ttu-id="c068d-146">Bei der Entwicklung von Skripts wird ein Registrierungs-Assistent mithilfe des [**Registration-auslöserobjekts**](registrationtrigger.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="c068d-146">For scripting development, a registration trigger is specified using the [**RegistrationTrigger**](registrationtrigger.md) object.</span></span>

<span data-ttu-id="c068d-147">Bei der C++-Entwicklung wird ein Registrierungs-Assistent mithilfe der [**iregistration-auslöserschnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) angegeben.</span><span class="sxs-lookup"><span data-stu-id="c068d-147">For C++ development, a registration trigger is specified using the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface.</span></span>

<span data-ttu-id="c068d-148">Die oben aufgeführten untergeordneten Elemente werden von den komplexen Elementtypen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) und [**registrationtriggertype**](taskschedulerschema-registrationtriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="c068d-148">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="c068d-149">Diese Elemente müssen in der unten gezeigten Sequenz hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c068d-149">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="c068d-150">**StartBoundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="c068d-150">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="c068d-151">**Endboundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="c068d-151">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="c068d-152">**Aktiviert (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="c068d-152">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="c068d-153">**Wiederholung (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="c068d-153">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="c068d-154">**Executiontimelimit (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="c068d-154">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="c068d-155">**Delay (registrationtriggertype)**</span><span class="sxs-lookup"><span data-stu-id="c068d-155">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a><span data-ttu-id="c068d-156">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c068d-156">Examples</span></span>

<span data-ttu-id="c068d-157">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Start--Auslösers angibt, finden Sie unter [Beispiel für Registrierungs Beispiel (XML)](registration-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="c068d-157">For a complete example of the XML for a task that specifies a boot trigger, see [Registration Trigger Example (XML)](registration-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c068d-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c068d-158">Requirements</span></span>



| <span data-ttu-id="c068d-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c068d-159">Requirement</span></span> | <span data-ttu-id="c068d-160">Wert</span><span class="sxs-lookup"><span data-stu-id="c068d-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c068d-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c068d-161">Minimum supported client</span></span><br/> | <span data-ttu-id="c068d-162">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c068d-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c068d-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c068d-163">Minimum supported server</span></span><br/> | <span data-ttu-id="c068d-164">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c068d-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c068d-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c068d-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c068d-166">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="c068d-166">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c068d-167">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="c068d-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





