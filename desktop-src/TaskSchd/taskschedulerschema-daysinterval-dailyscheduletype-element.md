---
title: Daysinterval-Element (dailyscheduletype)
description: Gibt das Intervall zwischen den Tagen im Zeitplan an.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- Daysinterval-Element Taskplaner
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97b50581aa4825b31983a234a5eb47ff7b7b7e06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949521"
---
# <a name="daysinterval-dailyscheduletype-element"></a><span data-ttu-id="88827-104">Daysinterval-Element (dailyscheduletype)</span><span class="sxs-lookup"><span data-stu-id="88827-104">DaysInterval (dailyScheduleType) Element</span></span>

<span data-ttu-id="88827-105">Gibt das Intervall zwischen den Tagen im Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="88827-105">Specifies the interval between the days in the schedule.</span></span>

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="88827-106">Das-Element wird durch den komplexen Typ " [**dailyscheduletype**](taskschedulerschema-dailyscheduletype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="88827-106">The element is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="88827-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="88827-107">Parent element</span></span>



| <span data-ttu-id="88827-108">Element</span><span class="sxs-lookup"><span data-stu-id="88827-108">Element</span></span>                                                                                | <span data-ttu-id="88827-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="88827-109">Derived from</span></span>                                                                   | <span data-ttu-id="88827-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88827-110">Description</span></span>                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="88827-111">**Schedulebyday**</span><span class="sxs-lookup"><span data-stu-id="88827-111">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [<span data-ttu-id="88827-112">**dailyscheduletype**</span><span class="sxs-lookup"><span data-stu-id="88827-112">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md) | <span data-ttu-id="88827-113">Gibt einen täglichen Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="88827-113">Specifies a daily schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="88827-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88827-114">Remarks</span></span>

<span data-ttu-id="88827-115">Bei der Skript Entwicklung wird das Tage Intervall für einen täglichen-Befehl von der [**Daily-Eigenschaft. daysinterval**](dailytrigger-daysinterval.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="88827-115">For script development, the days interval for a daily trigger is specified by the [**DailyTrigger.DaysInterval**](dailytrigger-daysinterval.md) property.</span></span>

<span data-ttu-id="88827-116">Bei der C++-Entwicklung wird das Tage Intervall für einen täglichen-Befehl durch die [**idaily-Funktion::D aysinterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="88827-116">For C++ development, the days interval for a daily trigger is specified by the [**IDailyTrigger::DaysInterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="88827-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88827-117">Examples</span></span>

<span data-ttu-id="88827-118">Der folgende XML-Code definiert einen täglichen Kalender--Auslösers, der die Aufgabe täglich startet.</span><span class="sxs-lookup"><span data-stu-id="88827-118">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="88827-119">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen täglichen Zeitplan angibt, finden Sie unter Beispiel für das [tägliche Beispiel (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="88827-119">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88827-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88827-120">Requirements</span></span>



| <span data-ttu-id="88827-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88827-121">Requirement</span></span> | <span data-ttu-id="88827-122">Wert</span><span class="sxs-lookup"><span data-stu-id="88827-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="88827-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88827-123">Minimum supported client</span></span><br/> | <span data-ttu-id="88827-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88827-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="88827-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88827-125">Minimum supported server</span></span><br/> | <span data-ttu-id="88827-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88827-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88827-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88827-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88827-128">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="88827-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="88827-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="88827-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





