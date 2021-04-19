---
title: Mai-Element (monthstype)
description: Gibt an, dass der Task im Mai ausgeführt wird.
ms.assetid: 1fcc3eb7-6500-4ba3-b146-14d169d9b445
keywords:
- Mai-Element Taskplaner
topic_type:
- apiref
api_name:
- May
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d3f0c107124aa2c87672f63a469857f3795e13c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346518"
---
# <a name="may-monthstype-element"></a><span data-ttu-id="4e8f1-104">Mai-Element (monthstype)</span><span class="sxs-lookup"><span data-stu-id="4e8f1-104">May (monthsType) Element</span></span>

<span data-ttu-id="4e8f1-105">Gibt an, dass der Task im Mai ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e8f1-105">Specifies that the task runs in May.</span></span>

``` syntax
<xs:element name="May">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="4e8f1-106">Das " **May** "-Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="4e8f1-106">The **May** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4e8f1-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="4e8f1-107">Parent element</span></span>



| <span data-ttu-id="4e8f1-108">Element</span><span class="sxs-lookup"><span data-stu-id="4e8f1-108">Element</span></span>                                                                                                          | <span data-ttu-id="4e8f1-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="4e8f1-109">Derived from</span></span>                                                     | <span data-ttu-id="4e8f1-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e8f1-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e8f1-111">**Monate (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="4e8f1-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="4e8f1-112">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="4e8f1-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="4e8f1-113">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e8f1-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="4e8f1-114">**Monate (monthlyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="4e8f1-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="4e8f1-115">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="4e8f1-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="4e8f1-116">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e8f1-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="4e8f1-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e8f1-117">Examples</span></span>

<span data-ttu-id="4e8f1-118">Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im Mai ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e8f1-118">The following XML defines a months calendar that runs the task in May.</span></span>


```XML
<Months>
    <May/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="4e8f1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e8f1-119">Requirements</span></span>



| <span data-ttu-id="4e8f1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e8f1-120">Requirement</span></span> | <span data-ttu-id="4e8f1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4e8f1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4e8f1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e8f1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4e8f1-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e8f1-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4e8f1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e8f1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4e8f1-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e8f1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e8f1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e8f1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e8f1-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="4e8f1-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4e8f1-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="4e8f1-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





