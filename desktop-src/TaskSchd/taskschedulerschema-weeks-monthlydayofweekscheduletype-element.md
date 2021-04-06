---
title: Wochen (monthlydayosweekscheduletype)-Element
description: Gibt die Wochen des Monats an, in denen der Task ausgeführt wird.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Wochen Element Taskplaner
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e032b936353d2c89a84b5da684f681ea3c2b6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743312"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a><span data-ttu-id="c8016-104">Wochen (monthlydayosweekscheduletype)-Element</span><span class="sxs-lookup"><span data-stu-id="c8016-104">Weeks (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="c8016-105">Gibt die Wochen des Monats an, in denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8016-105">Specifies the weeks of the month in which the task is run.</span></span>

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

<span data-ttu-id="c8016-106">Das **weeks** -Element wird durch den komplexen [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="c8016-106">The **Weeks** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c8016-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="c8016-107">Parent element</span></span>



| <span data-ttu-id="c8016-108">Element</span><span class="sxs-lookup"><span data-stu-id="c8016-108">Element</span></span>                                                                                                      | <span data-ttu-id="c8016-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="c8016-109">Derived from</span></span>                                                                                         | <span data-ttu-id="c8016-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8016-110">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8016-111">**Schedulebymonthdayof-Woche**</span><span class="sxs-lookup"><span data-stu-id="c8016-111">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="c8016-112">**monthlydayosweekscheduletype**</span><span class="sxs-lookup"><span data-stu-id="c8016-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="c8016-113">Gibt einen-Vorgang an, durch den ein Auftrag an einem monatlichen Wochentag gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c8016-113">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="c8016-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c8016-114">Child elements</span></span>



| <span data-ttu-id="c8016-115">Element</span><span class="sxs-lookup"><span data-stu-id="c8016-115">Element</span></span>                                                    | <span data-ttu-id="c8016-116">type</span><span class="sxs-lookup"><span data-stu-id="c8016-116">Type</span></span>                                                        | <span data-ttu-id="c8016-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8016-117">Description</span></span>                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="c8016-118">**Mitte**</span><span class="sxs-lookup"><span data-stu-id="c8016-118">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="c8016-119">**weektype**</span><span class="sxs-lookup"><span data-stu-id="c8016-119">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="c8016-120">Gibt eine bestimmte Woche des Monats an.</span><span class="sxs-lookup"><span data-stu-id="c8016-120">Specifies a specific week of the month.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c8016-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8016-121">Remarks</span></span>

<span data-ttu-id="c8016-122">Bei der Entwicklung von Skripts werden die Wochen des Monats mithilfe der [**monthlydowauslöst. weeksofmonth**](monthlydowtrigger-weeksofmonth.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="c8016-122">For scripting development, the weeks of the month are specified using the [**MonthlyDOWTrigger.WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) property.</span></span>

<span data-ttu-id="c8016-123">Bei der C++-Entwicklung werden die Wochen des Monats mithilfe der [**imonthlydowauslöst:: weeksofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="c8016-123">For C++ development, the weeks of the month are specified using the [**IMonthlyDOWTrigger::WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) property.</span></span>

<span data-ttu-id="c8016-124">Wenn Sie die Wochen des Monats angeben, verwenden Sie 1-4, um die ersten vier Wochen des Monats anzugeben, oder verwenden Sie die Zeichenfolge "Last", um die letzte Woche anzugeben, unabhängig von der Woche, an der Sie sich befindet.</span><span class="sxs-lookup"><span data-stu-id="c8016-124">When specifying the weeks of the month, use 1-4 to specify the first four weeks of the month or use the string "Last" to indicate the last week regardless of which week it is.</span></span>

## <a name="examples"></a><span data-ttu-id="c8016-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8016-125">Examples</span></span>

<span data-ttu-id="c8016-126">Im folgenden XML-Code wird ein monatlicher Wochentag definiert, der die Aufgabe am Montag der ersten Woche für jeden Monat des Jahres startet.</span><span class="sxs-lookup"><span data-stu-id="c8016-126">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c8016-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8016-127">Requirements</span></span>



| <span data-ttu-id="c8016-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8016-128">Requirement</span></span> | <span data-ttu-id="c8016-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c8016-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c8016-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8016-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c8016-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8016-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c8016-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8016-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c8016-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8016-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8016-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8016-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8016-135">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="c8016-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c8016-136">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="c8016-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





