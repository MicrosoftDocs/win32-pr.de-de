---
title: komplexer monthstype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für die Monate (monthlydayosweekscheduletype) und die Monate (monthlyscheduletype).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- komplexer monthstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6a19000073fd12e05aa915921850264979a0541
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740440"
---
# <a name="monthstype-complex-type"></a><span data-ttu-id="0fdad-104">komplexer monthstype-Typ</span><span class="sxs-lookup"><span data-stu-id="0fdad-104">monthsType Complex Type</span></span>

<span data-ttu-id="0fdad-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für die [**Monate (monthlydayosweekscheduletype)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) und die [**Monate (monthlyscheduletype)**](taskschedulerschema-months-monthlyscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0fdad-105">Defines the child elements and sequencing information for the [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) and [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0fdad-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0fdad-106">Child elements</span></span>



| <span data-ttu-id="0fdad-107">Element</span><span class="sxs-lookup"><span data-stu-id="0fdad-107">Element</span></span>                                                               | <span data-ttu-id="0fdad-108">type</span><span class="sxs-lookup"><span data-stu-id="0fdad-108">Type</span></span> | <span data-ttu-id="0fdad-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fdad-109">Description</span></span>                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [<span data-ttu-id="0fdad-110">**Am**</span><span class="sxs-lookup"><span data-stu-id="0fdad-110">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         | <span data-ttu-id="0fdad-111">–</span><span class="sxs-lookup"><span data-stu-id="0fdad-111">N/A</span></span>  | <span data-ttu-id="0fdad-112">Gibt an, dass der Task im April ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fdad-112">Specifies that the task runs in April.</span></span> <br/>     |
| [<span data-ttu-id="0fdad-113">**August**</span><span class="sxs-lookup"><span data-stu-id="0fdad-113">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       | <span data-ttu-id="0fdad-114">–</span><span class="sxs-lookup"><span data-stu-id="0fdad-114">N/A</span></span>  | <span data-ttu-id="0fdad-115">Gibt an, dass der Task im August ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fdad-115">Specifies that the task runs in August.</span></span> <br/>    |
| [<span data-ttu-id="0fdad-116">**Dezember**</span><span class="sxs-lookup"><span data-stu-id="0fdad-116">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   | <span data-ttu-id="0fdad-117">–</span><span class="sxs-lookup"><span data-stu-id="0fdad-117">N/A</span></span>  | <span data-ttu-id="0fdad-118">Gibt an, dass der Task im Dezember ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fdad-118">Specifies that the task runs in December.</span></span> <br/>  |
| [<span data-ttu-id="0fdad-119">**Februar**</span><span class="sxs-lookup"><span data-stu-id="0fdad-119">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   | <span data-ttu-id="0fdad-120">–</span><span class="sxs-lookup"><span data-stu-id="0fdad-120">N/A</span></span>  | <span data-ttu-id="0fdad-121">Gibt an, dass der Task im Februar ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fdad-121">Specifies that the task runs in February.</span></span> <br/>  |
| [<span data-ttu-id="0fdad-122">**January**</span><span class="sxs-lookup"><span data-stu-id="0fdad-122">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     | <span data-ttu-id="0fdad-123">–</span><span class="sxs-lookup"><span data-stu-id="0fdad-123">N/A</span></span>  | <span data-ttu-id="0fdad-124">Gibt an, dass der Task im Januar ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fdad-124">Specifies that the task runs in January.</span></span> <br/>   |
| [<span data-ttu-id="0fdad-125">**Juli**</span><span class="sxs-lookup"><span data-stu-id="0fdad-125">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           | <span data-ttu-id="0fdad-126">–</span><span class="sxs-lookup"><span data-stu-id="0fdad-126">N/A</span></span>  | <span data-ttu-id="0fdad-127">Gibt an, dass der Task im Juli ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fdad-127">Specifies that the task runs in July.</span></span> <br/>      |
| [<span data-ttu-id="0fdad-128">**June**</span><span class="sxs-lookup"><span data-stu-id="0fdad-128">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           | <span data-ttu-id="0fdad-129">–</span><span class="sxs-lookup"><span data-stu-id="0fdad-129">N/A</span></span>  | <span data-ttu-id="0fdad-130">Gibt an, dass der Task im Juni ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fdad-130">Specifies that the task runs in June.</span></span> <br/>      |
| [<span data-ttu-id="0fdad-131">**März**</span><span class="sxs-lookup"><span data-stu-id="0fdad-131">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         | <span data-ttu-id="0fdad-132">–</span><span class="sxs-lookup"><span data-stu-id="0fdad-132">N/A</span></span>  | <span data-ttu-id="0fdad-133">Gibt an, dass der Task im März ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fdad-133">Specifies that the task runs in March.</span></span> <br/>     |
| [<span data-ttu-id="0fdad-134">**May**</span><span class="sxs-lookup"><span data-stu-id="0fdad-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             | <span data-ttu-id="0fdad-135">–</span><span class="sxs-lookup"><span data-stu-id="0fdad-135">N/A</span></span>  | <span data-ttu-id="0fdad-136">Gibt an, dass der Task im Mai ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fdad-136">Specifies that the task runs in May.</span></span> <br/>       |
| [<span data-ttu-id="0fdad-137">**November**</span><span class="sxs-lookup"><span data-stu-id="0fdad-137">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   | <span data-ttu-id="0fdad-138">–</span><span class="sxs-lookup"><span data-stu-id="0fdad-138">N/A</span></span>  | <span data-ttu-id="0fdad-139">Gibt an, dass der Task im November ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fdad-139">Specifies that the task runs in November.</span></span> <br/>  |
| [<span data-ttu-id="0fdad-140">**Vom**</span><span class="sxs-lookup"><span data-stu-id="0fdad-140">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     | <span data-ttu-id="0fdad-141">–</span><span class="sxs-lookup"><span data-stu-id="0fdad-141">N/A</span></span>  | <span data-ttu-id="0fdad-142">Gibt an, dass der Task im Oktober ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fdad-142">Specifies that the task runs in October.</span></span> <br/>   |
| [<span data-ttu-id="0fdad-143">**September**</span><span class="sxs-lookup"><span data-stu-id="0fdad-143">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) | <span data-ttu-id="0fdad-144">–</span><span class="sxs-lookup"><span data-stu-id="0fdad-144">N/A</span></span>  | <span data-ttu-id="0fdad-145">Gibt an, dass der Task im September ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fdad-145">Specifies that the task runs in September.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="0fdad-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fdad-146">Requirements</span></span>



| <span data-ttu-id="0fdad-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fdad-147">Requirement</span></span> | <span data-ttu-id="0fdad-148">Wert</span><span class="sxs-lookup"><span data-stu-id="0fdad-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0fdad-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fdad-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0fdad-150">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fdad-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0fdad-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fdad-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0fdad-152">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fdad-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0fdad-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fdad-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fdad-154">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="0fdad-154">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="0fdad-155">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="0fdad-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





