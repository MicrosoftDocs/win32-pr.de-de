---
title: Schedulebymonth (calendartriggertype)-Element
description: Gibt einen monatlichen Zeitplan an.
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- Schedulebymonth-Element Taskplaner
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6fda84a1cd4373f7988fa66a5ad70c97dd371d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105362"
---
# <a name="schedulebymonth-calendartriggertype-element"></a><span data-ttu-id="d3437-104">Schedulebymonth (calendartriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="d3437-104">ScheduleByMonth (calendarTriggerType) Element</span></span>

<span data-ttu-id="d3437-105">Gibt einen monatlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="d3437-105">Specifies a monthly schedule.</span></span> <span data-ttu-id="d3437-106">Der Task wird z. b. um 8:00 Uhr an bestimmten Tagen des Monats in bestimmten Monaten gestartet.</span><span class="sxs-lookup"><span data-stu-id="d3437-106">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span>

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

<span data-ttu-id="d3437-107">Das **schedulebymonth** -Element wird durch den komplexen Typ [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="d3437-107">The **ScheduleByMonth** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d3437-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d3437-108">Parent element</span></span>



| <span data-ttu-id="d3437-109">Element</span><span class="sxs-lookup"><span data-stu-id="d3437-109">Element</span></span>                                                                             | <span data-ttu-id="d3437-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="d3437-110">Derived from</span></span>                                                                       | <span data-ttu-id="d3437-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3437-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3437-112">**Calendarausgelöst**</span><span class="sxs-lookup"><span data-stu-id="d3437-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="d3437-113">**calendartriggertype**</span><span class="sxs-lookup"><span data-stu-id="d3437-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="d3437-114">Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.</span><span class="sxs-lookup"><span data-stu-id="d3437-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="d3437-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3437-115">Child elements</span></span>



| <span data-ttu-id="d3437-116">Element</span><span class="sxs-lookup"><span data-stu-id="d3437-116">Element</span></span>                                                                                                  | <span data-ttu-id="d3437-117">type</span><span class="sxs-lookup"><span data-stu-id="d3437-117">Type</span></span>                                                                       | <span data-ttu-id="d3437-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3437-118">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="d3437-119">**DaysOfMonth (monthlyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="d3437-119">**DaysOfMonth (monthlyScheduleType)**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="d3437-120">**daysofmonthtype**</span><span class="sxs-lookup"><span data-stu-id="d3437-120">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="d3437-121">Gibt die Tage des Monats an, in denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3437-121">Specifies the days of the month during which the task runs.</span></span><br/>  |
| [<span data-ttu-id="d3437-122">**Monate (monthlyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="d3437-122">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="d3437-123">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="d3437-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="d3437-124">Gibt die Monate des Jahres an, in dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3437-124">Specifies the months of the year during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d3437-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3437-125">Remarks</span></span>

<span data-ttu-id="d3437-126">Die Uhrzeit, zu der die Aufgabe gestartet wird, wird durch das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3437-126">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="d3437-127">Bei der Skript Entwicklung wird ein monatlicher-Auslösung mit dem [**Monthly-Auslöserobjekt**](monthlytrigger.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3437-127">For script development, a monthly trigger is specified using the [**MonthlyTrigger**](monthlytrigger.md) object.</span></span>

<span data-ttu-id="d3437-128">Bei der C++-Entwicklung wird ein monatlicher-Auslösers mithilfe der [**imonthly-**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) Schnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3437-128">For C++ development, a monthly trigger is specified using the [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) interface.</span></span>

<span data-ttu-id="d3437-129">Die unten aufgeführten untergeordneten Elemente werden von den komplexen Elementtypen [**monthlyscheduletype**](taskschedulerschema-monthlyscheduletype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="d3437-129">The child elements listed below are defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="d3437-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3437-130">Examples</span></span>

<span data-ttu-id="d3437-131">Der folgende XML-Code definiert einen monatlichen Kalender-, der einen Task (um 8:00 Uhr) am 1. und 15. Tag eines jeden Monats des Jahres startet.</span><span class="sxs-lookup"><span data-stu-id="d3437-131">The following XML defines a monthly calendar trigger that starts a task ( at 8:00 AM) on the 1st and 15th day of every month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>
            <Day>15</Day>
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
        </Months>
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="d3437-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3437-132">Requirements</span></span>



| <span data-ttu-id="d3437-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3437-133">Requirement</span></span> | <span data-ttu-id="d3437-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d3437-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d3437-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3437-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d3437-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3437-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d3437-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3437-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d3437-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3437-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3437-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3437-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3437-140">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="d3437-140">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d3437-141">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d3437-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





