---
title: Interval (repetitionType)-Element
description: Gibt die Zeitspanne zwischen jedem Neustart der Aufgabe an.
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
ms.openlocfilehash: bfb87884438f1a39a5bd6f08eb9bb855311eb5d3
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734195"
---
# <a name="interval-repetitiontype-element"></a><span data-ttu-id="846ad-104">Interval (repetitionType)-Element</span><span class="sxs-lookup"><span data-stu-id="846ad-104">Interval (repetitionType) Element</span></span>

<span data-ttu-id="846ad-105">Gibt die Zeitspanne zwischen jedem Neustart der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="846ad-105">Specifies the amount of time between each restart of the task.</span></span> <span data-ttu-id="846ad-106">Das Format für diese Zeichenfolge lautet `P<days>DT<hours>H<minutes>M<seconds>S` (z. B. "PT5M" ist 5 Minuten, "PT1H" ist 1 Stunde und "PT20M" ist 20 Minuten).</span><span class="sxs-lookup"><span data-stu-id="846ad-106">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="846ad-107">Die maximal zulässige Zeit beträgt 31 Tage, und die zulässige Mindestzeit beträgt 1 Minute.</span><span class="sxs-lookup"><span data-stu-id="846ad-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

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

<span data-ttu-id="846ad-108">Das Element wird durch den komplexen [**Wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="846ad-108">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="846ad-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="846ad-109">Parent element</span></span>



| <span data-ttu-id="846ad-110">Element</span><span class="sxs-lookup"><span data-stu-id="846ad-110">Element</span></span>                                                                      | <span data-ttu-id="846ad-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="846ad-111">Derived from</span></span>                                                             | <span data-ttu-id="846ad-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="846ad-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="846ad-113">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="846ad-113">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="846ad-114">**wiederholungstyp**</span><span class="sxs-lookup"><span data-stu-id="846ad-114">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="846ad-115">Gibt an, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="846ad-115">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="846ad-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="846ad-116">Remarks</span></span>

<span data-ttu-id="846ad-117">Für die Skriptentwicklung wird das Intervall des Wiederholungsmusters mithilfe der [**RepetitionPattern.Interval-Eigenschaft**](repetitionpattern-interval.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="846ad-117">For scripting development, the interval of the repetition pattern is specified using the [**RepetitionPattern.Interval**](repetitionpattern-interval.md) property.</span></span>

<span data-ttu-id="846ad-118">Für die C++-Entwicklung wird das Intervall des Wiederholungsmusters mithilfe der [**IRepetitionPattern::Interval-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) angegeben.</span><span class="sxs-lookup"><span data-stu-id="846ad-118">For C++ development, the interval of the repetition pattern is specified using the [**IRepetitionPattern::Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="846ad-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="846ad-119">Examples</span></span>

<span data-ttu-id="846ad-120">Ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die ein Wiederholungsintervall verwendet, finden Sie unter Beispiel für [täglichen Trigger (XML).](daily-trigger-example--xml-.md)</span><span class="sxs-lookup"><span data-stu-id="846ad-120">For a complete example of the XML for a task that uses a repetition interval, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="846ad-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="846ad-121">Requirements</span></span>



| <span data-ttu-id="846ad-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="846ad-122">Requirement</span></span> | <span data-ttu-id="846ad-123">Wert</span><span class="sxs-lookup"><span data-stu-id="846ad-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="846ad-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="846ad-124">Minimum supported client</span></span><br/> | <span data-ttu-id="846ad-125">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="846ad-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="846ad-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="846ad-126">Minimum supported server</span></span><br/> | <span data-ttu-id="846ad-127">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="846ad-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="846ad-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="846ad-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="846ad-129">Taskplaner Schemaelemente</span><span class="sxs-lookup"><span data-stu-id="846ad-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="846ad-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="846ad-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





