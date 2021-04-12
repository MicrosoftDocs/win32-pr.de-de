---
title: Monate (monthlyscheduletype)-Element
description: Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
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
ms.openlocfilehash: 0ed40fd2466f8962f839f39e7addd3b7e1bc33eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105369"
---
# <a name="months-monthlyscheduletype-element"></a><span data-ttu-id="f9605-104">Monate (monthlyscheduletype)-Element</span><span class="sxs-lookup"><span data-stu-id="f9605-104">Months (monthlyScheduleType) Element</span></span>

<span data-ttu-id="f9605-105">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9605-105">Specifies the months of the year during which the task runs for a monthly schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="f9605-106">Das **Monats** Element wird durch den komplexen [**monthlyscheduletype**](taskschedulerschema-monthlyscheduletype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="f9605-106">The **Months** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f9605-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f9605-107">Parent element</span></span>



| <span data-ttu-id="f9605-108">Element</span><span class="sxs-lookup"><span data-stu-id="f9605-108">Element</span></span>                                                                                    | <span data-ttu-id="f9605-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="f9605-109">Derived from</span></span>                                                                       | <span data-ttu-id="f9605-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9605-110">Description</span></span>                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="f9605-111">**Schedulebymonth**</span><span class="sxs-lookup"><span data-stu-id="f9605-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="f9605-112">**monthlyscheduletype**</span><span class="sxs-lookup"><span data-stu-id="f9605-112">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md) | <span data-ttu-id="f9605-113">Gibt einen monatlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="f9605-113">Specifies a monthly schedule.</span></span> <br/> |



## <a name="child-elements"></a><span data-ttu-id="f9605-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9605-114">Child elements</span></span>



| <span data-ttu-id="f9605-115">Element</span><span class="sxs-lookup"><span data-stu-id="f9605-115">Element</span></span>                                                                            | <span data-ttu-id="f9605-116">type</span><span class="sxs-lookup"><span data-stu-id="f9605-116">Type</span></span> | <span data-ttu-id="f9605-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9605-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="f9605-118">**April (monthstype)**</span><span class="sxs-lookup"><span data-stu-id="f9605-118">**April (monthsType)**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="f9605-119">Gibt an, dass der Task im April ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9605-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="f9605-120">**August (monthstype)**</span><span class="sxs-lookup"><span data-stu-id="f9605-120">**August (monthsType)**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="f9605-121">Gibt an, dass der Task im August ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9605-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="f9605-122">**Dezember (monthstype)**</span><span class="sxs-lookup"><span data-stu-id="f9605-122">**December (monthsType)**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="f9605-123">Gibt an, dass der Task im Dezember ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9605-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="f9605-124">**Februar (monthstype)**</span><span class="sxs-lookup"><span data-stu-id="f9605-124">**February (monthsType)**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="f9605-125">Gibt an, dass der Task im Februar ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9605-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="f9605-126">**Januar (monthstype)**</span><span class="sxs-lookup"><span data-stu-id="f9605-126">**January (monthsType)**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="f9605-127">Gibt an, dass der Task im Januar ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9605-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="f9605-128">**Juli (monthstype)**</span><span class="sxs-lookup"><span data-stu-id="f9605-128">**July (monthsType)**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="f9605-129">Gibt an, dass der Task im Juli ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9605-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="f9605-130">**Juni (monthstype)**</span><span class="sxs-lookup"><span data-stu-id="f9605-130">**June (monthsType)**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="f9605-131">Gibt an, dass der Task im Juni ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9605-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="f9605-132">**März (monthstype)**</span><span class="sxs-lookup"><span data-stu-id="f9605-132">**March (monthsType)**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="f9605-133">Gibt an, dass der Task im März ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9605-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="f9605-134">**Mai (monthstype)**</span><span class="sxs-lookup"><span data-stu-id="f9605-134">**May (monthsType)**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="f9605-135">Gibt an, dass der Task im Mai ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9605-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="f9605-136">**November (monthstype)**</span><span class="sxs-lookup"><span data-stu-id="f9605-136">**November (monthsType)**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="f9605-137">Gibt an, dass der Task im November ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9605-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="f9605-138">**Oktober (monthstype)**</span><span class="sxs-lookup"><span data-stu-id="f9605-138">**October (monthsType)**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="f9605-139">Gibt an, dass der Task im Oktober ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9605-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="f9605-140">**September (monthstype)**</span><span class="sxs-lookup"><span data-stu-id="f9605-140">**September (monthsType)**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="f9605-141">Gibt an, dass der Task im September ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9605-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f9605-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9605-142">Remarks</span></span>

<span data-ttu-id="f9605-143">Bei der Skript Entwicklung werden die Monate des Zeitplans mithilfe der [**Monthly-Eigenschaft. MONTHSOFYEAR**](monthlytrigger-monthsofyear.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="f9605-143">For script development, the months of the schedule are specified using the [**MonthlyTrigger.MonthsOfYear**](monthlytrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="f9605-144">Bei der C++-Entwicklung werden die Monate des Zeitplans mithilfe der [**imonthlyauslöst:: MONTHSOFYEAR**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="f9605-144">For C++ development, the months of the schedule are specified using the [**IMonthlyTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) property.</span></span>

## <a name="examples"></a><span data-ttu-id="f9605-145">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9605-145">Examples</span></span>

<span data-ttu-id="f9605-146">Im folgenden XML-Code wird ein monatlicher Kalender definiert, der die Aufgabe am 1. und 15. Tag eines jeden Monats des Jahres startet.</span><span class="sxs-lookup"><span data-stu-id="f9605-146">The following XML defines a monthly calendar that starts the task on the 1st and 15th day of every month of the year.</span></span>


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
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
```



## <a name="requirements"></a><span data-ttu-id="f9605-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9605-147">Requirements</span></span>



| <span data-ttu-id="f9605-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9605-148">Requirement</span></span> | <span data-ttu-id="f9605-149">Wert</span><span class="sxs-lookup"><span data-stu-id="f9605-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9605-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9605-150">Minimum supported client</span></span><br/> | <span data-ttu-id="f9605-151">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9605-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f9605-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9605-152">Minimum supported server</span></span><br/> | <span data-ttu-id="f9605-153">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9605-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9605-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9605-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9605-155">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="f9605-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f9605-156">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="f9605-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





