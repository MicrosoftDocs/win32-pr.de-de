---
title: komplexer dailyscheduletype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das schedulebyday-Element.
ms.assetid: e0b1b09f-d72a-4a85-9059-4a917bc0104a
keywords:
- komplexer dailyscheduletype-Typ Taskplaner
topic_type:
- apiref
api_name:
- dailyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5982ab7e72a79dc909a4e91fafe363ca4703639d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346743"
---
# <a name="dailyscheduletype-complex-type"></a><span data-ttu-id="2f359-104">komplexer dailyscheduletype-Typ</span><span class="sxs-lookup"><span data-stu-id="2f359-104">dailyScheduleType Complex Type</span></span>

<span data-ttu-id="2f359-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**schedulebyday**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="2f359-105">Defines the child elements and sequencing information for the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="dailyScheduleType">
    <xs:all>
        <xs:element name="DaysInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedInt"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="365"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="2f359-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f359-106">Child elements</span></span>



| <span data-ttu-id="2f359-107">Element</span><span class="sxs-lookup"><span data-stu-id="2f359-107">Element</span></span>                                                                            | <span data-ttu-id="2f359-108">type</span><span class="sxs-lookup"><span data-stu-id="2f359-108">Type</span></span> | <span data-ttu-id="2f359-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f359-109">Description</span></span>                                                          |
|------------------------------------------------------------------------------------|------|----------------------------------------------------------------------|
| [<span data-ttu-id="2f359-110">**Daysinterval**</span><span class="sxs-lookup"><span data-stu-id="2f359-110">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |      | <span data-ttu-id="2f359-111">Gibt das Intervall zwischen den Tagen im Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="2f359-111">Specifies the interval between the days in the schedule.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="2f359-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f359-112">Requirements</span></span>



| <span data-ttu-id="2f359-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f359-113">Requirement</span></span> | <span data-ttu-id="2f359-114">Wert</span><span class="sxs-lookup"><span data-stu-id="2f359-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2f359-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f359-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2f359-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f359-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2f359-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f359-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2f359-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f359-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f359-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f359-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f359-120">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="2f359-120">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="2f359-121">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="2f359-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





