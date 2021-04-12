---
title: Executiontimelimit (triggerbasetype)-Element
description: Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.
ms.assetid: f78e7c7b-d069-4920-9435-020f6e081eff
keywords:
- Executiontimelimit-Element Taskplaner
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fbe56fb0431ab109b1a19030ae6ba20af55492ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478183"
---
# <a name="executiontimelimit-triggerbasetype-element"></a><span data-ttu-id="278f9-104">Executiontimelimit (triggerbasetype)-Element</span><span class="sxs-lookup"><span data-stu-id="278f9-104">ExecutionTimeLimit (triggerBaseType) Element</span></span>

<span data-ttu-id="278f9-105">Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="278f9-105">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span> <span data-ttu-id="278f9-106">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="278f9-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="278f9-107">Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="278f9-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
 />
```

<span data-ttu-id="278f9-108">Das **executiontimelimit** -Element wird durch den komplexen [**triggerbasetype**](taskschedulerschema-boottriggertype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="278f9-108">The **ExecutionTimeLimit** element is defined by the [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="278f9-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="278f9-109">Parent element</span></span>



| <span data-ttu-id="278f9-110">Element</span><span class="sxs-lookup"><span data-stu-id="278f9-110">Element</span></span>                                                                                     | <span data-ttu-id="278f9-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="278f9-111">Derived from</span></span>                                                                               | <span data-ttu-id="278f9-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="278f9-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="278f9-113">**Boottrigger**</span><span class="sxs-lookup"><span data-stu-id="278f9-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="278f9-114">**boottriggertype**</span><span class="sxs-lookup"><span data-stu-id="278f9-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="278f9-115">Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="278f9-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="278f9-116">**Calendarausgelöst**</span><span class="sxs-lookup"><span data-stu-id="278f9-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="278f9-117">**calendartriggertype**</span><span class="sxs-lookup"><span data-stu-id="278f9-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="278f9-118">Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.</span><span class="sxs-lookup"><span data-stu-id="278f9-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="278f9-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="278f9-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="278f9-120">**eventtriggertype**</span><span class="sxs-lookup"><span data-stu-id="278f9-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="278f9-121">Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="278f9-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="278f9-122">**Idle-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="278f9-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="278f9-123">**idletriggertype**</span><span class="sxs-lookup"><span data-stu-id="278f9-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="278f9-124">Gibt einen-Auslösers an, der einen Task startet, wenn der Computer in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="278f9-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="278f9-125">**Logonauslöst**</span><span class="sxs-lookup"><span data-stu-id="278f9-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="278f9-126">**logontriggertype**</span><span class="sxs-lookup"><span data-stu-id="278f9-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="278f9-127">Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="278f9-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="278f9-128">**Registration-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="278f9-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="278f9-129">**registrationtriggertype**</span><span class="sxs-lookup"><span data-stu-id="278f9-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="278f9-130">Gibt einen-Typ an, der einen Task startet, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="278f9-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="278f9-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="278f9-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="278f9-132">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="278f9-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="278f9-133">Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="278f9-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="278f9-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="278f9-134">Remarks</span></span>

<span data-ttu-id="278f9-135">Bei der Skripterstellung wird das Ausführungszeit Limit mithilfe der [**Trigger.Executiontimelimit**](trigger-executiontimelimit.md) -Eigenschaft angegeben, die von den all-Triggerobjekten geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="278f9-135">For scripting development, the execution time limit is specified using the [**Trigger.ExecutionTimeLimit**](trigger-executiontimelimit.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="278f9-136">Bei der C++-Entwicklung wird das Ausführungszeit Limit mithilfe der [**ITrigger: executiontimelimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) -Eigenschaft angegeben, die von den all-triggerschnittstellen geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="278f9-136">For C++ development, the execution time limit is specified using the [**ITrigger::ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="278f9-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="278f9-137">Requirements</span></span>



| <span data-ttu-id="278f9-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="278f9-138">Requirement</span></span> | <span data-ttu-id="278f9-139">Wert</span><span class="sxs-lookup"><span data-stu-id="278f9-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="278f9-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="278f9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="278f9-141">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="278f9-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="278f9-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="278f9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="278f9-143">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="278f9-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="278f9-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="278f9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="278f9-145">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="278f9-145">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="278f9-146">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="278f9-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





