---
title: September-Element (monthstype)
description: Gibt an, dass der Task im September ausgeführt wird.
ms.assetid: b1ad2221-ca22-4808-bf20-ecf3cbb930f2
keywords:
- September-Element Taskplaner
topic_type:
- apiref
api_name:
- September
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdd7e18ba9ae1cc7653589710fb9529281e84ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957070"
---
# <a name="september-monthstype-element"></a><span data-ttu-id="1c5e5-104">September-Element (monthstype)</span><span class="sxs-lookup"><span data-stu-id="1c5e5-104">September (monthsType) Element</span></span>

<span data-ttu-id="1c5e5-105">Gibt an, dass der Task im September ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c5e5-105">Specifies that the task runs in September.</span></span>

``` syntax
<xs:element name="September">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="1c5e5-106">Das **September** -Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="1c5e5-106">The **September** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1c5e5-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1c5e5-107">Parent element</span></span>



| <span data-ttu-id="1c5e5-108">Element</span><span class="sxs-lookup"><span data-stu-id="1c5e5-108">Element</span></span>                                                                                                          | <span data-ttu-id="1c5e5-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="1c5e5-109">Derived from</span></span>                                                     | <span data-ttu-id="1c5e5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c5e5-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c5e5-111">**Monate (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="1c5e5-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="1c5e5-112">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="1c5e5-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="1c5e5-113">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c5e5-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="1c5e5-114">**Monate (monthlyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="1c5e5-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="1c5e5-115">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="1c5e5-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="1c5e5-116">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c5e5-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="1c5e5-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c5e5-117">Examples</span></span>

<span data-ttu-id="1c5e5-118">Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im September ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c5e5-118">The following XML defines a months calendar that runs the task in September.</span></span>


```XML
<Months>
    <September/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="1c5e5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c5e5-119">Requirements</span></span>



| <span data-ttu-id="1c5e5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c5e5-120">Requirement</span></span> | <span data-ttu-id="1c5e5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1c5e5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1c5e5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c5e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1c5e5-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c5e5-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1c5e5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c5e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1c5e5-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c5e5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c5e5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c5e5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c5e5-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="1c5e5-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1c5e5-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="1c5e5-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





