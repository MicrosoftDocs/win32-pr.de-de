---
title: Dezember-Element (monthstype)
description: Gibt an, dass der Task im Dezember ausgeführt wird.
ms.assetid: 42f3cfb2-8e82-46a0-b3ef-42e83d329124
keywords:
- Dezember-Element Taskplaner
topic_type:
- apiref
api_name:
- December
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c907262fe67a0529917d085583465eb97f94c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340379"
---
# <a name="december-monthstype-element"></a><span data-ttu-id="316e7-104">Dezember-Element (monthstype)</span><span class="sxs-lookup"><span data-stu-id="316e7-104">December (monthsType) Element</span></span>

<span data-ttu-id="316e7-105">Gibt an, dass der Task im Dezember ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="316e7-105">Specifies that the task runs in December.</span></span>

``` syntax
<xs:element name="December">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="316e7-106">Das **Dezember** -Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="316e7-106">The **December** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="316e7-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="316e7-107">Parent element</span></span>



| <span data-ttu-id="316e7-108">Element</span><span class="sxs-lookup"><span data-stu-id="316e7-108">Element</span></span>                                                                                                          | <span data-ttu-id="316e7-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="316e7-109">Derived from</span></span>                                                     | <span data-ttu-id="316e7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="316e7-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="316e7-111">**Monate (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="316e7-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="316e7-112">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="316e7-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="316e7-113">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="316e7-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="316e7-114">**Monate (monthlyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="316e7-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="316e7-115">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="316e7-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="316e7-116">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="316e7-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="316e7-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="316e7-117">Examples</span></span>

<span data-ttu-id="316e7-118">Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im Dezember ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="316e7-118">The following XML defines a months calendar that runs the task in December.</span></span>


```XML
<Months>
    <December/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="316e7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="316e7-119">Requirements</span></span>



| <span data-ttu-id="316e7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="316e7-120">Requirement</span></span> | <span data-ttu-id="316e7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="316e7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="316e7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="316e7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="316e7-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="316e7-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="316e7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="316e7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="316e7-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="316e7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="316e7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="316e7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="316e7-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="316e7-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="316e7-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="316e7-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





