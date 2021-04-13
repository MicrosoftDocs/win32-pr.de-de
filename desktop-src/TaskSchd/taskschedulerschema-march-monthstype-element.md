---
title: March (monthstype)-Element
description: Gibt an, dass der Task im März ausgeführt wird.
ms.assetid: 0cd82405-8e17-483d-88ba-32cae590f6b3
keywords:
- März-Element Taskplaner
topic_type:
- apiref
api_name:
- March
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bf6792cf65ab3aecb74bff82282daa0d8fb2bdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340938"
---
# <a name="march-monthstype-element"></a><span data-ttu-id="38c56-104">March (monthstype)-Element</span><span class="sxs-lookup"><span data-stu-id="38c56-104">March (monthsType) Element</span></span>

<span data-ttu-id="38c56-105">Gibt an, dass der Task im März ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38c56-105">Specifies that the task runs in March.</span></span>

``` syntax
<xs:element name="March">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="38c56-106">Das **March** -Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="38c56-106">The **March** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="38c56-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="38c56-107">Parent element</span></span>



| <span data-ttu-id="38c56-108">Element</span><span class="sxs-lookup"><span data-stu-id="38c56-108">Element</span></span>                                                                                                          | <span data-ttu-id="38c56-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="38c56-109">Derived from</span></span>                                                     | <span data-ttu-id="38c56-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38c56-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38c56-111">**Monate (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="38c56-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="38c56-112">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="38c56-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="38c56-113">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38c56-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="38c56-114">**Monate (monthlyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="38c56-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="38c56-115">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="38c56-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="38c56-116">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38c56-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="38c56-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38c56-117">Examples</span></span>

<span data-ttu-id="38c56-118">Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im März ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38c56-118">The following XML defines a months calendar that runs the task in March.</span></span>


```XML
<Months>
    <March/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="38c56-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38c56-119">Requirements</span></span>



| <span data-ttu-id="38c56-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38c56-120">Requirement</span></span> | <span data-ttu-id="38c56-121">Wert</span><span class="sxs-lookup"><span data-stu-id="38c56-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="38c56-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38c56-122">Minimum supported client</span></span><br/> | <span data-ttu-id="38c56-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38c56-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="38c56-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38c56-124">Minimum supported server</span></span><br/> | <span data-ttu-id="38c56-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38c56-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38c56-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38c56-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38c56-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="38c56-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="38c56-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="38c56-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





