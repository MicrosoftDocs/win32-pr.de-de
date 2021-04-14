---
title: komplexer Wiederholungstyp
description: Definiert die untergeordneten Elemente und Sequenz Informationen für das Wiederholungs Element (triggerbasetype).
ms.assetid: d2b4b840-3a69-4ff8-ac32-6ec76e7e8788
keywords:
- komplexer Wiederholungstyp Taskplaner
topic_type:
- apiref
api_name:
- repetitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aa9ee8c08a79f5db053b772c86929f98a72f011c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392081"
---
# <a name="repetitiontype-complex-type"></a><span data-ttu-id="38f13-104">komplexer Wiederholungstyp</span><span class="sxs-lookup"><span data-stu-id="38f13-104">repetitionType Complex Type</span></span>

<span data-ttu-id="38f13-105">Definiert die untergeordneten Elemente und Sequenz Informationen für das [**Wiederholungs Element (triggerbasetype)**](taskschedulerschema-repetition-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="38f13-105">Defines the child elements and sequence information for the [**Repetition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

``` syntax
<xs:complexType name="repetitionType">
    <xs:all>
        <xs:element name="Interval">
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                    <xs:maxInclusive
                        value="P31D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Duration"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="StopAtDurationEnd"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="38f13-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38f13-106">Child elements</span></span>



| <span data-ttu-id="38f13-107">Element</span><span class="sxs-lookup"><span data-stu-id="38f13-107">Element</span></span>                                                                                   | <span data-ttu-id="38f13-108">type</span><span class="sxs-lookup"><span data-stu-id="38f13-108">Type</span></span>    | <span data-ttu-id="38f13-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38f13-109">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38f13-110">**Duration**</span><span class="sxs-lookup"><span data-stu-id="38f13-110">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   |         | <span data-ttu-id="38f13-111">Gibt an, wie lange das Muster wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="38f13-111">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="38f13-112">Wenn kein Wert angegeben wird, wird das Muster unbegrenzt wiederholt.</span><span class="sxs-lookup"><span data-stu-id="38f13-112">If no value is specified, the pattern is repeated indefinitely.</span></span><br/> |
| [<span data-ttu-id="38f13-113">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="38f13-113">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   |         | <span data-ttu-id="38f13-114">Gibt die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="38f13-114">Specifies the amount of time between each restart of the task.</span></span><br/>                                              |
| [<span data-ttu-id="38f13-115">**Stopatdurationend**</span><span class="sxs-lookup"><span data-stu-id="38f13-115">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="38f13-116">boolean</span><span class="sxs-lookup"><span data-stu-id="38f13-116">boolean</span></span> | <span data-ttu-id="38f13-117">Gibt an, dass eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird.</span><span class="sxs-lookup"><span data-stu-id="38f13-117">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="38f13-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38f13-118">Requirements</span></span>



| <span data-ttu-id="38f13-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38f13-119">Requirement</span></span> | <span data-ttu-id="38f13-120">Wert</span><span class="sxs-lookup"><span data-stu-id="38f13-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="38f13-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38f13-121">Minimum supported client</span></span><br/> | <span data-ttu-id="38f13-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38f13-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="38f13-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38f13-123">Minimum supported server</span></span><br/> | <span data-ttu-id="38f13-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38f13-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38f13-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38f13-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f13-126">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="38f13-126">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="38f13-127">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="38f13-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





