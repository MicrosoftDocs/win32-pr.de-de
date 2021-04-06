---
title: Schedulebymonthdayoatweek (calendartriggertype)-Element
description: Gibt einen monatlichen Zeitplan an Wochentagen an.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- Schedulebymonthdayomaweek-Element Taskplaner
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e92d6ad530466a2238c8239c9e262f85ae361d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742889"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a><span data-ttu-id="4cc2b-104">Schedulebymonthdayoatweek (calendartriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="4cc2b-104">ScheduleByMonthDayOfWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="4cc2b-105">Gibt einen monatlichen Zeitplan an Wochentagen an.</span><span class="sxs-lookup"><span data-stu-id="4cc2b-105">Specifies a monthly day-of-week schedule.</span></span> <span data-ttu-id="4cc2b-106">Beispielsweise wird die Aufgabe an bestimmten Wochentagen, Wochen des Monats und Monaten des Jahres gestartet.</span><span class="sxs-lookup"><span data-stu-id="4cc2b-106">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span>

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

<span data-ttu-id="4cc2b-107">Das **schedulebymonthdayosweek** -Element wird durch den komplexen [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="4cc2b-107">The **ScheduleByMonthDayOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4cc2b-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="4cc2b-108">Parent element</span></span>



| <span data-ttu-id="4cc2b-109">Element</span><span class="sxs-lookup"><span data-stu-id="4cc2b-109">Element</span></span>                                                                             | <span data-ttu-id="4cc2b-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="4cc2b-110">Derived from</span></span>                                                                       | <span data-ttu-id="4cc2b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cc2b-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4cc2b-112">**Calendarausgelöst**</span><span class="sxs-lookup"><span data-stu-id="4cc2b-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="4cc2b-113">**calendartriggertype**</span><span class="sxs-lookup"><span data-stu-id="4cc2b-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="4cc2b-114">Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.</span><span class="sxs-lookup"><span data-stu-id="4cc2b-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="4cc2b-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4cc2b-115">Child elements</span></span>



| <span data-ttu-id="4cc2b-116">Element</span><span class="sxs-lookup"><span data-stu-id="4cc2b-116">Element</span></span>                                                                                   | <span data-ttu-id="4cc2b-117">type</span><span class="sxs-lookup"><span data-stu-id="4cc2b-117">Type</span></span>                                                                     | <span data-ttu-id="4cc2b-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cc2b-118">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="4cc2b-119">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="4cc2b-119">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="4cc2b-120">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="4cc2b-120">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="4cc2b-121">Gibt die Wochentage an, an denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4cc2b-121">Specifies the days of the week in which the task runs.</span></span><br/>       |
| [<span data-ttu-id="4cc2b-122">**Monate**</span><span class="sxs-lookup"><span data-stu-id="4cc2b-122">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="4cc2b-123">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="4cc2b-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="4cc2b-124">Gibt die Monate des Jahres an, in dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4cc2b-124">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="4cc2b-125">**Wochen**</span><span class="sxs-lookup"><span data-stu-id="4cc2b-125">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | <span data-ttu-id="4cc2b-126">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="4cc2b-126">unsignedByte</span></span>                                                             | <span data-ttu-id="4cc2b-127">Gibt das Intervall zwischen den Wochen im Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="4cc2b-127">Specifies the interval between the weeks in the schedule.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="4cc2b-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cc2b-128">Remarks</span></span>

<span data-ttu-id="4cc2b-129">Die Uhrzeit, zu der die Aufgabe gestartet wird, wird durch das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4cc2b-129">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="4cc2b-130">Bei der Skripterstellung wird ein monatlicher Tag-of-week-Wert mit dem [**monthlydowauslöserobjekt**](monthlydowtrigger.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="4cc2b-130">For scripting development, a monthly day-of-week trigger is specified using the [**MonthlyDOWTrigger**](monthlydowtrigger.md) object.</span></span>

<span data-ttu-id="4cc2b-131">Bei der C++-Entwicklung wird ein monatlicher Wochentag mithilfe der [**imonthlydow-auslöserschnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) angegeben.</span><span class="sxs-lookup"><span data-stu-id="4cc2b-131">For C++ development, a monthly day-of-week trigger is specified using the [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) interface.</span></span>

<span data-ttu-id="4cc2b-132">Die oben aufgeführten untergeordneten Elemente werden von den komplexen Elementtypen [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="4cc2b-132">The child elements listed above are defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="4cc2b-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4cc2b-133">Examples</span></span>

<span data-ttu-id="4cc2b-134">Im folgenden XML-Code wird ein monatlicher Tag of week-Kalender-Auslösers definiert, mit dem eine Aufgabe (um 8:00 Uhr) am Montag der ersten Woche für jeden Monat des Jahres gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="4cc2b-134">The following XML defines a monthly day of week calendar trigger that starts a task ( at 8:00 AM) on Monday of the first week for each month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonthDayOfWeek>
        <Weeks>
            <Week>1</Week>
        </Weeks>
        <DaysOfWeek>
            <Monday/>
        </DaysOfWeek>
        <Months>
            <January/>
            <February/>
            <March/>
            <April/>
            <May/>
            <June/>
            <July/>
            <August/>
            <September/>
            <October/>
            <November/>
            <December/>
        <Months>
    </ScheduleByMonthDayOfWeek>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="4cc2b-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cc2b-135">Requirements</span></span>



| <span data-ttu-id="4cc2b-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cc2b-136">Requirement</span></span> | <span data-ttu-id="4cc2b-137">Wert</span><span class="sxs-lookup"><span data-stu-id="4cc2b-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4cc2b-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4cc2b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4cc2b-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4cc2b-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4cc2b-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4cc2b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4cc2b-141">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4cc2b-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4cc2b-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cc2b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc2b-143">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="4cc2b-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4cc2b-144">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="4cc2b-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





