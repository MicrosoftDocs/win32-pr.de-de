---
title: CalendarTriggerType Complex Type
description: Definiert die untergeordneten Elemente und Sequenzierungsinformationen für Kalenderelemente.
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- komplexer calendarTriggerType-Taskplaner
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a891f60d46f8826faed1cc4b95e4c55f6efa4f7f
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734165"
---
# <a name="calendartriggertype-complex-type"></a><span data-ttu-id="646ae-104">CalendarTriggerType Complex Type</span><span class="sxs-lookup"><span data-stu-id="646ae-104">calendarTriggerType Complex Type</span></span>

<span data-ttu-id="646ae-105">Definiert die untergeordneten Elemente und Sequenzierungsinformationen für Kalenderelemente.</span><span class="sxs-lookup"><span data-stu-id="646ae-105">Defines the child elements and sequencing information for calendar elements.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="646ae-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="646ae-106">Child elements</span></span>



| <span data-ttu-id="646ae-107">Element</span><span class="sxs-lookup"><span data-stu-id="646ae-107">Element</span></span>                                                                                                      | <span data-ttu-id="646ae-108">Typ</span><span class="sxs-lookup"><span data-stu-id="646ae-108">Type</span></span>                                                                                                 | <span data-ttu-id="646ae-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="646ae-109">Description</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="646ae-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="646ae-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | <span data-ttu-id="646ae-111">duration</span><span class="sxs-lookup"><span data-stu-id="646ae-111">duration</span></span>                                                                                             | <span data-ttu-id="646ae-112">Enthält die Verzögerungszeit, die zufällig zur Startzeit des Triggers hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="646ae-112">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="646ae-113">Das Format für diese Zeichenfolge ist (z. B. `P<days>DT<hours>H<minutes>M<seconds>S` ist P2DT5S eine Verzögerung von 2 Tag, 5 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="646ae-113">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span><br/> |
| [<span data-ttu-id="646ae-114">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="646ae-114">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="646ae-115">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="646ae-115">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="646ae-116">Gibt einen täglichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="646ae-116">Specifies a daily schedule.</span></span> <span data-ttu-id="646ae-117">Die Aufgabe wird beispielsweise jeden Tag, jeden anderen Tag, jeden dritten Tag und so weiter gestartet.</span><span class="sxs-lookup"><span data-stu-id="646ae-117">For example, the task starts every day, every-other day, every third day, and so on.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="646ae-118">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="646ae-118">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="646ae-119">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="646ae-119">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="646ae-120">Gibt einen monatlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="646ae-120">Specifies a monthly schedule.</span></span> <span data-ttu-id="646ae-121">Beispielsweise beginnt die Aufgabe an bestimmten Tagen des Monats an bestimmten Monaten um 8:00 Uhr.</span><span class="sxs-lookup"><span data-stu-id="646ae-121">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="646ae-122">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="646ae-122">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="646ae-123">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="646ae-123">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="646ae-124">Gibt einen Trigger an, der einen Auftrag nach einem monatlichen Wochentag startet.</span><span class="sxs-lookup"><span data-stu-id="646ae-124">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span> <span data-ttu-id="646ae-125">Die Aufgabe beginnt z. B. an bestimmten Wochentagen, Wochen des Monats und Monaten des Jahres.</span><span class="sxs-lookup"><span data-stu-id="646ae-125">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span> <br/>                                               |
| [<span data-ttu-id="646ae-126">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="646ae-126">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="646ae-127">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="646ae-127">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="646ae-128">Gibt einen wöchentlichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="646ae-128">Specifies a weekly schedule.</span></span> <span data-ttu-id="646ae-129">Die Aufgabe beginnt beispielsweise jede Woche um 8:00 Uhr an einem bestimmten Wochentag oder jede andere Woche an einem bestimmten Wochentag.</span><span class="sxs-lookup"><span data-stu-id="646ae-129">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span> <br/>                                                              |



## <a name="remarks"></a><span data-ttu-id="646ae-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="646ae-130">Remarks</span></span>

<span data-ttu-id="646ae-131">Zusätzlich zum hier definierten untergeordneten Element verwendet das [**CalendarTrigger-Element**](taskschedulerschema-calendartrigger-triggergroup-element.md) auch die untergeordneten Elemente, die vom komplexen [**triggerBaseType-Typ**](taskschedulerschema-triggerbasetype-complextype.md) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="646ae-131">In addition to the child element defined here, the [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) element also uses the child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="646ae-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="646ae-132">Requirements</span></span>



| <span data-ttu-id="646ae-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="646ae-133">Requirement</span></span> | <span data-ttu-id="646ae-134">Wert</span><span class="sxs-lookup"><span data-stu-id="646ae-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="646ae-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="646ae-135">Minimum supported client</span></span><br/> | <span data-ttu-id="646ae-136">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="646ae-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="646ae-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="646ae-137">Minimum supported server</span></span><br/> | <span data-ttu-id="646ae-138">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="646ae-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="646ae-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="646ae-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="646ae-140">komplexe Schematypen Taskplaner</span><span class="sxs-lookup"><span data-stu-id="646ae-140">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="646ae-141">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="646ae-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





