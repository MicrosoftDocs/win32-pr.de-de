---
title: Monate (monthlydayosweekscheduletype)-Element
description: Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Monate-Element Taskplaner
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76f13a5823e0154519dbdb093dd03ea36bbe77b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391694"
---
# <a name="months-monthlydayofweekscheduletype-element"></a><span data-ttu-id="f538f-104">Monate (monthlydayosweekscheduletype)-Element</span><span class="sxs-lookup"><span data-stu-id="f538f-104">Months (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="f538f-105">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f538f-105">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="f538f-106">Das **Monats** Element wird durch den komplexen Typ [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="f538f-106">The **Months** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f538f-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f538f-107">Parent element</span></span>



| <span data-ttu-id="f538f-108">Element</span><span class="sxs-lookup"><span data-stu-id="f538f-108">Element</span></span>                                                                                                                            | <span data-ttu-id="f538f-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="f538f-109">Derived from</span></span>                                                                                         | <span data-ttu-id="f538f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f538f-110">Description</span></span>                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="f538f-111">**Schedulebymonthdayoatweek (calendartriggertype)**</span><span class="sxs-lookup"><span data-stu-id="f538f-111">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="f538f-112">**monthlydayosweekscheduletype**</span><span class="sxs-lookup"><span data-stu-id="f538f-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="f538f-113">Gibt einen-Vorgang an, der einen Auftrag für einen monatlichen Wochentag startet.</span><span class="sxs-lookup"><span data-stu-id="f538f-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f538f-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f538f-114">Child elements</span></span>



| <span data-ttu-id="f538f-115">Element</span><span class="sxs-lookup"><span data-stu-id="f538f-115">Element</span></span>                                                               | <span data-ttu-id="f538f-116">type</span><span class="sxs-lookup"><span data-stu-id="f538f-116">Type</span></span> | <span data-ttu-id="f538f-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f538f-117">Description</span></span>                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="f538f-118">**Am**</span><span class="sxs-lookup"><span data-stu-id="f538f-118">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="f538f-119">Gibt an, dass der Task im April ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f538f-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="f538f-120">**August**</span><span class="sxs-lookup"><span data-stu-id="f538f-120">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="f538f-121">Gibt an, dass der Task im August ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f538f-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="f538f-122">**Dezember**</span><span class="sxs-lookup"><span data-stu-id="f538f-122">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="f538f-123">Gibt an, dass der Task im Dezember ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f538f-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="f538f-124">**Februar**</span><span class="sxs-lookup"><span data-stu-id="f538f-124">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="f538f-125">Gibt an, dass der Task im Februar ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f538f-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="f538f-126">**January**</span><span class="sxs-lookup"><span data-stu-id="f538f-126">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="f538f-127">Gibt an, dass der Task im Januar ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f538f-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="f538f-128">**Juli**</span><span class="sxs-lookup"><span data-stu-id="f538f-128">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="f538f-129">Gibt an, dass der Task im Juli ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f538f-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="f538f-130">**June**</span><span class="sxs-lookup"><span data-stu-id="f538f-130">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="f538f-131">Gibt an, dass der Task im Juni ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f538f-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="f538f-132">**März**</span><span class="sxs-lookup"><span data-stu-id="f538f-132">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="f538f-133">Gibt an, dass der Task im März ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f538f-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="f538f-134">**May**</span><span class="sxs-lookup"><span data-stu-id="f538f-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="f538f-135">Gibt an, dass der Task im Mai ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f538f-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="f538f-136">**November**</span><span class="sxs-lookup"><span data-stu-id="f538f-136">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="f538f-137">Gibt an, dass der Task im November ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f538f-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="f538f-138">**Vom**</span><span class="sxs-lookup"><span data-stu-id="f538f-138">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="f538f-139">Gibt an, dass der Task im Oktober ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f538f-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="f538f-140">**September**</span><span class="sxs-lookup"><span data-stu-id="f538f-140">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="f538f-141">Gibt an, dass der Task im September ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f538f-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f538f-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f538f-142">Remarks</span></span>

<span data-ttu-id="f538f-143">Bei der Entwicklung von Skripts werden die Monate eines Jahres für einen monatlichen Wochentag mithilfe der Eigenschaft [**monthlydowauslöst. MONTHSOFYEAR**](monthlydowtrigger-monthsofyear.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="f538f-143">For scripting development, the months of a year for a monthly day-of-week schedule are specified using the [**MonthlyDOWTrigger.MonthsOfYear**](monthlydowtrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="f538f-144">Bei der C++-Entwicklung werden die Monate eines Jahres für einen monatlichen Wochentag mithilfe der [**imonthlydowauslöst:: MONTHSOFYEAR**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="f538f-144">For C++ development, the months of a year for a monthly day-of-week schedule are specified using the [**IMonthlyDOWTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) property.</span></span>

<span data-ttu-id="f538f-145">Die oben aufgeführten untergeordneten Elemente werden durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="f538f-145">The child elements above are defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="f538f-146">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f538f-146">Examples</span></span>

<span data-ttu-id="f538f-147">Im folgenden XML-Code wird ein monatlicher Wochentag definiert, der die Aufgabe am Montag der ersten Woche für jeden Monat des Jahres startet.</span><span class="sxs-lookup"><span data-stu-id="f538f-147">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f538f-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f538f-148">Requirements</span></span>



| <span data-ttu-id="f538f-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f538f-149">Requirement</span></span> | <span data-ttu-id="f538f-150">Wert</span><span class="sxs-lookup"><span data-stu-id="f538f-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f538f-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f538f-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f538f-152">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f538f-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f538f-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f538f-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f538f-154">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f538f-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f538f-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f538f-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f538f-156">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="f538f-156">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f538f-157">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="f538f-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





