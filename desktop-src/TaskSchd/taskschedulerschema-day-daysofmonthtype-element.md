---
title: Day (daysofmonthtype)-Element
description: Gibt den Tag des Monats an, in dem die Aufgabe ausgeführt wird.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Day-Element Taskplaner
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e8e06169d2b758264f181263a5cb717977a1602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040336"
---
# <a name="day-daysofmonthtype-element"></a><span data-ttu-id="b362f-104">Day (daysofmonthtype)-Element</span><span class="sxs-lookup"><span data-stu-id="b362f-104">Day (daysOfMonthType) Element</span></span>

<span data-ttu-id="b362f-105">Gibt den Tag des Monats an, in dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b362f-105">Specifies a day of the month during which the task runs.</span></span>

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

<span data-ttu-id="b362f-106">Das **Day** -Element wird durch den komplexen [**tagsofmonthtype**](taskschedulerschema-daysofmonthtype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="b362f-106">The **Day** element is defined by the [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b362f-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="b362f-107">Parent element</span></span>



| <span data-ttu-id="b362f-108">Element</span><span class="sxs-lookup"><span data-stu-id="b362f-108">Element</span></span>                                                                            | <span data-ttu-id="b362f-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="b362f-109">Derived from</span></span>                                                               | <span data-ttu-id="b362f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b362f-110">Description</span></span>                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="b362f-111">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="b362f-111">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="b362f-112">**daysofmonthtype**</span><span class="sxs-lookup"><span data-stu-id="b362f-112">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="b362f-113">Gibt die Tage des Monats an, in denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b362f-113">Specifies the days of the month during which the task runs.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="b362f-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b362f-114">Examples</span></span>

<span data-ttu-id="b362f-115">Im folgenden XML-Code wird der Tage Teil eines monatlichen Kalenders definiert, der die Aufgabe am 1. und 15. Tag des Monats ausführt.</span><span class="sxs-lookup"><span data-stu-id="b362f-115">The following XML defines the days portion of a monthly calendar that runs the task on the 1st and 15th day of the month.</span></span>


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a><span data-ttu-id="b362f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b362f-116">Requirements</span></span>



| <span data-ttu-id="b362f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b362f-117">Requirement</span></span> | <span data-ttu-id="b362f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b362f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b362f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b362f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b362f-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b362f-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b362f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b362f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b362f-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b362f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b362f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b362f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b362f-124">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="b362f-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





