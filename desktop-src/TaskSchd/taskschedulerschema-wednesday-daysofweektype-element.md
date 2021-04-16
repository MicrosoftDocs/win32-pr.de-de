---
title: Wednesday (daysofweektype)-Element
description: Gibt an, dass der Task am Mittwoch ausgeführt wird.
ms.assetid: 6d4f52e2-4390-4f9d-bab8-813bd0851582
keywords:
- Mittwoch-Element Taskplaner
topic_type:
- apiref
api_name:
- Wednesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f9d8c60cb7cea818cc0b096e99e97e8f1490d47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518482"
---
# <a name="wednesday-daysofweektype-element"></a><span data-ttu-id="49ecd-104">Wednesday (daysofweektype)-Element</span><span class="sxs-lookup"><span data-stu-id="49ecd-104">Wednesday (daysOfWeekType) Element</span></span>

<span data-ttu-id="49ecd-105">Gibt an, dass der Task am Mittwoch ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49ecd-105">Specifies that the task runs on Wednesday.</span></span>

``` syntax
<xs:element name="Wednesday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="49ecd-106">Das **Mittwoch** -Element wird durch den komplexen Typ [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="49ecd-106">The **Wednesday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="49ecd-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="49ecd-107">Parent element</span></span>



| <span data-ttu-id="49ecd-108">Element</span><span class="sxs-lookup"><span data-stu-id="49ecd-108">Element</span></span>                                                                                                                  | <span data-ttu-id="49ecd-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="49ecd-109">Derived from</span></span>                                                             | <span data-ttu-id="49ecd-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49ecd-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49ecd-111">**DaysOfWeek (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="49ecd-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="49ecd-112">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="49ecd-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="49ecd-113">Gibt die Wochentage an, an denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49ecd-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="49ecd-114">**DaysOfWeek (weeklyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="49ecd-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="49ecd-115">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="49ecd-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="49ecd-116">Gibt die Wochentage an, an denen der Task für einen wöchentlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49ecd-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="49ecd-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49ecd-117">Examples</span></span>

<span data-ttu-id="49ecd-118">Der folgende XML-Code definiert einen Wochentag-Kalender, der eine Aufgabe am Mittwoch startet.</span><span class="sxs-lookup"><span data-stu-id="49ecd-118">The following XML defines a day of week calendar that starts a task on Wednesday.</span></span>


```XML
<DaysOfWeek>
    <Wednesday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="49ecd-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49ecd-119">Requirements</span></span>



| <span data-ttu-id="49ecd-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49ecd-120">Requirement</span></span> | <span data-ttu-id="49ecd-121">Wert</span><span class="sxs-lookup"><span data-stu-id="49ecd-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49ecd-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49ecd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="49ecd-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49ecd-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="49ecd-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49ecd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="49ecd-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49ecd-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49ecd-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49ecd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ecd-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="49ecd-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="49ecd-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="49ecd-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





