---
title: Juli-Element (monthstype)
description: Gibt an, dass der Task im Juli ausgeführt wird.
ms.assetid: 6fcb06f1-0806-469c-a283-ba8f2ba2c256
keywords:
- Juli-Element Taskplaner
topic_type:
- apiref
api_name:
- July
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6901ca83792ffd98269e26dc9cf24dd575025c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742904"
---
# <a name="july-monthstype-element"></a><span data-ttu-id="65ce0-104">Juli-Element (monthstype)</span><span class="sxs-lookup"><span data-stu-id="65ce0-104">July (monthsType) Element</span></span>

<span data-ttu-id="65ce0-105">Gibt an, dass der Task im Juli ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65ce0-105">Specifies that the task runs in July.</span></span>

``` syntax
<xs:element name="July">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="65ce0-106">Das **Juli** -Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="65ce0-106">The **July** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="65ce0-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="65ce0-107">Parent element</span></span>



| <span data-ttu-id="65ce0-108">Element</span><span class="sxs-lookup"><span data-stu-id="65ce0-108">Element</span></span>                                                                                                          | <span data-ttu-id="65ce0-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="65ce0-109">Derived from</span></span>                                                     | <span data-ttu-id="65ce0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65ce0-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65ce0-111">**Monate (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="65ce0-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="65ce0-112">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="65ce0-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="65ce0-113">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65ce0-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="65ce0-114">**Monate (monthlyscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="65ce0-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="65ce0-115">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="65ce0-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="65ce0-116">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65ce0-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="65ce0-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65ce0-117">Examples</span></span>

<span data-ttu-id="65ce0-118">Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im Juli ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65ce0-118">The following XML defines a months calendar that runs the task in July.</span></span>


```XML
<Months>
    <July/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="65ce0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65ce0-119">Requirements</span></span>



| <span data-ttu-id="65ce0-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65ce0-120">Requirement</span></span> | <span data-ttu-id="65ce0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="65ce0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="65ce0-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65ce0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="65ce0-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65ce0-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="65ce0-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65ce0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="65ce0-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65ce0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65ce0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65ce0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ce0-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="65ce0-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="65ce0-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="65ce0-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





