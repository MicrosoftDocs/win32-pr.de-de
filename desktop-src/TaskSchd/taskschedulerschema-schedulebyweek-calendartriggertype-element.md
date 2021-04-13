---
title: Schedulebyweek (calendartriggertype)-Element
description: Gibt einen wöchentlichen Zeitplan an.
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- wöchentlicher auslöserTaskplaner, XML-Element
- Schedulebyweek-Element Taskplaner
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d5ab62a0c39c4c1d0102edcdb96d310e9315820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392174"
---
# <a name="schedulebyweek-calendartriggertype-element"></a><span data-ttu-id="bdc1d-105">Schedulebyweek (calendartriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="bdc1d-105">ScheduleByWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="bdc1d-106">Gibt einen wöchentlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-106">Specifies a weekly schedule.</span></span> <span data-ttu-id="bdc1d-107">Der Task wird z. b. jede Woche um 8:00 Uhr an einem bestimmten Wochentag oder an einem bestimmten Wochentag in der Woche gestartet.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-107">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span>

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

<span data-ttu-id="bdc1d-108">Das **schedulebyweek** -Element wird durch den komplexen Typ [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-108">The **ScheduleByWeek** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bdc1d-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="bdc1d-109">Parent element</span></span>



| <span data-ttu-id="bdc1d-110">Element</span><span class="sxs-lookup"><span data-stu-id="bdc1d-110">Element</span></span>                                                                             | <span data-ttu-id="bdc1d-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="bdc1d-111">Derived from</span></span>                                                                       | <span data-ttu-id="bdc1d-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdc1d-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bdc1d-113">**Calendarausgelöst**</span><span class="sxs-lookup"><span data-stu-id="bdc1d-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="bdc1d-114">**calendartriggertype**</span><span class="sxs-lookup"><span data-stu-id="bdc1d-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="bdc1d-115">Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="bdc1d-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bdc1d-116">Child elements</span></span>



| <span data-ttu-id="bdc1d-117">Element</span><span class="sxs-lookup"><span data-stu-id="bdc1d-117">Element</span></span>                                                                               | <span data-ttu-id="bdc1d-118">type</span><span class="sxs-lookup"><span data-stu-id="bdc1d-118">Type</span></span>                                                                     | <span data-ttu-id="bdc1d-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdc1d-119">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="bdc1d-120">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="bdc1d-120">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="bdc1d-121">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="bdc1d-121">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="bdc1d-122">Gibt die Wochentage an, an denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-122">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="bdc1d-123">**Weeksinterval**</span><span class="sxs-lookup"><span data-stu-id="bdc1d-123">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | <span data-ttu-id="bdc1d-124">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="bdc1d-124">unsignedByte</span></span>                                                             | <span data-ttu-id="bdc1d-125">Gibt das Intervall zwischen den Wochen im Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-125">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bdc1d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdc1d-126">Remarks</span></span>

<span data-ttu-id="bdc1d-127">Die oben aufgeführten untergeordneten Elemente werden von den komplexen Elementtypen [**weeklyscheduletype**](taskschedulerschema-weeklyscheduletype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-127">The child elements listed above are defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="bdc1d-128">Die Uhrzeit, zu der die Aufgabe gestartet wird, wird durch das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-128">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="bdc1d-129">Bei der Skripterstellung wird ein wöchentlicher-Auslösung mithilfe des [**Weekly-auslöserobjekts**](weeklytrigger.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-129">For scripting development, a weekly trigger is specified using the [**WeeklyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="bdc1d-130">Bei der C++-Entwicklung wird ein wöchentlicher-Auslösers mithilfe der [**iweekly-**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) Schnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-130">For C++ development, a weekly trigger is specified using the [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="bdc1d-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdc1d-131">Examples</span></span>

<span data-ttu-id="bdc1d-132">Der folgende XML-Code definiert einen wöchentlichen Kalender--Auslösers, der jede Woche einen Task Montag bis Freitag (um 8:00 Uhr) startet.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-132">The following XML defines a weekly calendar trigger that starts a task Monday through Friday (at 8:00 AM) every week.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="bdc1d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdc1d-133">Requirements</span></span>



| <span data-ttu-id="bdc1d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdc1d-134">Requirement</span></span> | <span data-ttu-id="bdc1d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="bdc1d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bdc1d-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdc1d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc1d-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdc1d-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bdc1d-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdc1d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc1d-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdc1d-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bdc1d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdc1d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc1d-141">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="bdc1d-141">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="bdc1d-142">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="bdc1d-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





