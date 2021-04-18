---
title: Calendartrigger (triggergroup)-Element
description: Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- Calendar-auslöserTaskplaner, XML-Element
- Calendarauslöserelement Taskplaner
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02c061d8821dffa82eca8756ab26acadc6bb9281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338749"
---
# <a name="calendartrigger-triggergroup-element"></a><span data-ttu-id="d1c09-105">Calendartrigger (triggergroup)-Element</span><span class="sxs-lookup"><span data-stu-id="d1c09-105">CalendarTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="d1c09-106">Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.</span><span class="sxs-lookup"><span data-stu-id="d1c09-106">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span>

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

<span data-ttu-id="d1c09-107">Das **calendartrigger** -Element wird durch den komplexen Typ [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="d1c09-107">The **CalendarTrigger** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d1c09-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d1c09-108">Parent element</span></span>



| <span data-ttu-id="d1c09-109">Element</span><span class="sxs-lookup"><span data-stu-id="d1c09-109">Element</span></span>                                                           | <span data-ttu-id="d1c09-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="d1c09-110">Derived from</span></span>                                                         | <span data-ttu-id="d1c09-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1c09-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="d1c09-112">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="d1c09-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="d1c09-113">**triggerstype**</span><span class="sxs-lookup"><span data-stu-id="d1c09-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="d1c09-114">Gibt die Trigger an, die den Task starten.</span><span class="sxs-lookup"><span data-stu-id="d1c09-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="d1c09-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1c09-115">Child elements</span></span>



| <span data-ttu-id="d1c09-116">Element</span><span class="sxs-lookup"><span data-stu-id="d1c09-116">Element</span></span>                                                                                                                            | <span data-ttu-id="d1c09-117">type</span><span class="sxs-lookup"><span data-stu-id="d1c09-117">Type</span></span>                                                                                                 | <span data-ttu-id="d1c09-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1c09-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1c09-119">**Aktiviert (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d1c09-119">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | <span data-ttu-id="d1c09-120">boolean</span><span class="sxs-lookup"><span data-stu-id="d1c09-120">boolean</span></span>                                                                                              | <span data-ttu-id="d1c09-121">Gibt an, dass der-Wert aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d1c09-121">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="d1c09-122">**Endboundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d1c09-122">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | <span data-ttu-id="d1c09-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="d1c09-123">dateTime</span></span>                                                                                             | <span data-ttu-id="d1c09-124">Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="d1c09-124">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="d1c09-125">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="d1c09-125">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="d1c09-126">**Executiontimelimit (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d1c09-126">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | <span data-ttu-id="d1c09-127">duration</span><span class="sxs-lookup"><span data-stu-id="d1c09-127">duration</span></span>                                                                                             | <span data-ttu-id="d1c09-128">Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d1c09-128">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="d1c09-129">**Wiederholung (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d1c09-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [<span data-ttu-id="d1c09-130">**Wiederholungstyp**</span><span class="sxs-lookup"><span data-stu-id="d1c09-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md)                             | <span data-ttu-id="d1c09-131">Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="d1c09-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="d1c09-132">**Schedulebyday (calendartriggertype)**</span><span class="sxs-lookup"><span data-stu-id="d1c09-132">**ScheduleByDay (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="d1c09-133">**dailyscheduletype**</span><span class="sxs-lookup"><span data-stu-id="d1c09-133">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="d1c09-134">Gibt einen täglichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="d1c09-134">Specifies a daily schedule.</span></span><br/>                                                                                             |
| [<span data-ttu-id="d1c09-135">**Schedulebymonth (calendartriggertype)**</span><span class="sxs-lookup"><span data-stu-id="d1c09-135">**ScheduleByMonth (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="d1c09-136">**monthlyscheduletype**</span><span class="sxs-lookup"><span data-stu-id="d1c09-136">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="d1c09-137">Gibt einen monatlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="d1c09-137">Specifies a monthly schedule.</span></span><br/>                                                                                           |
| [<span data-ttu-id="d1c09-138">**Schedulebymonthdayoatweek (calendartriggertype)**</span><span class="sxs-lookup"><span data-stu-id="d1c09-138">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="d1c09-139">**monthlydayosweekscheduletype**</span><span class="sxs-lookup"><span data-stu-id="d1c09-139">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="d1c09-140">Gibt einen-Vorgang an, durch den ein Auftrag an einem monatlichen Wochentag gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d1c09-140">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/>                                                |
| [<span data-ttu-id="d1c09-141">**Schedulebyweek (calendartriggertype)**</span><span class="sxs-lookup"><span data-stu-id="d1c09-141">**ScheduleByWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="d1c09-142">**weeklyscheduletype**</span><span class="sxs-lookup"><span data-stu-id="d1c09-142">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="d1c09-143">Gibt einen wöchentlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="d1c09-143">Specifies a weekly schedule.</span></span><br/>                                                                                            |
| [<span data-ttu-id="d1c09-144">**StartBoundary (triggerbasetype)**</span><span class="sxs-lookup"><span data-stu-id="d1c09-144">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | <span data-ttu-id="d1c09-145">dateTime</span><span class="sxs-lookup"><span data-stu-id="d1c09-145">dateTime</span></span>                                                                                             | <span data-ttu-id="d1c09-146">Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="d1c09-146">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="d1c09-147">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d1c09-147">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="d1c09-148">Attributes</span><span class="sxs-lookup"><span data-stu-id="d1c09-148">Attributes</span></span>



| <span data-ttu-id="d1c09-149">Name</span><span class="sxs-lookup"><span data-stu-id="d1c09-149">Name</span></span> | <span data-ttu-id="d1c09-150">type</span><span class="sxs-lookup"><span data-stu-id="d1c09-150">Type</span></span> | <span data-ttu-id="d1c09-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1c09-151">Description</span></span>                               |
|------|------|-------------------------------------------|
| <span data-ttu-id="d1c09-152">Id</span><span class="sxs-lookup"><span data-stu-id="d1c09-152">Id</span></span>   | <span data-ttu-id="d1c09-153">id</span><span class="sxs-lookup"><span data-stu-id="d1c09-153">ID</span></span>   | <span data-ttu-id="d1c09-154">Der Bezeichner des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="d1c09-154">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d1c09-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1c09-155">Remarks</span></span>

<span data-ttu-id="d1c09-156">Das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element ist ein erforderliches Element für Zeit-und Kalender Trigger ([**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) und **calendartrigger**).</span><span class="sxs-lookup"><span data-stu-id="d1c09-156">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and **CalendarTrigger**).</span></span>

<span data-ttu-id="d1c09-157">Die oben aufgeführten untergeordneten Elemente werden von den komplexen Elementtypen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) und [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="d1c09-157">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex element types.</span></span>

<span data-ttu-id="d1c09-158">Bei der Skript Entwicklung werden Kalender Trigger mithilfe eines der folgenden Objekte angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1c09-158">For script development, calendar triggers are specified using one of the following objects.</span></span>

-   [<span data-ttu-id="d1c09-159">**Dailylöst**</span><span class="sxs-lookup"><span data-stu-id="d1c09-159">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="d1c09-160">**Weeklyauslösers**</span><span class="sxs-lookup"><span data-stu-id="d1c09-160">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="d1c09-161">**Monthly-auslöst**</span><span class="sxs-lookup"><span data-stu-id="d1c09-161">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="d1c09-162">**Monthlydowlöst**</span><span class="sxs-lookup"><span data-stu-id="d1c09-162">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)

<span data-ttu-id="d1c09-163">Bei der C++-Entwicklung werden Kalender Trigger mithilfe einer der folgenden Schnittstellen angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1c09-163">For C++ development, calendar triggers are specified using one of the following interfaces.</span></span>

-   [<span data-ttu-id="d1c09-164">**Idaily-Fehler**</span><span class="sxs-lookup"><span data-stu-id="d1c09-164">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="d1c09-165">**Iweeklylöst**</span><span class="sxs-lookup"><span data-stu-id="d1c09-165">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [<span data-ttu-id="d1c09-166">**Imonthly-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="d1c09-166">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="d1c09-167">**Imonthlydowlöst**</span><span class="sxs-lookup"><span data-stu-id="d1c09-167">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a><span data-ttu-id="d1c09-168">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1c09-168">Examples</span></span>

<span data-ttu-id="d1c09-169">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Kalender--Auslösers angibt, finden Sie unter Beispiel für das [tägliche Beispiel (XML)](daily-trigger-example--xml-.md)</span><span class="sxs-lookup"><span data-stu-id="d1c09-169">For a complete example of the XML for a task that specifies a calendar trigger, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1c09-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1c09-170">Requirements</span></span>



| <span data-ttu-id="d1c09-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1c09-171">Requirement</span></span> | <span data-ttu-id="d1c09-172">Wert</span><span class="sxs-lookup"><span data-stu-id="d1c09-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d1c09-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1c09-173">Minimum supported client</span></span><br/> | <span data-ttu-id="d1c09-174">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1c09-174">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d1c09-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1c09-175">Minimum supported server</span></span><br/> | <span data-ttu-id="d1c09-176">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1c09-176">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1c09-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1c09-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c09-178">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="d1c09-178">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d1c09-179">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d1c09-179">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





