---
title: Duration (repetitiontype)-Element
description: Gibt an, wie lange das Muster wiederholt wird.
ms.assetid: a24f3827-18b2-465e-b132-77dce139e0d4
keywords:
- Duration-Element Taskplaner
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3772abb0224b03db4985de126e1d9cc0058ab5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341327"
---
# <a name="duration-repetitiontype-element"></a><span data-ttu-id="097bd-104">Duration (repetitiontype)-Element</span><span class="sxs-lookup"><span data-stu-id="097bd-104">Duration (repetitionType) Element</span></span>

<span data-ttu-id="097bd-105">Gibt an, wie lange das Muster wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="097bd-105">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="097bd-106">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="097bd-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="097bd-107">Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="097bd-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="097bd-108">Wenn für die Dauer kein Wert angegeben wird, wird das Muster unbegrenzt wiederholt.</span><span class="sxs-lookup"><span data-stu-id="097bd-108">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span> <span data-ttu-id="097bd-109">Der Mindestwert ist eine Minute.</span><span class="sxs-lookup"><span data-stu-id="097bd-109">The minimum value is one minute.</span></span>

``` syntax
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
```

<span data-ttu-id="097bd-110">Das-Element wird durch den komplexen Typ " [**wiederholtiontype**](taskschedulerschema-repetitiontype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="097bd-110">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="097bd-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="097bd-111">Parent element</span></span>



| <span data-ttu-id="097bd-112">Element</span><span class="sxs-lookup"><span data-stu-id="097bd-112">Element</span></span>                                                                      | <span data-ttu-id="097bd-113">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="097bd-113">Derived from</span></span>                                                             | <span data-ttu-id="097bd-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="097bd-114">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="097bd-115">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="097bd-115">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="097bd-116">**Wiederholungstyp**</span><span class="sxs-lookup"><span data-stu-id="097bd-116">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="097bd-117">Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="097bd-117">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="097bd-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="097bd-118">Remarks</span></span>

<span data-ttu-id="097bd-119">Bei Skript Anwendungen wird die Dauer des Musters mithilfe der [**wiederholtionpattern. Duration**](repetitionpattern-duration.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="097bd-119">For scripting applications, the duration of the pattern is specified using the [**RepetitionPattern.Duration**](repetitionpattern-duration.md) property.</span></span>

<span data-ttu-id="097bd-120">Für C++-Anwendungen wird die Dauer des Musters mithilfe der [**irepetitionpattern::D urations**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="097bd-120">For C++ applications, the duration of the pattern is specified using the [**IRepetitionPattern::Duration**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="097bd-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="097bd-121">Examples</span></span>

<span data-ttu-id="097bd-122">Der folgende XML-Code definiert ein Wiederholungsmuster für einen-Auslösers.</span><span class="sxs-lookup"><span data-stu-id="097bd-122">The following XML defines a repetition pattern for a trigger.</span></span>


```XML
<Repetition>
    <Interval></Interval>
    <Duration></Duration>
    <StopAtDurationEnd>true</StopAtDirationEnd>
</Repetition>
```



## <a name="requirements"></a><span data-ttu-id="097bd-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="097bd-123">Requirements</span></span>



| <span data-ttu-id="097bd-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="097bd-124">Requirement</span></span> | <span data-ttu-id="097bd-125">Wert</span><span class="sxs-lookup"><span data-stu-id="097bd-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="097bd-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="097bd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="097bd-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="097bd-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="097bd-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="097bd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="097bd-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="097bd-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="097bd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="097bd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="097bd-131">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="097bd-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="097bd-132">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="097bd-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





