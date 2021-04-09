---
title: Oktober-Element (monthstype)
description: Gibt an, dass der Task im Oktober ausgeführt wird.
ms.assetid: 62c8bb3e-a70f-45b8-8d80-7a7eef9dfaeb
keywords:
- Oktober-Element Taskplaner
topic_type:
- apiref
api_name:
- October
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79bf2a2dde46341f48808342ab6aefb78863524b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106359"
---
# <a name="october-monthstype-element"></a><span data-ttu-id="d8487-104">Oktober-Element (monthstype)</span><span class="sxs-lookup"><span data-stu-id="d8487-104">October (monthsType) Element</span></span>

<span data-ttu-id="d8487-105">Gibt an, dass der Task im Oktober ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8487-105">Specifies that the task runs in October.</span></span>

``` syntax
<xs:element name="October">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="d8487-106">Das **Oktober** -Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="d8487-106">The **October** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d8487-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="d8487-107">Parent element</span></span>



| <span data-ttu-id="d8487-108">Element</span><span class="sxs-lookup"><span data-stu-id="d8487-108">Element</span></span>                                                                                                          | <span data-ttu-id="d8487-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="d8487-109">Derived from</span></span>                                                     | <span data-ttu-id="d8487-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8487-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8487-111">**Monate (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="d8487-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="d8487-112">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="d8487-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="d8487-113">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8487-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="d8487-114">**Monate (monthlyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="d8487-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="d8487-115">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="d8487-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="d8487-116">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8487-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="d8487-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8487-117">Examples</span></span>

<span data-ttu-id="d8487-118">Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im Oktober ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8487-118">The following XML defines a months calendar that runs the task in October.</span></span>


```XML
<Months>
    <October/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="d8487-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8487-119">Requirements</span></span>



| <span data-ttu-id="d8487-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8487-120">Requirement</span></span> | <span data-ttu-id="d8487-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d8487-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d8487-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8487-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d8487-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8487-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d8487-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8487-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d8487-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8487-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8487-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8487-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8487-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="d8487-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d8487-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d8487-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





