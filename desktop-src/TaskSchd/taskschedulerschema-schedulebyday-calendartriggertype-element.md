---
title: Schedulebyday (calendartriggertype)-Element
description: Gibt einen täglichen Zeitplan an.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- täglicher Taskplaner des Auslösers, XML-Element
- Schedulebyday-Element Taskplaner
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 614777ede63605dc7ed6936bda952c6071bda371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956958"
---
# <a name="schedulebyday-calendartriggertype-element"></a><span data-ttu-id="91087-105">Schedulebyday (calendartriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="91087-105">ScheduleByDay (calendarTriggerType) Element</span></span>

<span data-ttu-id="91087-106">Gibt einen täglichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="91087-106">Specifies a daily schedule.</span></span> <span data-ttu-id="91087-107">Der Task wird z. b. täglich um 8:00 Uhr täglich, täglich, an jedem dritten Tag usw. gestartet.</span><span class="sxs-lookup"><span data-stu-id="91087-107">For example, the task starts at 8:00 AM every day, every-other day, every third day, and so on.</span></span>

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

<span data-ttu-id="91087-108">Das **schedulebyday** -Element wird durch den komplexen Typ [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="91087-108">The **ScheduleByDay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="91087-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="91087-109">Parent element</span></span>



| <span data-ttu-id="91087-110">Element</span><span class="sxs-lookup"><span data-stu-id="91087-110">Element</span></span>                                                                             | <span data-ttu-id="91087-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="91087-111">Derived from</span></span>                                                                       | <span data-ttu-id="91087-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91087-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91087-113">**Calendarausgelöst**</span><span class="sxs-lookup"><span data-stu-id="91087-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="91087-114">**calendartriggertype**</span><span class="sxs-lookup"><span data-stu-id="91087-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="91087-115">Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.</span><span class="sxs-lookup"><span data-stu-id="91087-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="91087-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91087-116">Child elements</span></span>



| <span data-ttu-id="91087-117">Element</span><span class="sxs-lookup"><span data-stu-id="91087-117">Element</span></span>                                                                            | <span data-ttu-id="91087-118">type</span><span class="sxs-lookup"><span data-stu-id="91087-118">Type</span></span>             | <span data-ttu-id="91087-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91087-119">Description</span></span>                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="91087-120">**Daysinterval**</span><span class="sxs-lookup"><span data-stu-id="91087-120">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | <span data-ttu-id="91087-121">**unsignedByte**</span><span class="sxs-lookup"><span data-stu-id="91087-121">**unsignedByte**</span></span> | <span data-ttu-id="91087-122">Gibt das Intervall zwischen den Tagen im Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="91087-122">Specifies the interval between the days in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="91087-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91087-123">Remarks</span></span>

<span data-ttu-id="91087-124">Das zuvor aufgeführte untergeordnete Element wird von den komplexen Elementtypen [**dailyscheduletype**](taskschedulerschema-dailyscheduletype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="91087-124">The child element listed previously is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="91087-125">Die Uhrzeit, zu der die Aufgabe gestartet wird, wird durch das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="91087-125">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="91087-126">Bei der Skripterstellung wird ein täglicher-Fehler mithilfe des [**Daily-auslöserobjekts**](weeklytrigger.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="91087-126">For scripting development, a daily trigger is specified using the [**DailyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="91087-127">Bei der C++-Entwicklung wird ein täglicher-Fehler mithilfe der [**idaily-**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) Schnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="91087-127">For C++ development, a daily trigger is specified using the [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="91087-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91087-128">Examples</span></span>

<span data-ttu-id="91087-129">Der folgende XML-Code definiert einen täglichen Kalender--Auslösers, der die Aufgabe täglich startet.</span><span class="sxs-lookup"><span data-stu-id="91087-129">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="91087-130">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen täglichen Zeitplan angibt, finden Sie unter Beispiel für das [tägliche Beispiel (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="91087-130">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91087-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91087-131">Requirements</span></span>



| <span data-ttu-id="91087-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91087-132">Requirement</span></span> | <span data-ttu-id="91087-133">Wert</span><span class="sxs-lookup"><span data-stu-id="91087-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="91087-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91087-134">Minimum supported client</span></span><br/> | <span data-ttu-id="91087-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91087-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="91087-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91087-136">Minimum supported server</span></span><br/> | <span data-ttu-id="91087-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91087-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91087-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91087-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91087-139">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="91087-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="91087-140">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="91087-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





