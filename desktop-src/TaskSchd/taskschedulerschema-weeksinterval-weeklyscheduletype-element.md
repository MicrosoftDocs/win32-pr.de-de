---
title: Weeksinterval-Element (weeklyscheduletype)
description: Gibt das Intervall zwischen den Wochen im Zeitplan an.
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- Weeksinterval-Element Taskplaner
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747ca4b73ff18bdb3e29d8b909d72b8d2367d89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392133"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a><span data-ttu-id="672b6-104">Weeksinterval-Element (weeklyscheduletype)</span><span class="sxs-lookup"><span data-stu-id="672b6-104">WeeksInterval (weeklyScheduleType) Element</span></span>

<span data-ttu-id="672b6-105">Gibt das Intervall zwischen den Wochen im Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="672b6-105">Specifies the interval between the weeks in the schedule.</span></span>

``` syntax
<xs:element name="WeeksInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="52"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="672b6-106">Das-Element wird durch den komplexen Typ " [**weeklyscheduletype**](taskschedulerschema-weeklyscheduletype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="672b6-106">The element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="672b6-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="672b6-107">Parent element</span></span>



| <span data-ttu-id="672b6-108">Element</span><span class="sxs-lookup"><span data-stu-id="672b6-108">Element</span></span>                                                                                  | <span data-ttu-id="672b6-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="672b6-109">Derived from</span></span>                                                                     | <span data-ttu-id="672b6-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="672b6-110">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="672b6-111">**Schedulebyweek**</span><span class="sxs-lookup"><span data-stu-id="672b6-111">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="672b6-112">**weeklyscheduletype**</span><span class="sxs-lookup"><span data-stu-id="672b6-112">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="672b6-113">Gibt einen wöchentlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="672b6-113">Specifies a weekly schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="672b6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="672b6-114">Remarks</span></span>

<span data-ttu-id="672b6-115">Bei der Skripterstellung wird das wöchentliche Intervall mithilfe der [**weeklyghost. weeksinterval**](weeklytrigger-weeksinterval.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="672b6-115">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="672b6-116">Bei der C++-Entwicklung wird das wöchentliche Intervall mithilfe der [**iweeklyauslöst:: weeksinterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="672b6-116">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="672b6-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="672b6-117">Examples</span></span>

<span data-ttu-id="672b6-118">Der folgende XML-Code definiert einen wöchentlichen Kalender--Auslösers, der jede Woche einen Task Montag bis Freitag (um 8:00 Uhr) startet.</span><span class="sxs-lookup"><span data-stu-id="672b6-118">The following XML defines a weekly calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="672b6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="672b6-119">Requirements</span></span>



| <span data-ttu-id="672b6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="672b6-120">Requirement</span></span> | <span data-ttu-id="672b6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="672b6-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="672b6-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="672b6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="672b6-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="672b6-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="672b6-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="672b6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="672b6-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="672b6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="672b6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="672b6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="672b6-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="672b6-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="672b6-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="672b6-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





