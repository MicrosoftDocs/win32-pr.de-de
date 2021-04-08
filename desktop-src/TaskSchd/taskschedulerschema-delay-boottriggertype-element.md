---
title: Delay (boottriggertype)-Element
description: Gibt den Zeitraum zwischen dem Start des Systems und dem Start der Aufgabe an.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
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
ms.openlocfilehash: 1ab28da8e9c739d3deff52572fe6a5d37f862119
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957205"
---
# <a name="delay-boottriggertype-element"></a><span data-ttu-id="bce99-104">Delay (boottriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="bce99-104">Delay (bootTriggerType) Element</span></span>

<span data-ttu-id="bce99-105">Gibt den Zeitraum zwischen dem Start des Systems und dem Start der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="bce99-105">Specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="bce99-106">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="bce99-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="bce99-107">Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="bce99-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="bce99-108">Das **Delay** -Element wird durch den komplexen [**boottriggertype**](taskschedulerschema-boottriggertype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="bce99-108">The **Delay** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bce99-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="bce99-109">Parent element</span></span>



| <span data-ttu-id="bce99-110">Element</span><span class="sxs-lookup"><span data-stu-id="bce99-110">Element</span></span>                                                                     | <span data-ttu-id="bce99-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="bce99-111">Derived from</span></span>                                                               | <span data-ttu-id="bce99-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bce99-112">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="bce99-113">**Boottrigger**</span><span class="sxs-lookup"><span data-stu-id="bce99-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md) | [<span data-ttu-id="bce99-114">**boottriggertype**</span><span class="sxs-lookup"><span data-stu-id="bce99-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md) | <span data-ttu-id="bce99-115">Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="bce99-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bce99-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bce99-116">Remarks</span></span>

<span data-ttu-id="bce99-117">Bei der Skript Entwicklung wird die Verzögerung des Ereignis Auslösers durch die [**boottrigger. Delay**](boottrigger-delay.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="bce99-117">For script development, the event trigger delay is specified by the [**BootTrigger.Delay**](boottrigger-delay.md) property.</span></span>

<span data-ttu-id="bce99-118">Bei der C++-Entwicklung wird die Verzögerung des Ereignis Auslösers durch die [**iboottrigger::D Elay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="bce99-118">For C++ development, the event trigger delay is specified by the [**IBootTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="bce99-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bce99-119">Requirements</span></span>



| <span data-ttu-id="bce99-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bce99-120">Requirement</span></span> | <span data-ttu-id="bce99-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bce99-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bce99-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bce99-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bce99-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bce99-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bce99-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bce99-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bce99-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bce99-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bce99-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bce99-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce99-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="bce99-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="bce99-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="bce99-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





