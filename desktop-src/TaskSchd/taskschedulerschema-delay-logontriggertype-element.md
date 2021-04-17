---
title: Delay (logontriggertype)-Element
description: Zeitraum zwischen dem Zeitpunkt, an dem sich der Benutzer anmeldet, und dem Start der Aufgabe.
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
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
ms.openlocfilehash: a820bad3d68cfb0a697f795a9fd7326c9e52abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478903"
---
# <a name="delay-logontriggertype-element"></a><span data-ttu-id="da0eb-104">Delay (logontriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="da0eb-104">Delay (logonTriggerType) Element</span></span>

<span data-ttu-id="da0eb-105">Zeitraum zwischen dem Zeitpunkt, an dem sich der Benutzer anmeldet, und dem Start der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="da0eb-105">Amount of time between when the user logs on and when the task is started.</span></span> <span data-ttu-id="da0eb-106">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="da0eb-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="da0eb-107">Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="da0eb-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="da0eb-108">Das **Delay** -Element wird durch den komplexen [**logontriggertype**](taskschedulerschema-logontriggertype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="da0eb-108">The **Delay** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="da0eb-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="da0eb-109">Parent element</span></span>



| <span data-ttu-id="da0eb-110">Element</span><span class="sxs-lookup"><span data-stu-id="da0eb-110">Element</span></span>                                                                       | <span data-ttu-id="da0eb-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="da0eb-111">Derived from</span></span>                                                                 | <span data-ttu-id="da0eb-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da0eb-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="da0eb-113">**Logonauslöst**</span><span class="sxs-lookup"><span data-stu-id="da0eb-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="da0eb-114">**logontriggertype**</span><span class="sxs-lookup"><span data-stu-id="da0eb-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="da0eb-115">Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="da0eb-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="da0eb-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da0eb-116">Remarks</span></span>

<span data-ttu-id="da0eb-117">Bei der Skripterstellung wird die Verzögerung des LOGON-Auslösers mithilfe der [**LOGON-Eigenschaft. Delay**](logontrigger-delay.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="da0eb-117">For scripting development, the logon trigger delay is specified using the [**LogonTrigger.Delay**](logontrigger-delay.md) property.</span></span>

<span data-ttu-id="da0eb-118">Bei der C++-Entwicklung wird die Benutzer-ID für den Logon-Auslösers mithilfe der [**iLogon-:D Elay**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="da0eb-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="da0eb-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da0eb-119">Requirements</span></span>



| <span data-ttu-id="da0eb-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da0eb-120">Requirement</span></span> | <span data-ttu-id="da0eb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="da0eb-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da0eb-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da0eb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="da0eb-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da0eb-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da0eb-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da0eb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="da0eb-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da0eb-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da0eb-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da0eb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0eb-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="da0eb-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="da0eb-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="da0eb-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





