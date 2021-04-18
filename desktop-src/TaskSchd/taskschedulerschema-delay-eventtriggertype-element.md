---
title: Delay (eventtriggertype)-Element
description: Gibt die Zeitspanne zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe an.
ms.assetid: b38bebc7-9818-41f0-a277-cb0e63c28d86
keywords:
- Verzögertes Element Taskplaner
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de1117ff4f7e0f823b1b213721521e1b526125bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341042"
---
# <a name="delay-eventtriggertype-element"></a><span data-ttu-id="8cc38-104">Delay (eventtriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="8cc38-104">Delay (eventTriggerType) Element</span></span>

<span data-ttu-id="8cc38-105">Gibt die Zeitspanne zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="8cc38-105">Specifies the amount of time between when the event occurs and when the task is started.</span></span> <span data-ttu-id="8cc38-106">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="8cc38-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="8cc38-107">Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="8cc38-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="8cc38-108">Das **Delay** -Element wird durch den komplexen Typ [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="8cc38-108">The **Delay** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8cc38-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="8cc38-109">Parent element</span></span>



| <span data-ttu-id="8cc38-110">Element</span><span class="sxs-lookup"><span data-stu-id="8cc38-110">Element</span></span>                                                                       | <span data-ttu-id="8cc38-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="8cc38-111">Derived from</span></span>                                                                 | <span data-ttu-id="8cc38-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cc38-112">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="8cc38-113">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="8cc38-113">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="8cc38-114">**eventtriggertype**</span><span class="sxs-lookup"><span data-stu-id="8cc38-114">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="8cc38-115">Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="8cc38-115">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8cc38-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cc38-116">Remarks</span></span>

<span data-ttu-id="8cc38-117">Bei der Skript Entwicklung wird die Ereignis Trigger-Verzögerung von der [**EventTrigger. Delay**](eventtrigger-delay.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="8cc38-117">For script development, the event trigger delay is specified by the [**EventTrigger.Delay**](eventtrigger-delay.md) property.</span></span>

<span data-ttu-id="8cc38-118">Bei der C++-Entwicklung wird die Verzögerung des Ereignis Auslösers durch die [**ieventvent::D Elay**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="8cc38-118">For C++ development, the event trigger delay is specified by the [**IEventTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc38-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cc38-119">Requirements</span></span>



| <span data-ttu-id="8cc38-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cc38-120">Requirement</span></span> | <span data-ttu-id="8cc38-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8cc38-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8cc38-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8cc38-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8cc38-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cc38-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8cc38-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8cc38-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8cc38-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cc38-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8cc38-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cc38-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc38-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="8cc38-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="8cc38-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="8cc38-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





