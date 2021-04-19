---
title: DaysOfWeek-Element (weeklyscheduletype)
description: Gibt die Wochentage an, an denen der Task ausgeführt wird. | DaysOfWeek-Element (weeklyscheduletype)
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
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
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366424"
---
# <a name="daysofweek-weeklyscheduletype-element"></a><span data-ttu-id="15672-105">DaysOfWeek-Element (weeklyscheduletype)</span><span class="sxs-lookup"><span data-stu-id="15672-105">DaysOfWeek (weeklyScheduleType) Element</span></span>

<span data-ttu-id="15672-106">Gibt die Wochentage an, an denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15672-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="15672-107">Das **DaysOfWeek** -Element wird durch den komplexen Typ " [**weeklyscheduletype**](taskschedulerschema-weeklyscheduletype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="15672-107">The **DaysOfWeek** element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="15672-108">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="15672-108">Parent element</span></span>



| <span data-ttu-id="15672-109">Element</span><span class="sxs-lookup"><span data-stu-id="15672-109">Element</span></span>                                                                                  | <span data-ttu-id="15672-110">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="15672-110">Derived from</span></span>                                                                     | <span data-ttu-id="15672-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15672-111">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="15672-112">**Schedulebyweek**</span><span class="sxs-lookup"><span data-stu-id="15672-112">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="15672-113">**weeklyscheduletype**</span><span class="sxs-lookup"><span data-stu-id="15672-113">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="15672-114">Gibt einen wöchentlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="15672-114">Specifies a weekly schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="15672-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15672-115">Child elements</span></span>



| <span data-ttu-id="15672-116">Element</span><span class="sxs-lookup"><span data-stu-id="15672-116">Element</span></span>                                                                   | <span data-ttu-id="15672-117">type</span><span class="sxs-lookup"><span data-stu-id="15672-117">Type</span></span> | <span data-ttu-id="15672-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15672-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="15672-119">**Am**</span><span class="sxs-lookup"><span data-stu-id="15672-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="15672-120">Gibt an, dass der Task am Freitag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15672-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="15672-121">**Pfingst**</span><span class="sxs-lookup"><span data-stu-id="15672-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="15672-122">Gibt an, dass der Task am Montag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15672-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="15672-123">**Samstag**</span><span class="sxs-lookup"><span data-stu-id="15672-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="15672-124">Gibt an, dass der Task am Samstag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15672-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="15672-125">**Sunday**</span><span class="sxs-lookup"><span data-stu-id="15672-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="15672-126">Gibt an, dass der Task am Sonntag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15672-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="15672-127">**Mitteilte**</span><span class="sxs-lookup"><span data-stu-id="15672-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="15672-128">Gibt an, dass der Task am Donnerstag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15672-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="15672-129">**Mitteilte**</span><span class="sxs-lookup"><span data-stu-id="15672-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="15672-130">Gibt an, dass der Task am Dienstag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15672-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="15672-131">**Mittwochs**</span><span class="sxs-lookup"><span data-stu-id="15672-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="15672-132">Gibt an, dass der Task am Mittwoch ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15672-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="15672-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15672-133">Remarks</span></span>

<span data-ttu-id="15672-134">Die vorherigen untergeordneten Elemente werden durch den komplexen Typ [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="15672-134">The previous child elements are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

<span data-ttu-id="15672-135">Bei der Skripterstellung wird das wöchentliche Intervall mithilfe der [**weeklyghost. weeksinterval**](weeklytrigger-weeksinterval.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="15672-135">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="15672-136">Bei der C++-Entwicklung wird das wöchentliche Intervall mithilfe der [**iweeklyauslöst:: weeksinterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="15672-136">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="15672-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15672-137">Examples</span></span>

<span data-ttu-id="15672-138">Der folgende XML-Code definiert einen täglichen Kalender-Auslösers, der jede Woche einen Task Montag bis Freitag (um 8:00 Uhr) startet.</span><span class="sxs-lookup"><span data-stu-id="15672-138">The following XML defines a daily calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


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



<span data-ttu-id="15672-139">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen wöchentlichen-Auslösers verwendet, finden Sie unter Beispiel für einen [wöchentlichen Beispiel (XML)](weekly-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="15672-139">For a complete example of the XML for a task that uses a weekly trigger, see [Weekly Trigger Example (XML)](weekly-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15672-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15672-140">Requirements</span></span>



| <span data-ttu-id="15672-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15672-141">Requirement</span></span> | <span data-ttu-id="15672-142">Wert</span><span class="sxs-lookup"><span data-stu-id="15672-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="15672-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15672-143">Minimum supported client</span></span><br/> | <span data-ttu-id="15672-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15672-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="15672-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15672-145">Minimum supported server</span></span><br/> | <span data-ttu-id="15672-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15672-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="15672-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15672-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15672-148">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="15672-148">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="15672-149">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="15672-149">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





