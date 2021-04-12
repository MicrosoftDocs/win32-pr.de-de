---
title: Friday (daysofweektype)-Element
description: Gibt an, dass der Task am Freitag ausgeführt wird.
ms.assetid: bff85911-d354-4954-8c69-7b6f2ca312d3
keywords:
- Friday-Element Taskplaner
topic_type:
- apiref
api_name:
- Friday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 951142e7e925ea71ef1f833be4421351aaea3b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105224"
---
# <a name="friday-daysofweektype-element"></a><span data-ttu-id="d1fb3-104">Friday (daysofweektype)-Element</span><span class="sxs-lookup"><span data-stu-id="d1fb3-104">Friday (daysOfWeekType) Element</span></span>

<span data-ttu-id="d1fb3-105">Gibt an, dass der Task am Freitag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1fb3-105">Specifies that the task runs on Friday.</span></span>

``` syntax
<xs:element name="Friday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="d1fb3-106">Das **Friday** -Element wird durch den komplexen Typ [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="d1fb3-106">The **Friday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d1fb3-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d1fb3-107">Parent element</span></span>



| <span data-ttu-id="d1fb3-108">Element</span><span class="sxs-lookup"><span data-stu-id="d1fb3-108">Element</span></span>                                                                                                                  | <span data-ttu-id="d1fb3-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="d1fb3-109">Derived from</span></span>                                                             | <span data-ttu-id="d1fb3-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1fb3-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1fb3-111">**DaysOfWeek (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="d1fb3-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="d1fb3-112">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="d1fb3-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="d1fb3-113">Gibt die Wochentage an, an denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1fb3-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="d1fb3-114">**DaysOfWeek (weeklyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="d1fb3-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="d1fb3-115">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="d1fb3-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="d1fb3-116">Gibt die Wochentage an, an denen der Task für einen wöchentlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1fb3-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="d1fb3-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1fb3-117">Examples</span></span>

<span data-ttu-id="d1fb3-118">Der folgende XML-Code definiert einen Wochentag-Kalender, der eine Aufgabe am Freitag startet.</span><span class="sxs-lookup"><span data-stu-id="d1fb3-118">The following XML defines a day of week calendar that starts a task on Friday.</span></span>


```XML
<DaysOfWeek>
    <Friday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="d1fb3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1fb3-119">Requirements</span></span>



| <span data-ttu-id="d1fb3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1fb3-120">Requirement</span></span> | <span data-ttu-id="d1fb3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d1fb3-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d1fb3-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1fb3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d1fb3-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1fb3-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d1fb3-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1fb3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d1fb3-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1fb3-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1fb3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1fb3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1fb3-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="d1fb3-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d1fb3-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d1fb3-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





