---
title: komplexer weeklyscheduletype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das schedulebyweek-Element.
ms.assetid: 048832fa-2262-4461-9cfc-823a4eb7a1df
keywords:
- der komplexe Typ "weeklyscheduletype" Taskplaner
topic_type:
- apiref
api_name:
- weeklyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 797e01c20e749593d64bad12f017af8be613992e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391757"
---
# <a name="weeklyscheduletype-complex-type"></a><span data-ttu-id="621f8-104">komplexer weeklyscheduletype-Typ</span><span class="sxs-lookup"><span data-stu-id="621f8-104">weeklyScheduleType Complex Type</span></span>

<span data-ttu-id="621f8-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**schedulebyweek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="621f8-105">Defines the child elements and sequencing information for the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeklyScheduleType">
    <xs:all>
        <xs:element name="WeeksInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="52"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="621f8-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="621f8-106">Child elements</span></span>



| <span data-ttu-id="621f8-107">Element</span><span class="sxs-lookup"><span data-stu-id="621f8-107">Element</span></span>                                                                               | <span data-ttu-id="621f8-108">type</span><span class="sxs-lookup"><span data-stu-id="621f8-108">Type</span></span>                                                                     | <span data-ttu-id="621f8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="621f8-109">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="621f8-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="621f8-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="621f8-111">**daysofweektype**</span><span class="sxs-lookup"><span data-stu-id="621f8-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="621f8-112">Gibt die Wochentage an, an denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="621f8-112">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="621f8-113">**Weeksinterval**</span><span class="sxs-lookup"><span data-stu-id="621f8-113">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) |                                                                          | <span data-ttu-id="621f8-114">Gibt das Intervall zwischen den Wochen im Zeitplan an.</span><span class="sxs-lookup"><span data-stu-id="621f8-114">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="621f8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="621f8-115">Requirements</span></span>



| <span data-ttu-id="621f8-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="621f8-116">Requirement</span></span> | <span data-ttu-id="621f8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="621f8-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="621f8-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="621f8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="621f8-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="621f8-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="621f8-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="621f8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="621f8-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="621f8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="621f8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="621f8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="621f8-123">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="621f8-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





