---
title: Februar-Element (monthstype)
description: Gibt an, dass der Task im Februar ausgeführt wird.
ms.assetid: 871449f8-fa3a-4e1f-be36-bc5c98125721
keywords:
- Februar-Element Taskplaner
topic_type:
- apiref
api_name:
- February
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 727751964bfb9a752eb1190f8c7d3a86de2a9413
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344099"
---
# <a name="february-monthstype-element"></a><span data-ttu-id="06e68-104">Februar-Element (monthstype)</span><span class="sxs-lookup"><span data-stu-id="06e68-104">February (monthsType) Element</span></span>

<span data-ttu-id="06e68-105">Gibt an, dass der Task im Februar ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06e68-105">Specifies that the task runs in February.</span></span>

``` syntax
<xs:element name="February">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="06e68-106">Das **Februar** -Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="06e68-106">The **February** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="06e68-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="06e68-107">Parent element</span></span>



| <span data-ttu-id="06e68-108">Element</span><span class="sxs-lookup"><span data-stu-id="06e68-108">Element</span></span>                                                                                                          | <span data-ttu-id="06e68-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="06e68-109">Derived from</span></span>                                                     | <span data-ttu-id="06e68-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06e68-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06e68-111">**Monate (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="06e68-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="06e68-112">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="06e68-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="06e68-113">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06e68-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="06e68-114">**Monate (monthlyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="06e68-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="06e68-115">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="06e68-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="06e68-116">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06e68-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="06e68-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06e68-117">Examples</span></span>

<span data-ttu-id="06e68-118">Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im Februar ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06e68-118">The following XML defines a months calendar that runs the task in February.</span></span>


```XML
<Months>
    <February/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="06e68-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06e68-119">Requirements</span></span>



| <span data-ttu-id="06e68-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06e68-120">Requirement</span></span> | <span data-ttu-id="06e68-121">Wert</span><span class="sxs-lookup"><span data-stu-id="06e68-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="06e68-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06e68-122">Minimum supported client</span></span><br/> | <span data-ttu-id="06e68-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06e68-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="06e68-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06e68-124">Minimum supported server</span></span><br/> | <span data-ttu-id="06e68-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06e68-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06e68-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06e68-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06e68-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="06e68-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="06e68-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="06e68-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





