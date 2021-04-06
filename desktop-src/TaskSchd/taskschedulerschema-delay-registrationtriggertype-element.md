---
title: Delay (registrationtriggertype)-Element
description: Gibt die Zeitspanne zwischen dem Registrieren der Aufgabe und dem Start der Aufgabe an.
ms.assetid: 8955d86c-8306-45e7-93cf-eacf50e10075
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
ms.openlocfilehash: 4fe1a580a0e69c8e4816022971b2d0bc143544cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743777"
---
# <a name="delay-registrationtriggertype-element"></a><span data-ttu-id="a584d-104">Delay (registrationtriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="a584d-104">Delay (registrationTriggerType) Element</span></span>

<span data-ttu-id="a584d-105">Gibt die Zeitspanne zwischen dem Registrieren der Aufgabe und dem Start der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="a584d-105">Specifies the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="a584d-106">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="a584d-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="a584d-107">Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="a584d-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="a584d-108">Das **Delay** -Element wird durch den komplexen Typ [**registrationtriggertype**](taskschedulerschema-registrationtriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="a584d-108">The **Delay** element is defined by the [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a584d-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="a584d-109">Parent element</span></span>



| <span data-ttu-id="a584d-110">Element</span><span class="sxs-lookup"><span data-stu-id="a584d-110">Element</span></span>                                                                                     | <span data-ttu-id="a584d-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="a584d-111">Derived from</span></span>                                                                               | <span data-ttu-id="a584d-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a584d-112">Description</span></span>                                                                    |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="a584d-113">**Registration-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="a584d-113">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="a584d-114">**registrationtriggertype**</span><span class="sxs-lookup"><span data-stu-id="a584d-114">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="a584d-115">Gibt einen-Typ an, der einen Task startet, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="a584d-115">Specifies a trigger that starts a task when the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a584d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a584d-116">Remarks</span></span>

<span data-ttu-id="a584d-117">Bei der Skripterstellung wird die Verzögerung des Registrierungs Auslösers mithilfe der [**registrationauslöst. Delay**](registrationtrigger-delay.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="a584d-117">For scripting development, the registration trigger delay is specified using the [**RegistrationTrigger.Delay**](registrationtrigger-delay.md) property.</span></span>

<span data-ttu-id="a584d-118">Bei der C++-Entwicklung wird die Verzögerung des Registrierungs Auslösers mithilfe der [**iregistration-:D Elay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="a584d-118">For C++ development, the registration trigger delay is specified using the [**IRegistrationTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) property.</span></span>

## <a name="examples"></a><span data-ttu-id="a584d-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a584d-119">Examples</span></span>

<span data-ttu-id="a584d-120">Der folgende XML-Code definiert eine Registrierungs-Auslöserverzögerung, die eine 5-minütige Verzögerung zwischen dem Zeitpunkt der Registrierung und dem Start der Aufgabe zulässt.</span><span class="sxs-lookup"><span data-stu-id="a584d-120">The following XML defines a registration trigger delay that allows a 5 minute delay between when the task is registered and when the task is started.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay>PT5M<Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="a584d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a584d-121">Requirements</span></span>



| <span data-ttu-id="a584d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a584d-122">Requirement</span></span> | <span data-ttu-id="a584d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a584d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a584d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a584d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a584d-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a584d-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a584d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a584d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a584d-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a584d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a584d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a584d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a584d-129">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="a584d-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a584d-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="a584d-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





