---
title: Interval (repetitiontype)-Element
description: Gibt die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe an.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Interval-Element Taskplaner
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9720bc2257d4c0b45116089bfdd4113335fc6b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949643"
---
# <a name="interval-repetitiontype-element"></a><span data-ttu-id="ed361-104">Interval (repetitiontype)-Element</span><span class="sxs-lookup"><span data-stu-id="ed361-104">Interval (repetitionType) Element</span></span>

<span data-ttu-id="ed361-105">Gibt die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="ed361-105">Specifies the amount of time between each restart of the task.</span></span> <span data-ttu-id="ed361-106">Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S ("PT5M" ist beispielsweise 5 Minuten, "PT1H" ist 1 Stunde, und "PT20M" beträgt 20 Minuten).</span><span class="sxs-lookup"><span data-stu-id="ed361-106">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="ed361-107">Die maximal zulässige Dauer beträgt 31 Tage, und die zulässige Mindestanzahl beträgt 1 Minute.</span><span class="sxs-lookup"><span data-stu-id="ed361-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

``` syntax
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
```

<span data-ttu-id="ed361-108">Das-Element wird durch den komplexen Typ " [**wiederholtiontype**](taskschedulerschema-repetitiontype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="ed361-108">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ed361-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="ed361-109">Parent element</span></span>



| <span data-ttu-id="ed361-110">Element</span><span class="sxs-lookup"><span data-stu-id="ed361-110">Element</span></span>                                                                      | <span data-ttu-id="ed361-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="ed361-111">Derived from</span></span>                                                             | <span data-ttu-id="ed361-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed361-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed361-113">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="ed361-113">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="ed361-114">**Wiederholungstyp**</span><span class="sxs-lookup"><span data-stu-id="ed361-114">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="ed361-115">Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="ed361-115">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ed361-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed361-116">Remarks</span></span>

<span data-ttu-id="ed361-117">Bei der Skripterstellung wird das Intervall des Wiederholungs Musters mithilfe der [**repetitionpattern. Interval**](repetitionpattern-interval.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="ed361-117">For scripting development, the interval of the repetition pattern is specified using the [**RepetitionPattern.Interval**](repetitionpattern-interval.md) property.</span></span>

<span data-ttu-id="ed361-118">Bei der C++-Entwicklung wird das Intervall des Wiederholungs Musters mithilfe der [**irepetitionpattern:: Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="ed361-118">For C++ development, the interval of the repetition pattern is specified using the [**IRepetitionPattern::Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="ed361-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed361-119">Examples</span></span>

<span data-ttu-id="ed361-120">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die ein Wiederholungsintervall verwendet, finden Sie unter Beispiel für das [tägliche Beispiel (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="ed361-120">For a complete example of the XML for a task that uses a repetition interval, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed361-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed361-121">Requirements</span></span>



| <span data-ttu-id="ed361-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed361-122">Requirement</span></span> | <span data-ttu-id="ed361-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ed361-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ed361-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed361-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ed361-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed361-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ed361-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed361-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ed361-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed361-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed361-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed361-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed361-129">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="ed361-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ed361-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="ed361-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





