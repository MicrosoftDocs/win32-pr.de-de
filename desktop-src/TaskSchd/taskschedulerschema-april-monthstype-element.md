---
title: April (monthstype)-Element
description: Gibt an, dass der Task im April ausgeführt wird.
ms.assetid: b642e142-0acc-4b88-a86a-5d539613ead6
keywords:
- April-Element Taskplaner
topic_type:
- apiref
api_name:
- April
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecde82e5091adf51c2e42b682e36dba6d45e85c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105885"
---
# <a name="april-monthstype-element"></a><span data-ttu-id="485d8-104">April (monthstype)-Element</span><span class="sxs-lookup"><span data-stu-id="485d8-104">April (monthsType) Element</span></span>

<span data-ttu-id="485d8-105">Gibt an, dass der Task im April ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="485d8-105">Specifies that the task runs in April.</span></span>

``` syntax
<xs:element name="April">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="485d8-106">Das **April** -Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="485d8-106">The **April** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="485d8-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="485d8-107">Parent element</span></span>



| <span data-ttu-id="485d8-108">Element</span><span class="sxs-lookup"><span data-stu-id="485d8-108">Element</span></span>                                                                                                          | <span data-ttu-id="485d8-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="485d8-109">Derived from</span></span>                                                     | <span data-ttu-id="485d8-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="485d8-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="485d8-111">**Monate (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="485d8-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="485d8-112">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="485d8-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="485d8-113">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="485d8-113">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |
| [<span data-ttu-id="485d8-114">**Monate (monthlyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="485d8-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="485d8-115">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="485d8-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="485d8-116">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="485d8-116">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="485d8-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="485d8-117">Examples</span></span>

<span data-ttu-id="485d8-118">Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im April ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="485d8-118">The following XML defines a months calendar that runs the task in April.</span></span>


```XML
<Months>
    <April/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="485d8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="485d8-119">Requirements</span></span>



| <span data-ttu-id="485d8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="485d8-120">Requirement</span></span> | <span data-ttu-id="485d8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="485d8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="485d8-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="485d8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="485d8-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="485d8-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="485d8-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="485d8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="485d8-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="485d8-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="485d8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="485d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="485d8-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="485d8-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="485d8-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="485d8-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





