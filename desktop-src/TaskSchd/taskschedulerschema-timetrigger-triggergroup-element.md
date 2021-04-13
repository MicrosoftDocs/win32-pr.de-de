---
title: Timetrigger-Element (triggergroup)
description: Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- Time-Auslöserelement Taskplaner
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83d3b0a63a8be70af7eba4edb90e49db71892f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478162"
---
# <a name="timetrigger-triggergroup-element"></a><span data-ttu-id="d781d-104">Timetrigger-Element (triggergroup)</span><span class="sxs-lookup"><span data-stu-id="d781d-104">TimeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="d781d-105">Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="d781d-105">Specifies a trigger that starts a task when the trigger is activated.</span></span>

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

<span data-ttu-id="d781d-106">Das **timetrigger** -Element wird von [**triggergroup**](taskschedulerschema-triggergroup-group.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="d781d-106">The **TimeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="d781d-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d781d-107">Parent element</span></span>



| <span data-ttu-id="d781d-108">Element</span><span class="sxs-lookup"><span data-stu-id="d781d-108">Element</span></span>                                                           | <span data-ttu-id="d781d-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="d781d-109">Derived from</span></span>                                                         | <span data-ttu-id="d781d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d781d-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="d781d-111">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="d781d-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="d781d-112">**triggerstype**</span><span class="sxs-lookup"><span data-stu-id="d781d-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="d781d-113">Gibt die Trigger an, die den Task starten.</span><span class="sxs-lookup"><span data-stu-id="d781d-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="d781d-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d781d-114">Child elements</span></span>



| <span data-ttu-id="d781d-115">Element</span><span class="sxs-lookup"><span data-stu-id="d781d-115">Element</span></span>                                                                                                        | <span data-ttu-id="d781d-116">type</span><span class="sxs-lookup"><span data-stu-id="d781d-116">Type</span></span>                                                                     | <span data-ttu-id="d781d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d781d-117">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d781d-118">**Aktiviert (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d781d-118">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="d781d-119">boolean</span><span class="sxs-lookup"><span data-stu-id="d781d-119">boolean</span></span>                                                                  | <span data-ttu-id="d781d-120">Gibt an, dass der-Wert aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d781d-120">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="d781d-121">**Endboundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d781d-121">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="d781d-122">dateTime</span><span class="sxs-lookup"><span data-stu-id="d781d-122">dateTime</span></span>                                                                 | <span data-ttu-id="d781d-123">Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="d781d-123">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="d781d-124">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="d781d-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="d781d-125">**Executiontimelimit (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d781d-125">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="d781d-126">duration</span><span class="sxs-lookup"><span data-stu-id="d781d-126">duration</span></span>                                                                 | <span data-ttu-id="d781d-127">Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d781d-127">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="d781d-128">**Wiederholung (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d781d-128">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="d781d-129">**Wiederholungstyp**</span><span class="sxs-lookup"><span data-stu-id="d781d-129">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="d781d-130">Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="d781d-130">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="d781d-131">**StartBoundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d781d-131">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="d781d-132">dateTime</span><span class="sxs-lookup"><span data-stu-id="d781d-132">dateTime</span></span>                                                                 | <span data-ttu-id="d781d-133">Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="d781d-133">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="d781d-134">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d781d-134">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="d781d-135">Attributes</span><span class="sxs-lookup"><span data-stu-id="d781d-135">Attributes</span></span>



| <span data-ttu-id="d781d-136">Name</span><span class="sxs-lookup"><span data-stu-id="d781d-136">Name</span></span> | <span data-ttu-id="d781d-137">type</span><span class="sxs-lookup"><span data-stu-id="d781d-137">Type</span></span>       | <span data-ttu-id="d781d-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d781d-138">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="d781d-139">Id</span><span class="sxs-lookup"><span data-stu-id="d781d-139">Id</span></span>   | <span data-ttu-id="d781d-140">**string**</span><span class="sxs-lookup"><span data-stu-id="d781d-140">**string**</span></span> | <span data-ttu-id="d781d-141">Der Bezeichner des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="d781d-141">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d781d-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d781d-142">Remarks</span></span>

<span data-ttu-id="d781d-143">Das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element ist ein erforderliches Element für Zeit-und Kalender Trigger (**timetrigger** und [**calendartrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span><span class="sxs-lookup"><span data-stu-id="d781d-143">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers (**TimeTrigger** and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="d781d-144">Bei der Skripterstellung wird ein Zeit-und Zeit Auslöserwert mit dem [**time-Auslöserobjekt**](timetrigger.md)</span><span class="sxs-lookup"><span data-stu-id="d781d-144">For scripting development, a time trigger is specified using the [**TimeTrigger**](timetrigger.md) object.</span></span>

<span data-ttu-id="d781d-145">Bei der C++-Entwicklung wird mithilfe der [**Itime-auslöserschnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) ein Zeit-und ein Zeit--</span><span class="sxs-lookup"><span data-stu-id="d781d-145">For C++ development, a time trigger is specified using the [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) interface.</span></span>

<span data-ttu-id="d781d-146">Die oben aufgeführten untergeordneten Elemente werden von den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Elementtypen definiert.</span><span class="sxs-lookup"><span data-stu-id="d781d-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="d781d-147">Diese Elemente müssen in der unten gezeigten Sequenz hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d781d-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="d781d-148">**StartBoundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d781d-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="d781d-149">**Endboundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d781d-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="d781d-150">**Aktiviert (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d781d-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="d781d-151">**Wiederholung (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d781d-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="d781d-152">**Executiontimelimit (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d781d-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="d781d-153">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d781d-153">Examples</span></span>

<span data-ttu-id="d781d-154">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Zeit--Timeout angibt, finden Sie unter [time-auslöserbeispiel (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="d781d-154">For a complete example of the XML for a task that specifies a time trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d781d-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d781d-155">Requirements</span></span>



| <span data-ttu-id="d781d-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d781d-156">Requirement</span></span> | <span data-ttu-id="d781d-157">Wert</span><span class="sxs-lookup"><span data-stu-id="d781d-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d781d-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d781d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="d781d-159">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d781d-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d781d-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d781d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="d781d-161">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d781d-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d781d-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d781d-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d781d-163">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d781d-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





