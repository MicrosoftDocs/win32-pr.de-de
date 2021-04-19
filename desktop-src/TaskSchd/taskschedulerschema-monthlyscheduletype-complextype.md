---
title: komplexer monthlyscheduletype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das schedulebymonth (calendartriggertype)-Element.
ms.assetid: 3ade775c-ca44-403e-9602-80095c7dba1a
keywords:
- komplexer monthlyscheduletype-Typ Taskplaner
topic_type:
- apiref
api_name:
- monthlyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c2fafe2b05a01380c13aae2ab7cb3ddaa5330
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339554"
---
# <a name="monthlyscheduletype-complex-type"></a><span data-ttu-id="c01d8-104">komplexer monthlyscheduletype-Typ</span><span class="sxs-lookup"><span data-stu-id="c01d8-104">monthlyScheduleType Complex Type</span></span>

<span data-ttu-id="c01d8-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**schedulebymonth (calendartriggertype)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="c01d8-105">Defines the child elements and sequencing information for the [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyScheduleType">
    <xs:all>
        <xs:element name="DaysOfMonth"
            type="daysOfMonthType"
            minOccurs="0"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c01d8-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c01d8-106">Child elements</span></span>



| <span data-ttu-id="c01d8-107">Element</span><span class="sxs-lookup"><span data-stu-id="c01d8-107">Element</span></span>                                                                            | <span data-ttu-id="c01d8-108">type</span><span class="sxs-lookup"><span data-stu-id="c01d8-108">Type</span></span>                                                                       | <span data-ttu-id="c01d8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c01d8-109">Description</span></span>                                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c01d8-110">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="c01d8-110">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="c01d8-111">**daysofmonthtype**</span><span class="sxs-lookup"><span data-stu-id="c01d8-111">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="c01d8-112">Gibt die Tage des Monats an, in denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c01d8-112">Specifies the days of the month during which the task runs.</span></span><br/>                         |
| [<span data-ttu-id="c01d8-113">**Monate**</span><span class="sxs-lookup"><span data-stu-id="c01d8-113">**Months**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="c01d8-114">**monthstype**</span><span class="sxs-lookup"><span data-stu-id="c01d8-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="c01d8-115">Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c01d8-115">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c01d8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c01d8-116">Requirements</span></span>



| <span data-ttu-id="c01d8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c01d8-117">Requirement</span></span> | <span data-ttu-id="c01d8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c01d8-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c01d8-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c01d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c01d8-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c01d8-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c01d8-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c01d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c01d8-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c01d8-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c01d8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c01d8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c01d8-124">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="c01d8-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="c01d8-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="c01d8-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





