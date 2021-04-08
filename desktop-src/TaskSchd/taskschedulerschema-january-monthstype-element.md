---
title: Januar-Element (monthstype)
description: Gibt an, dass der Task im Januar ausgeführt wird.
ms.assetid: 3a0dde08-f2de-4ff4-9c5a-4368ff7a0e2c
keywords:
- Taskplaner Januar-Element
topic_type:
- apiref
api_name:
- January
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e72967f0fb6addb70af1792ffabf0457b1d20c29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740441"
---
# <a name="january-monthstype-element"></a><span data-ttu-id="eaaff-104">Januar-Element (monthstype)</span><span class="sxs-lookup"><span data-stu-id="eaaff-104">January (monthsType) Element</span></span>

<span data-ttu-id="eaaff-105">Gibt an, dass der Task im Januar ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eaaff-105">Specifies that the task runs in January.</span></span>

``` syntax
<xs:element name="January">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="eaaff-106">Das **Januar** -Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="eaaff-106">The **January** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="eaaff-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="eaaff-107">Parent element</span></span>



| <span data-ttu-id="eaaff-108">Element</span><span class="sxs-lookup"><span data-stu-id="eaaff-108">Element</span></span>                                                                                                          | <span data-ttu-id="eaaff-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="eaaff-109">Derived from</span></span>                                                     | <span data-ttu-id="eaaff-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eaaff-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eaaff-111">**Monate (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="eaaff-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="eaaff-112">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="eaaff-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="eaaff-113">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eaaff-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="eaaff-114">**Monate (monthlyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="eaaff-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="eaaff-115">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="eaaff-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="eaaff-116">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eaaff-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="eaaff-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eaaff-117">Examples</span></span>

<span data-ttu-id="eaaff-118">Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im Januar ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eaaff-118">The following XML defines a months calendar that runs the task in January.</span></span>


```XML
<Months>
    <January/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="eaaff-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaaff-119">Requirements</span></span>



| <span data-ttu-id="eaaff-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eaaff-120">Requirement</span></span> | <span data-ttu-id="eaaff-121">Wert</span><span class="sxs-lookup"><span data-stu-id="eaaff-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eaaff-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eaaff-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eaaff-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaaff-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eaaff-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eaaff-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eaaff-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaaff-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eaaff-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eaaff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaaff-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="eaaff-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="eaaff-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="eaaff-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





