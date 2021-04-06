---
title: Saturday (daysofweektype)-Element
description: Gibt an, dass der Task am Samstag ausgeführt wird.
ms.assetid: def26a72-c143-466a-b5b0-6105078afffa
keywords:
- Saturday-Element Taskplaner
topic_type:
- apiref
api_name:
- Saturday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b5f7cb36002b2add64cdea541caa2fd28df37ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742896"
---
# <a name="saturday-daysofweektype-element"></a><span data-ttu-id="33b1e-104">Saturday (daysofweektype)-Element</span><span class="sxs-lookup"><span data-stu-id="33b1e-104">Saturday (daysOfWeekType) Element</span></span>

<span data-ttu-id="33b1e-105">Gibt an, dass der Task am Samstag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33b1e-105">Specifies that the task runs on Saturday.</span></span>

``` syntax
<xs:element name="Saturday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="33b1e-106">Das **Saturday** -Element wird durch den komplexen Typ [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="33b1e-106">The **Saturday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="33b1e-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="33b1e-107">Parent element</span></span>



| <span data-ttu-id="33b1e-108">Element</span><span class="sxs-lookup"><span data-stu-id="33b1e-108">Element</span></span>                                                                                                                  | <span data-ttu-id="33b1e-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="33b1e-109">Derived from</span></span>                                                             | <span data-ttu-id="33b1e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33b1e-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33b1e-111">**DaysOfWeek (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="33b1e-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="33b1e-112">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="33b1e-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="33b1e-113">Gibt die Wochentage an, an denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33b1e-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="33b1e-114">**DaysOfWeek (weeklyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="33b1e-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="33b1e-115">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="33b1e-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="33b1e-116">Gibt die Wochentage an, an denen der Task für einen wöchentlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33b1e-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="33b1e-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33b1e-117">Examples</span></span>

<span data-ttu-id="33b1e-118">Der folgende XML-Code definiert einen Wochentag-Kalender, der eine Aufgabe am Samstag startet.</span><span class="sxs-lookup"><span data-stu-id="33b1e-118">The following XML defines a day of week calendar that starts a task on Saturday.</span></span>


```XML
<DaysOfWeek>
    <Saturday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="33b1e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33b1e-119">Requirements</span></span>



| <span data-ttu-id="33b1e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33b1e-120">Requirement</span></span> | <span data-ttu-id="33b1e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="33b1e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="33b1e-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33b1e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="33b1e-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33b1e-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="33b1e-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33b1e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="33b1e-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33b1e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="33b1e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33b1e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33b1e-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="33b1e-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="33b1e-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="33b1e-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





