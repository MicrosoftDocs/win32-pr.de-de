---
title: DaysOfWeek-Element (monthlydayosweekscheduletype)
description: Gibt die Wochentage an, an denen der Task ausgeführt wird. | DaysOfWeek-Element (monthlydayosweekscheduletype)
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
keywords:
- DaysOfWeek-Element Taskplaner
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3867e08dd001a035a3ab25da056f75c1e73eeeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106367329"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a><span data-ttu-id="3195f-105">DaysOfWeek-Element (monthlydayosweekscheduletype)</span><span class="sxs-lookup"><span data-stu-id="3195f-105">DaysOfWeek (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="3195f-106">Gibt die Wochentage an, an denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3195f-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="3195f-107">Das **DaysOfWeek** -Element wird durch den komplexen [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="3195f-107">The **DaysOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3195f-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="3195f-108">Parent element</span></span>



| <span data-ttu-id="3195f-109">Element</span><span class="sxs-lookup"><span data-stu-id="3195f-109">Element</span></span>                                                                                                      | <span data-ttu-id="3195f-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="3195f-110">Derived from</span></span>                                                                                         | <span data-ttu-id="3195f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3195f-111">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="3195f-112">**Schedulebymonthdayof-Woche**</span><span class="sxs-lookup"><span data-stu-id="3195f-112">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="3195f-113">**monthlydayosweekscheduletype**</span><span class="sxs-lookup"><span data-stu-id="3195f-113">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="3195f-114">Gibt einen-Vorgang an, der einen Auftrag für einen monatlichen Wochentag startet.</span><span class="sxs-lookup"><span data-stu-id="3195f-114">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="3195f-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3195f-115">Child elements</span></span>



| <span data-ttu-id="3195f-116">Element</span><span class="sxs-lookup"><span data-stu-id="3195f-116">Element</span></span>                                                                   | <span data-ttu-id="3195f-117">type</span><span class="sxs-lookup"><span data-stu-id="3195f-117">Type</span></span> | <span data-ttu-id="3195f-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3195f-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="3195f-119">**Am**</span><span class="sxs-lookup"><span data-stu-id="3195f-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="3195f-120">Gibt an, dass der Task am Freitag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3195f-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="3195f-121">**Pfingst**</span><span class="sxs-lookup"><span data-stu-id="3195f-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="3195f-122">Gibt an, dass der Task am Montag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3195f-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="3195f-123">**Samstag**</span><span class="sxs-lookup"><span data-stu-id="3195f-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="3195f-124">Gibt an, dass der Task am Samstag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3195f-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="3195f-125">**Sunday**</span><span class="sxs-lookup"><span data-stu-id="3195f-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="3195f-126">Gibt an, dass der Task am Sonntag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3195f-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="3195f-127">**Mitteilte**</span><span class="sxs-lookup"><span data-stu-id="3195f-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="3195f-128">Gibt an, dass der Task am Donnerstag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3195f-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="3195f-129">**Mitteilte**</span><span class="sxs-lookup"><span data-stu-id="3195f-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="3195f-130">Gibt an, dass der Task am Dienstag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3195f-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="3195f-131">**Mittwochs**</span><span class="sxs-lookup"><span data-stu-id="3195f-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="3195f-132">Gibt an, dass der Task am Mittwoch ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3195f-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3195f-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3195f-133">Remarks</span></span>

<span data-ttu-id="3195f-134">Bei der Entwicklung von Skripts werden die Wochentage für einen monatlichen Wochentag mit Wochentag mithilfe der Eigenschaft [**monthlydowauslöst. DaysOfWeek**](monthlydowtrigger-daysofweek.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="3195f-134">For scripting development, the days of the week for a monthly day-of-week calendar are specified using the [**MonthlyDOWTrigger.DaysOfWeek**](monthlydowtrigger-daysofweek.md) property.</span></span>

<span data-ttu-id="3195f-135">Bei der C++-Entwicklung werden die Wochentage für einen monatlichen Wochentag mithilfe der [**imonthlydowauslöst::D aysofweek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="3195f-135">For C++ development, the days of the week for a monthly day-of-week calendar are specified using the [**IMonthlyDOWTrigger::DaysOfWeek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) property.</span></span>

<span data-ttu-id="3195f-136">Die oben aufgeführten untergeordneten Elemente werden durch den komplexen Typ [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="3195f-136">The child elements above are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="3195f-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3195f-137">Examples</span></span>

<span data-ttu-id="3195f-138">Im folgenden XML-Code wird ein monatlicher Wochentag definiert, der die Aufgabe am Montag der ersten Woche für jeden Monat des Jahres startet.</span><span class="sxs-lookup"><span data-stu-id="3195f-138">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


```XML
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
```



## <a name="requirements"></a><span data-ttu-id="3195f-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3195f-139">Requirements</span></span>



| <span data-ttu-id="3195f-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3195f-140">Requirement</span></span> | <span data-ttu-id="3195f-141">Wert</span><span class="sxs-lookup"><span data-stu-id="3195f-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3195f-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3195f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3195f-143">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3195f-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3195f-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3195f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3195f-145">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3195f-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3195f-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3195f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3195f-147">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="3195f-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3195f-148">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="3195f-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





