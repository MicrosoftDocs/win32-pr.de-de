---
title: Week (weekstype)-Element
description: Gibt eine bestimmte Woche des Monats an.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Week-Element Taskplaner
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0487aa07e1f1132c998b6cb2ba0f518a9db57ce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342659"
---
# <a name="week-weekstype-element"></a><span data-ttu-id="9458f-104">Week (weekstype)-Element</span><span class="sxs-lookup"><span data-stu-id="9458f-104">Week (weeksType) Element</span></span>

<span data-ttu-id="9458f-105">Gibt eine bestimmte Woche des Monats an.</span><span class="sxs-lookup"><span data-stu-id="9458f-105">Specifies a specific week of the month.</span></span>

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

<span data-ttu-id="9458f-106">Das **Week** -Element wird durch den komplexen [**weekstype**](taskschedulerschema-weekstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="9458f-106">The **Week** element is defined by the [**weeksType**](taskschedulerschema-weekstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9458f-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="9458f-107">Parent element</span></span>



| <span data-ttu-id="9458f-108">Element</span><span class="sxs-lookup"><span data-stu-id="9458f-108">Element</span></span>                                                                                                        | <span data-ttu-id="9458f-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="9458f-109">Derived from</span></span>                                                   | <span data-ttu-id="9458f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9458f-110">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="9458f-111">**Wochen (monthlydayosweekscheduletype)**</span><span class="sxs-lookup"><span data-stu-id="9458f-111">**Weeks (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="9458f-112">**weekstype**</span><span class="sxs-lookup"><span data-stu-id="9458f-112">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md) | <span data-ttu-id="9458f-113">Gibt die Wochen des Monats an, in denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9458f-113">Specifies the weeks of the month in which the task is run.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9458f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9458f-114">Remarks</span></span>

<span data-ttu-id="9458f-115">Wenn Sie die Wochen des Monats angeben, verwenden Sie die Zahlen 1-4 für die ersten vier Wochen des Monats, oder verwenden Sie die Zeichenfolge "Last", um die letzte Woche des Monats anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9458f-115">When specifying the weeks of the month, use the numbers 1-4 for the first four weeks of the month or use the string "Last" to indicate that last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="9458f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9458f-116">Requirements</span></span>



| <span data-ttu-id="9458f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9458f-117">Requirement</span></span> | <span data-ttu-id="9458f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9458f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9458f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9458f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9458f-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9458f-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9458f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9458f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9458f-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9458f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9458f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9458f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9458f-124">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="9458f-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9458f-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="9458f-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





