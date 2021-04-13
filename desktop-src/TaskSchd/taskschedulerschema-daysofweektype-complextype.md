---
title: komplexer tagsofweektype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für die Elemente DaysOfWeek (weeklyscheduletype) und DaysOfWeek (monthlydayosweekscheduletype).
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- komplexer tagsofweektype-Typ Taskplaner
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341337"
---
# <a name="daysofweektype-complex-type"></a><span data-ttu-id="9e002-104">komplexer tagsofweektype-Typ</span><span class="sxs-lookup"><span data-stu-id="9e002-104">daysOfWeekType Complex Type</span></span>

<span data-ttu-id="9e002-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für die Elemente [**DaysOfWeek (weeklyscheduletype)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) und [**DaysOfWeek (monthlydayosweekscheduletype)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9e002-105">Defines the child elements and sequencing information for the [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) and [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9e002-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e002-106">Child elements</span></span>



| <span data-ttu-id="9e002-107">Element</span><span class="sxs-lookup"><span data-stu-id="9e002-107">Element</span></span>                                                                   | <span data-ttu-id="9e002-108">type</span><span class="sxs-lookup"><span data-stu-id="9e002-108">Type</span></span> | <span data-ttu-id="9e002-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e002-109">Description</span></span>                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [<span data-ttu-id="9e002-110">**Am**</span><span class="sxs-lookup"><span data-stu-id="9e002-110">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       | <span data-ttu-id="9e002-111">–</span><span class="sxs-lookup"><span data-stu-id="9e002-111">N/A</span></span>  | <span data-ttu-id="9e002-112">Der Task wird am Freitag ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e002-112">Task runs on Friday.</span></span> <br/>    |
| [<span data-ttu-id="9e002-113">**Pfingst**</span><span class="sxs-lookup"><span data-stu-id="9e002-113">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       | <span data-ttu-id="9e002-114">–</span><span class="sxs-lookup"><span data-stu-id="9e002-114">N/A</span></span>  | <span data-ttu-id="9e002-115">Der Task wird am Montag ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e002-115">Task runs on Monday.</span></span><br/>     |
| [<span data-ttu-id="9e002-116">**Samstag**</span><span class="sxs-lookup"><span data-stu-id="9e002-116">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   | <span data-ttu-id="9e002-117">–</span><span class="sxs-lookup"><span data-stu-id="9e002-117">N/A</span></span>  | <span data-ttu-id="9e002-118">Der Task wird am Samstag ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e002-118">Task runs on Saturday.</span></span> <br/>  |
| [<span data-ttu-id="9e002-119">**Sunday**</span><span class="sxs-lookup"><span data-stu-id="9e002-119">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       | <span data-ttu-id="9e002-120">–</span><span class="sxs-lookup"><span data-stu-id="9e002-120">N/A</span></span>  | <span data-ttu-id="9e002-121">Der Task wird am Sonntag ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e002-121">Task runs on Sunday.</span></span> <br/>    |
| [<span data-ttu-id="9e002-122">**Mitteilte**</span><span class="sxs-lookup"><span data-stu-id="9e002-122">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   | <span data-ttu-id="9e002-123">–</span><span class="sxs-lookup"><span data-stu-id="9e002-123">N/A</span></span>  | <span data-ttu-id="9e002-124">Task wird am Donnerstag ausgeführt</span><span class="sxs-lookup"><span data-stu-id="9e002-124">Task runs on Thursday</span></span> <br/>   |
| [<span data-ttu-id="9e002-125">**Mitteilte**</span><span class="sxs-lookup"><span data-stu-id="9e002-125">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     | <span data-ttu-id="9e002-126">–</span><span class="sxs-lookup"><span data-stu-id="9e002-126">N/A</span></span>  | <span data-ttu-id="9e002-127">Der Task wird am Dienstag ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e002-127">Task runs on Tuesday.</span></span> <br/>   |
| [<span data-ttu-id="9e002-128">**Mittwochs**</span><span class="sxs-lookup"><span data-stu-id="9e002-128">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) | <span data-ttu-id="9e002-129">–</span><span class="sxs-lookup"><span data-stu-id="9e002-129">N/A</span></span>  | <span data-ttu-id="9e002-130">Der Task wird am Mittwoch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e002-130">Task runs on Wednesday.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="9e002-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e002-131">Requirements</span></span>



| <span data-ttu-id="9e002-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e002-132">Requirement</span></span> | <span data-ttu-id="9e002-133">Wert</span><span class="sxs-lookup"><span data-stu-id="9e002-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9e002-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e002-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9e002-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e002-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9e002-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e002-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9e002-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e002-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e002-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e002-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e002-139">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="9e002-139">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="9e002-140">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="9e002-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





