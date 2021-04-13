---
title: Boottrigger-Element (triggergroup)
description: Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- Taskplaner des Start Auslösers, XML-Element
- Boottrigger-Element Taskplaner
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb6ccf590893e19340662fd4c47e4aa68047b29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340948"
---
# <a name="boottrigger-triggergroup-element"></a><span data-ttu-id="a7d08-105">Boottrigger-Element (triggergroup)</span><span class="sxs-lookup"><span data-stu-id="a7d08-105">BootTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="a7d08-106">Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a7d08-106">Specifies a trigger that starts a task when the system is booted.</span></span>

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

<span data-ttu-id="a7d08-107">Das **boottrigger** -Element wird durch den komplexen [**boottriggertype**](taskschedulerschema-boottriggertype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="a7d08-107">The **BootTrigger** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a7d08-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="a7d08-108">Parent element</span></span>



| <span data-ttu-id="a7d08-109">Element</span><span class="sxs-lookup"><span data-stu-id="a7d08-109">Element</span></span>                                                           | <span data-ttu-id="a7d08-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="a7d08-110">Derived from</span></span>                                                         | <span data-ttu-id="a7d08-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7d08-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="a7d08-112">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="a7d08-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="a7d08-113">**triggerstype**</span><span class="sxs-lookup"><span data-stu-id="a7d08-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="a7d08-114">Gibt die Trigger an, die den Task starten.</span><span class="sxs-lookup"><span data-stu-id="a7d08-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="a7d08-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7d08-115">Child elements</span></span>



| <span data-ttu-id="a7d08-116">Element</span><span class="sxs-lookup"><span data-stu-id="a7d08-116">Element</span></span>                                                                                                        | <span data-ttu-id="a7d08-117">type</span><span class="sxs-lookup"><span data-stu-id="a7d08-117">Type</span></span>                                                                     | <span data-ttu-id="a7d08-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7d08-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7d08-119">**Verzögerung (boottriggertype)**</span><span class="sxs-lookup"><span data-stu-id="a7d08-119">**Delay (bootTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                           | <span data-ttu-id="a7d08-120">duration</span><span class="sxs-lookup"><span data-stu-id="a7d08-120">duration</span></span>                                                                 | <span data-ttu-id="a7d08-121">Gibt den Zeitraum zwischen dem Start des Systems und dem Start der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="a7d08-121">Specifies the amount of time between when the system is booted and when the task is started.</span></span><br/>                            |
| [<span data-ttu-id="a7d08-122">**Aktiviert (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="a7d08-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="a7d08-123">boolean</span><span class="sxs-lookup"><span data-stu-id="a7d08-123">boolean</span></span>                                                                  | <span data-ttu-id="a7d08-124">Gibt an, dass der-Wert aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a7d08-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="a7d08-125">**Endboundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="a7d08-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="a7d08-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="a7d08-126">dateTime</span></span>                                                                 | <span data-ttu-id="a7d08-127">Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="a7d08-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="a7d08-128">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="a7d08-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="a7d08-129">**Executiontimelimit (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="a7d08-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="a7d08-130">duration</span><span class="sxs-lookup"><span data-stu-id="a7d08-130">duration</span></span>                                                                 | <span data-ttu-id="a7d08-131">Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7d08-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="a7d08-132">**Wiederholung (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="a7d08-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="a7d08-133">**Wiederholungstyp**</span><span class="sxs-lookup"><span data-stu-id="a7d08-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="a7d08-134">Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="a7d08-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="a7d08-135">**StartBoundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="a7d08-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="a7d08-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="a7d08-136">dateTime</span></span>                                                                 | <span data-ttu-id="a7d08-137">Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="a7d08-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="a7d08-138">Attributes</span><span class="sxs-lookup"><span data-stu-id="a7d08-138">Attributes</span></span>



| <span data-ttu-id="a7d08-139">Name</span><span class="sxs-lookup"><span data-stu-id="a7d08-139">Name</span></span> | <span data-ttu-id="a7d08-140">type</span><span class="sxs-lookup"><span data-stu-id="a7d08-140">Type</span></span>       | <span data-ttu-id="a7d08-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7d08-141">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="a7d08-142">Id</span><span class="sxs-lookup"><span data-stu-id="a7d08-142">Id</span></span>   | <span data-ttu-id="a7d08-143">**string**</span><span class="sxs-lookup"><span data-stu-id="a7d08-143">**string**</span></span> | <span data-ttu-id="a7d08-144">Der Bezeichner des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="a7d08-144">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a7d08-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7d08-145">Remarks</span></span>

<span data-ttu-id="a7d08-146">Bei der Skript Entwicklung wird ein Start-ausgelöst, der vom [**boottrigger**](boottrigger.md) -Objekt definiert wird.</span><span class="sxs-lookup"><span data-stu-id="a7d08-146">For script development, a boot trigger is defined by the [**BootTrigger**](boottrigger.md) object.</span></span>

<span data-ttu-id="a7d08-147">Bei der C++-Entwicklung wird ein Start-- [**Debugger durch das iboottrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) -Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="a7d08-147">For C++ development, a boot trigger is defined by the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) object.</span></span>

## <a name="examples"></a><span data-ttu-id="a7d08-148">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7d08-148">Examples</span></span>

<span data-ttu-id="a7d08-149">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Start--Auslösers angibt, finden Sie unter Beispiel für den [Start-Beispiel](boot-trigger-example--xml-.md)</span><span class="sxs-lookup"><span data-stu-id="a7d08-149">For a complete example of the XML for a task that specifies a boot trigger, see [Boot Trigger Example (XML)](boot-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d08-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7d08-150">Requirements</span></span>



| <span data-ttu-id="a7d08-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7d08-151">Requirement</span></span> | <span data-ttu-id="a7d08-152">Wert</span><span class="sxs-lookup"><span data-stu-id="a7d08-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a7d08-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7d08-153">Minimum supported client</span></span><br/> | <span data-ttu-id="a7d08-154">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7d08-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a7d08-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7d08-155">Minimum supported server</span></span><br/> | <span data-ttu-id="a7d08-156">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7d08-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7d08-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7d08-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d08-158">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="a7d08-158">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a7d08-159">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="a7d08-159">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





