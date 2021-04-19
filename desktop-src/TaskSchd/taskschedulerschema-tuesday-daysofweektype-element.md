---
title: Dienstag (daysofweektype)-Element
description: Gibt an, dass der Task am Dienstag ausgeführt wird.
ms.assetid: 588608e9-33f9-405d-8b4b-35f11ab403db
keywords:
- Dienstag-Element Taskplaner
topic_type:
- apiref
api_name:
- Tuesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ed48803d0cad5dae409202869c600e7e7a60643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345936"
---
# <a name="tuesday-daysofweektype-element"></a><span data-ttu-id="170e7-104">Dienstag (daysofweektype)-Element</span><span class="sxs-lookup"><span data-stu-id="170e7-104">Tuesday (daysOfWeekType) Element</span></span>

<span data-ttu-id="170e7-105">Gibt an, dass der Task am Dienstag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="170e7-105">Specifies that the task runs on Tuesday.</span></span>

``` syntax
<xs:element name="Tuesday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="170e7-106">Das **Dienstag** -Element wird durch den komplexen Typ [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="170e7-106">The **Tuesday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="170e7-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="170e7-107">Parent element</span></span>



| <span data-ttu-id="170e7-108">Element</span><span class="sxs-lookup"><span data-stu-id="170e7-108">Element</span></span>                                                                                                                  | <span data-ttu-id="170e7-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="170e7-109">Derived from</span></span>                                                             | <span data-ttu-id="170e7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="170e7-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="170e7-111">**DaysOfWeek (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="170e7-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="170e7-112">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="170e7-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="170e7-113">Gibt die Wochentage an, an denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="170e7-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="170e7-114">**DaysOfWeek (weeklyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="170e7-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="170e7-115">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="170e7-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="170e7-116">Gibt die Wochentage an, an denen der Task für einen wöchentlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="170e7-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="170e7-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="170e7-117">Examples</span></span>

<span data-ttu-id="170e7-118">Der folgende XML-Code definiert einen Wochentag-Kalender, der eine Aufgabe am Dienstag startet.</span><span class="sxs-lookup"><span data-stu-id="170e7-118">The following XML defines a day of week calendar that starts a task on Tuesday.</span></span>


```XML
<DaysOfWeek>
    <Tuesday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="170e7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="170e7-119">Requirements</span></span>



| <span data-ttu-id="170e7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="170e7-120">Requirement</span></span> | <span data-ttu-id="170e7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="170e7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="170e7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="170e7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="170e7-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="170e7-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="170e7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="170e7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="170e7-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="170e7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="170e7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="170e7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="170e7-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="170e7-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="170e7-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="170e7-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





