---
title: komplexer calendartriggertype-Typ
description: Definiert die untergeordneten Elemente und die Sequenzierungs Informationen für Kalender Elemente.
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- komplexer calendartriggertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f45434fa68b6300157a29318ba257f43bac5992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346732"
---
# <a name="calendartriggertype-complex-type"></a><span data-ttu-id="f4187-104">komplexer calendartriggertype-Typ</span><span class="sxs-lookup"><span data-stu-id="f4187-104">calendarTriggerType Complex Type</span></span>

<span data-ttu-id="f4187-105">Definiert die untergeordneten Elemente und die Sequenzierungs Informationen für Kalender Elemente.</span><span class="sxs-lookup"><span data-stu-id="f4187-105">Defines the child elements and sequencing information for calendar elements.</span></span>

``` syntax
<xs:complexType name="calendarTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:choice>
                    <xs:element name="ScheduleByDay"
                        type="dailyScheduleType"
                     />
                    <xs:element name="ScheduleByWeek"
                        type="weeklyScheduleType"
                     />
                    <xs:element name="ScheduleByMonth"
                        type="monthlyScheduleType"
                     />
                    <xs:element name="ScheduleByMonthDayOfWeek"
                        type="monthlyDayOfWeekScheduleType"
                     />
                </xs:choice>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f4187-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f4187-106">Child elements</span></span>



| <span data-ttu-id="f4187-107">Element</span><span class="sxs-lookup"><span data-stu-id="f4187-107">Element</span></span>                                                                                                      | <span data-ttu-id="f4187-108">type</span><span class="sxs-lookup"><span data-stu-id="f4187-108">Type</span></span>                                                                                                 | <span data-ttu-id="f4187-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4187-109">Description</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4187-110">**Randomdelay**</span><span class="sxs-lookup"><span data-stu-id="f4187-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | <span data-ttu-id="f4187-111">duration</span><span class="sxs-lookup"><span data-stu-id="f4187-111">duration</span></span>                                                                                             | <span data-ttu-id="f4187-112">Enthält die Verzögerungszeit, die der Startzeit des Auslösers zufällig hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f4187-112">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="f4187-113">Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S (z. b. P2DT5S ist eine Verzögerung von 2 Tagen, 5 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="f4187-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span><br/> |
| [<span data-ttu-id="f4187-114">**Schedulebyday**</span><span class="sxs-lookup"><span data-stu-id="f4187-114">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="f4187-115">**dailyscheduletype**</span><span class="sxs-lookup"><span data-stu-id="f4187-115">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="f4187-116">Gibt einen täglichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="f4187-116">Specifies a daily schedule.</span></span> <span data-ttu-id="f4187-117">Der Task wird z. b. täglich, jeden Tag, jeden dritten Tag usw. gestartet.</span><span class="sxs-lookup"><span data-stu-id="f4187-117">For example, the task starts every day, every-other day, every third day, and so on.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="f4187-118">**Schedulebymonth**</span><span class="sxs-lookup"><span data-stu-id="f4187-118">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="f4187-119">**monthlyscheduletype**</span><span class="sxs-lookup"><span data-stu-id="f4187-119">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="f4187-120">Gibt einen monatlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="f4187-120">Specifies a monthly schedule.</span></span> <span data-ttu-id="f4187-121">Der Task wird z. b. um 8:00 Uhr an bestimmten Tagen des Monats in bestimmten Monaten gestartet.</span><span class="sxs-lookup"><span data-stu-id="f4187-121">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="f4187-122">**Schedulebymonthdayof-Woche**</span><span class="sxs-lookup"><span data-stu-id="f4187-122">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="f4187-123">**monthlydayosweekscheduletype**</span><span class="sxs-lookup"><span data-stu-id="f4187-123">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="f4187-124">Gibt einen-Vorgang an, durch den ein Auftrag an einem monatlichen Wochentag gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f4187-124">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span> <span data-ttu-id="f4187-125">Beispielsweise wird die Aufgabe an bestimmten Wochentagen, Wochen des Monats und Monaten des Jahres gestartet.</span><span class="sxs-lookup"><span data-stu-id="f4187-125">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span> <br/>                                               |
| [<span data-ttu-id="f4187-126">**Schedulebyweek**</span><span class="sxs-lookup"><span data-stu-id="f4187-126">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="f4187-127">**weeklyscheduletype**</span><span class="sxs-lookup"><span data-stu-id="f4187-127">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="f4187-128">Gibt einen wöchentlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="f4187-128">Specifies a weekly schedule.</span></span> <span data-ttu-id="f4187-129">Der Task wird z. b. jede Woche um 8:00 Uhr an einem bestimmten Wochentag oder an einem bestimmten Wochentag in der Woche gestartet.</span><span class="sxs-lookup"><span data-stu-id="f4187-129">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span> <br/>                                                              |



## <a name="remarks"></a><span data-ttu-id="f4187-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4187-130">Remarks</span></span>

<span data-ttu-id="f4187-131">Zusätzlich zum untergeordneten-Element, das hier definiert ist, verwendet das [**calendartrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) -Element auch die untergeordneten Elemente, die durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f4187-131">In addition to the child element defined here, the [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) element also uses the child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4187-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4187-132">Requirements</span></span>



| <span data-ttu-id="f4187-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4187-133">Requirement</span></span> | <span data-ttu-id="f4187-134">Wert</span><span class="sxs-lookup"><span data-stu-id="f4187-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f4187-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4187-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f4187-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4187-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f4187-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4187-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f4187-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4187-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4187-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4187-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4187-140">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="f4187-140">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="f4187-141">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="f4187-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





