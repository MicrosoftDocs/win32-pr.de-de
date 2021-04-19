---
title: komplexer monthlydayosweekscheduletype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das schedulebymonthdayoorweek-Element.
ms.assetid: fb4e5ba3-592b-47a4-bedf-5181d2b7a50f
keywords:
- komplexer monthlydayosweekscheduletype-Typ Taskplaner
topic_type:
- apiref
api_name:
- monthlyDayOfWeekScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 782715aed5cbf59a98e996bfa18fdd7c1022227a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345498"
---
# <a name="monthlydayofweekscheduletype-complex-type"></a><span data-ttu-id="86b38-104">komplexer monthlydayosweekscheduletype-Typ</span><span class="sxs-lookup"><span data-stu-id="86b38-104">monthlyDayOfWeekScheduleType Complex Type</span></span>

<span data-ttu-id="86b38-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**schedulebymonthdayoorweek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="86b38-105">Defines the child elements and sequencing information for the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyDayOfWeekScheduleType">
    <xs:all>
        <xs:element name="Weeks"
            type="weeksType"
            minOccurs="0"
         />
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="86b38-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86b38-106">Child elements</span></span>



| <span data-ttu-id="86b38-107">Element</span><span class="sxs-lookup"><span data-stu-id="86b38-107">Element</span></span>                                                                                   | <span data-ttu-id="86b38-108">type</span><span class="sxs-lookup"><span data-stu-id="86b38-108">Type</span></span>                                                                     | <span data-ttu-id="86b38-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86b38-109">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="86b38-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="86b38-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="86b38-111">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="86b38-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="86b38-112">Gibt die Wochentage an, an denen die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86b38-112">Specifies the days of the week during which the task runs.</span></span><br/>   |
| [<span data-ttu-id="86b38-113">**Monate**</span><span class="sxs-lookup"><span data-stu-id="86b38-113">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="86b38-114">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="86b38-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="86b38-115">Gibt die Monate des Jahres an, in dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86b38-115">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="86b38-116">**Wochen**</span><span class="sxs-lookup"><span data-stu-id="86b38-116">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | [<span data-ttu-id="86b38-117">**weekstype**</span><span class="sxs-lookup"><span data-stu-id="86b38-117">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md)           | <span data-ttu-id="86b38-118">Gibt die Wochen des Monats an, in denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86b38-118">Specifies the weeks of the month during which the task runs.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="86b38-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86b38-119">Requirements</span></span>



| <span data-ttu-id="86b38-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86b38-120">Requirement</span></span> | <span data-ttu-id="86b38-121">Wert</span><span class="sxs-lookup"><span data-stu-id="86b38-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="86b38-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86b38-122">Minimum supported client</span></span><br/> | <span data-ttu-id="86b38-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86b38-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="86b38-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86b38-124">Minimum supported server</span></span><br/> | <span data-ttu-id="86b38-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86b38-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="86b38-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86b38-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b38-127">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="86b38-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="86b38-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="86b38-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





