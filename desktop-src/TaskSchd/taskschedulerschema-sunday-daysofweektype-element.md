---
title: Sunday (daysofweektype)-Element
description: Gibt an, dass der Task am Sonntag ausgeführt wird.
ms.assetid: 856db869-2273-4bb8-88c8-c126bb16c87b
keywords:
- Sunday-Element Taskplaner
topic_type:
- apiref
api_name:
- Sunday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40efba31b392da5959853feeb1cae567cee25cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105351"
---
# <a name="sunday-daysofweektype-element"></a><span data-ttu-id="4527c-104">Sunday (daysofweektype)-Element</span><span class="sxs-lookup"><span data-stu-id="4527c-104">Sunday (daysOfWeekType) Element</span></span>

<span data-ttu-id="4527c-105">Gibt an, dass der Task am Sonntag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4527c-105">Specifies that the task runs on Sunday.</span></span>

``` syntax
<xs:element name="Sunday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="4527c-106">Das **Sunday** -Element wird durch den komplexen Typ [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="4527c-106">The **Sunday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4527c-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="4527c-107">Parent element</span></span>



| <span data-ttu-id="4527c-108">Element</span><span class="sxs-lookup"><span data-stu-id="4527c-108">Element</span></span>                                                                                                                  | <span data-ttu-id="4527c-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="4527c-109">Derived from</span></span>                                                             | <span data-ttu-id="4527c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4527c-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4527c-111">**DaysOfWeek (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="4527c-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="4527c-112">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="4527c-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="4527c-113">Gibt die Wochentage an, an denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4527c-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="4527c-114">**DaysOfWeek (weeklyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="4527c-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="4527c-115">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="4527c-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="4527c-116">Gibt die Wochentage an, an denen der Task für einen wöchentlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4527c-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="4527c-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4527c-117">Examples</span></span>

<span data-ttu-id="4527c-118">Der folgende XML-Code definiert einen Wochentag-Kalender, der eine Aufgabe am Sonntag startet.</span><span class="sxs-lookup"><span data-stu-id="4527c-118">The following XML defines a day of week calendar that starts a task on Sunday.</span></span>


```XML
<DaysOfWeek>
    <Sunday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="4527c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4527c-119">Requirements</span></span>



| <span data-ttu-id="4527c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4527c-120">Requirement</span></span> | <span data-ttu-id="4527c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4527c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4527c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4527c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4527c-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4527c-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4527c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4527c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4527c-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4527c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4527c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4527c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4527c-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="4527c-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4527c-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="4527c-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





