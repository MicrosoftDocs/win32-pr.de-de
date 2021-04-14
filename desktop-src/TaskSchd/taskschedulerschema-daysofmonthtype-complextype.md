---
title: komplexer daysofmonthtype-Typ
description: Definiert das untergeordnete Element und die Sequenzierungs Informationen für das daysOfMonth (monthlyscheduletype)-Element.
ms.assetid: 8258c090-c836-497e-8e5b-db4782277822
keywords:
- komplexer daysofmonthtype-Typ Taskplaner
topic_type:
- apiref
api_name:
- daysOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1459528b47bf01a9e336b758b739c3f5751ee1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392119"
---
# <a name="daysofmonthtype-complex-type"></a><span data-ttu-id="e2983-104">komplexer daysofmonthtype-Typ</span><span class="sxs-lookup"><span data-stu-id="e2983-104">daysOfMonthType Complex Type</span></span>

<span data-ttu-id="e2983-105">Definiert das untergeordnete Element und die Sequenzierungs Informationen für das [**daysOfMonth (monthlyscheduletype)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="e2983-105">Defines the child element and sequencing information for the [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element.</span></span>

``` syntax
<xs:complexType name="daysOfMonthType">
    <xs:sequence>
        <xs:element name="Day"
            type="dayOfMonthType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e2983-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2983-106">Child elements</span></span>



| <span data-ttu-id="e2983-107">Element</span><span class="sxs-lookup"><span data-stu-id="e2983-107">Element</span></span>                                                        | <span data-ttu-id="e2983-108">type</span><span class="sxs-lookup"><span data-stu-id="e2983-108">Type</span></span>                                                                    | <span data-ttu-id="e2983-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2983-109">Description</span></span>                                                          |
|----------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="e2983-110">**Tag**</span><span class="sxs-lookup"><span data-stu-id="e2983-110">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="e2983-111">**dayoatmonthtype**</span><span class="sxs-lookup"><span data-stu-id="e2983-111">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="e2983-112">Gibt den Tag des Monats an, in dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2983-112">Specifies a day of the month during which the task runs.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="e2983-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2983-113">Requirements</span></span>



| <span data-ttu-id="e2983-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2983-114">Requirement</span></span> | <span data-ttu-id="e2983-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e2983-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2983-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2983-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e2983-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2983-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e2983-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2983-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e2983-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2983-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2983-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2983-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2983-121">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="e2983-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="e2983-122">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="e2983-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





