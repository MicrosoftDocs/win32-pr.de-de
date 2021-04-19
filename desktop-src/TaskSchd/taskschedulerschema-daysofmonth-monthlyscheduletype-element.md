---
title: DaysOfMonth (monthlyscheduletype)-Element
description: Gibt die Tage des Monats an, in denen der Task ausgeführt wird.
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- DaysOfMonth-Element Taskplaner
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344274"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a><span data-ttu-id="5cf24-104">DaysOfMonth (monthlyscheduletype)-Element</span><span class="sxs-lookup"><span data-stu-id="5cf24-104">DaysOfMonth (monthlyScheduleType) Element</span></span>

<span data-ttu-id="5cf24-105">Gibt die Tage des Monats an, in denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cf24-105">Specifies the days of the month during which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

<span data-ttu-id="5cf24-106">Das **daysOfMonth** -Element wird durch den komplexen [**monthlyscheduletype**](taskschedulerschema-monthlyscheduletype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="5cf24-106">The **DaysOfMonth** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5cf24-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="5cf24-107">Parent element</span></span>



| <span data-ttu-id="5cf24-108">Element</span><span class="sxs-lookup"><span data-stu-id="5cf24-108">Element</span></span>                                                                                    | <span data-ttu-id="5cf24-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="5cf24-109">Derived from</span></span>                                                                                         | <span data-ttu-id="5cf24-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5cf24-110">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="5cf24-111">**Schedulebymonth**</span><span class="sxs-lookup"><span data-stu-id="5cf24-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="5cf24-112">**monthlydayosweekscheduletype**</span><span class="sxs-lookup"><span data-stu-id="5cf24-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="5cf24-113">Gibt einen-Vorgang an, der einen Auftrag für einen monatlichen Wochentag startet.</span><span class="sxs-lookup"><span data-stu-id="5cf24-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="5cf24-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5cf24-114">Child elements</span></span>



| <span data-ttu-id="5cf24-115">Element</span><span class="sxs-lookup"><span data-stu-id="5cf24-115">Element</span></span>                                                        | <span data-ttu-id="5cf24-116">type</span><span class="sxs-lookup"><span data-stu-id="5cf24-116">Type</span></span>                                                                    | <span data-ttu-id="5cf24-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5cf24-117">Description</span></span>                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="5cf24-118">**Tag**</span><span class="sxs-lookup"><span data-stu-id="5cf24-118">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="5cf24-119">**dayoatmonthtype**</span><span class="sxs-lookup"><span data-stu-id="5cf24-119">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="5cf24-120">Gibt den Tag des Monats an, in dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cf24-120">Specifies a day of the month during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5cf24-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5cf24-121">Remarks</span></span>

<span data-ttu-id="5cf24-122">Bei der Skript Entwicklung werden die Tage des Monats für den Zeitplan mithilfe der [**Monthly-Eigenschaft. daysOfMonth**](monthlytrigger-daysofmonth.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="5cf24-122">For script development, the days of the month for the schedule are specified using the [**MonthlyTrigger.DaysOfMonth**](monthlytrigger-daysofmonth.md) property.</span></span>

<span data-ttu-id="5cf24-123">Bei der C++-Entwicklung werden die Tage des Monats für den Zeitplan mithilfe der [**imonthly-Eigenschaft:D aysofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="5cf24-123">For C++ development, the days of the month for the schedule are specified using the [**IMonthlyTrigger::DaysOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) property.</span></span>

<span data-ttu-id="5cf24-124">Das untergeordnete Element muss für jeden Tag des Monats, an dem die Aufgabe ausgeführt werden soll, wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="5cf24-124">The child element must be repeated for each day of the month the task is to run.</span></span>

## <a name="examples"></a><span data-ttu-id="5cf24-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5cf24-125">Examples</span></span>

<span data-ttu-id="5cf24-126">Mit dem folgenden XML-Code wird ein monatlicher Kalender-Auslösers definiert, der am 1. Tag jedes Monats eine Aufgabe (um 8:30 Uhr) startet.</span><span class="sxs-lookup"><span data-stu-id="5cf24-126">The following XML defines a monthly calendar trigger that starts a task (at 8:30 AM) on the 1st day of every month.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
        </DaysOfMonth>
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
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="5cf24-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5cf24-127">Requirements</span></span>



| <span data-ttu-id="5cf24-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5cf24-128">Requirement</span></span> | <span data-ttu-id="5cf24-129">Wert</span><span class="sxs-lookup"><span data-stu-id="5cf24-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5cf24-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5cf24-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5cf24-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5cf24-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5cf24-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5cf24-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5cf24-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5cf24-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cf24-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cf24-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf24-135">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="5cf24-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5cf24-136">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="5cf24-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





