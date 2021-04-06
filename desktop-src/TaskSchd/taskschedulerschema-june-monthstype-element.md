---
title: June-Element (monthstype)
description: Gibt an, dass der Task im Juni ausgeführt wird.
ms.assetid: 15b0e8c2-4dc1-4ca3-99c5-bd9a36718904
keywords:
- Juni-Element Taskplaner
topic_type:
- apiref
api_name:
- June
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e6c21834348a70033af69a71534c60c1b08d91a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742424"
---
# <a name="june-monthstype-element"></a><span data-ttu-id="ba6ff-104">June-Element (monthstype)</span><span class="sxs-lookup"><span data-stu-id="ba6ff-104">June (monthsType) Element</span></span>

<span data-ttu-id="ba6ff-105">Gibt an, dass der Task im Juni ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba6ff-105">Specifies that the task runs in June.</span></span>

``` syntax
<xs:element name="June">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="ba6ff-106">Das **Juni** -Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="ba6ff-106">The **June** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ba6ff-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ba6ff-107">Parent element</span></span>



| <span data-ttu-id="ba6ff-108">Element</span><span class="sxs-lookup"><span data-stu-id="ba6ff-108">Element</span></span>                                                                                                          | <span data-ttu-id="ba6ff-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="ba6ff-109">Derived from</span></span>                                                     | <span data-ttu-id="ba6ff-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba6ff-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba6ff-111">**Monate (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="ba6ff-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="ba6ff-112">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="ba6ff-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="ba6ff-113">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba6ff-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="ba6ff-114">**Monate (monthlyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="ba6ff-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="ba6ff-115">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="ba6ff-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="ba6ff-116">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba6ff-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="ba6ff-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba6ff-117">Examples</span></span>

<span data-ttu-id="ba6ff-118">Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im Juni ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba6ff-118">The following XML defines a months calendar that runs the task in June.</span></span>


```XML
<Months>
    <June/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="ba6ff-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba6ff-119">Requirements</span></span>



| <span data-ttu-id="ba6ff-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba6ff-120">Requirement</span></span> | <span data-ttu-id="ba6ff-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ba6ff-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ba6ff-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba6ff-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ba6ff-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba6ff-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ba6ff-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba6ff-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ba6ff-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba6ff-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba6ff-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba6ff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba6ff-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="ba6ff-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ba6ff-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="ba6ff-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





