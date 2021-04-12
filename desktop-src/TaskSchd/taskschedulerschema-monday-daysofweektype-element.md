---
title: Montag (daysofweektype)-Element
description: Gibt an, dass der Task am Montag ausgeführt wird.
ms.assetid: 2b7ce0c1-c635-47d0-b482-5c93c0028c92
keywords:
- Montag-Element Taskplaner
topic_type:
- apiref
api_name:
- Monday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3967db32a6ccd536e2e389e84de4eec05b333634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478165"
---
# <a name="monday-daysofweektype-element"></a><span data-ttu-id="be065-104">Montag (daysofweektype)-Element</span><span class="sxs-lookup"><span data-stu-id="be065-104">Monday (daysOfWeekType) Element</span></span>

<span data-ttu-id="be065-105">Gibt an, dass der Task am Montag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be065-105">Specifies that the task runs on Monday.</span></span>

``` syntax
<xs:element name="Monday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="be065-106">Das **Montag** -Element wird durch den komplexen Typ " [**weeklyscheduletype**](taskschedulerschema-weeklyscheduletype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="be065-106">The **Monday** element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="be065-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="be065-107">Parent element</span></span>



| <span data-ttu-id="be065-108">Element</span><span class="sxs-lookup"><span data-stu-id="be065-108">Element</span></span>                                                                                                                  | <span data-ttu-id="be065-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="be065-109">Derived from</span></span>                                                             | <span data-ttu-id="be065-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be065-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be065-111">**DaysOfWeek (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="be065-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="be065-112">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="be065-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="be065-113">Gibt die Wochentage an, an denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be065-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="be065-114">**DaysOfWeek (weeklyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="be065-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="be065-115">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="be065-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="be065-116">Gibt die Wochentage an, an denen der Task für einen wöchentlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be065-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="be065-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be065-117">Examples</span></span>

<span data-ttu-id="be065-118">Der folgende XML-Code definiert einen Wochentag-Kalender, der eine Aufgabe am Montag startet.</span><span class="sxs-lookup"><span data-stu-id="be065-118">The following XML defines a day of week calendar that starts a task on Monday.</span></span>


```XML
<DaysOfWeek>
    <Monday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="be065-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be065-119">Requirements</span></span>



| <span data-ttu-id="be065-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be065-120">Requirement</span></span> | <span data-ttu-id="be065-121">Wert</span><span class="sxs-lookup"><span data-stu-id="be065-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="be065-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be065-122">Minimum supported client</span></span><br/> | <span data-ttu-id="be065-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be065-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="be065-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be065-124">Minimum supported server</span></span><br/> | <span data-ttu-id="be065-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be065-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be065-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be065-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be065-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="be065-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="be065-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="be065-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





