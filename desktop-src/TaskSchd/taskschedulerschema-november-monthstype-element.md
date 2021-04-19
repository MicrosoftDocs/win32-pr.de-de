---
title: November-Element (monthstype)
description: Gibt an, dass der Task im November ausgeführt wird.
ms.assetid: 45f8c47b-3884-4f18-8275-f29f82ee32e2
keywords:
- November-Element Taskplaner
topic_type:
- apiref
api_name:
- November
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 295b63a4ff4dad1ec07504bb43c4a471d4389159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342454"
---
# <a name="november-monthstype-element"></a><span data-ttu-id="f1dbf-104">November-Element (monthstype)</span><span class="sxs-lookup"><span data-stu-id="f1dbf-104">November (monthsType) Element</span></span>

<span data-ttu-id="f1dbf-105">Gibt an, dass der Task im November ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-105">Specifies that the task runs in November.</span></span>

``` syntax
<xs:element name="November">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="f1dbf-106">Das **November** -Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-106">The **November** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f1dbf-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f1dbf-107">Parent element</span></span>



| <span data-ttu-id="f1dbf-108">Element</span><span class="sxs-lookup"><span data-stu-id="f1dbf-108">Element</span></span>                                                                                                          | <span data-ttu-id="f1dbf-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="f1dbf-109">Derived from</span></span>                                                     | <span data-ttu-id="f1dbf-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1dbf-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1dbf-111">**Monate (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="f1dbf-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="f1dbf-112">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="f1dbf-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="f1dbf-113">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="f1dbf-114">**Monate (monthlyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="f1dbf-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="f1dbf-115">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="f1dbf-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="f1dbf-116">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="f1dbf-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1dbf-117">Examples</span></span>

<span data-ttu-id="f1dbf-118">Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im November ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1dbf-118">The following XML defines a months calendar that runs the task in November.</span></span>


```XML
<Months>
    <November/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="f1dbf-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1dbf-119">Requirements</span></span>



| <span data-ttu-id="f1dbf-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1dbf-120">Requirement</span></span> | <span data-ttu-id="f1dbf-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f1dbf-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1dbf-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1dbf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f1dbf-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1dbf-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f1dbf-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1dbf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f1dbf-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1dbf-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1dbf-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1dbf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1dbf-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="f1dbf-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f1dbf-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="f1dbf-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





