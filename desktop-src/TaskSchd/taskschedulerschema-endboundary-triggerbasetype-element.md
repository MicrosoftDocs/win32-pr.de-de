---
title: Endboundary (triggerbasetype)-Element
description: Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.
ms.assetid: 84731c0b-3fb8-44dd-be1a-67547add1f9e
keywords:
- Endboundary-Element Taskplaner
topic_type:
- apiref
api_name:
- EndBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d687655498301595c1ab888fcc179ec0694f0aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341589"
---
# <a name="endboundary-triggerbasetype-element"></a><span data-ttu-id="46622-105">Endboundary (triggerbasetype)-Element</span><span class="sxs-lookup"><span data-stu-id="46622-105">EndBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="46622-106">Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="46622-106">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="46622-107">Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="46622-107">The trigger cannot start the task after it is deactivated.</span></span>

``` syntax
<xs:element name="EndBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="46622-108">Das **endboundary** -Element wird durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="46622-108">The **EndBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="46622-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="46622-109">Parent element</span></span>



| <span data-ttu-id="46622-110">Element</span><span class="sxs-lookup"><span data-stu-id="46622-110">Element</span></span>                                                                                     | <span data-ttu-id="46622-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="46622-111">Derived from</span></span>                                                                               | <span data-ttu-id="46622-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46622-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46622-113">**Boottrigger**</span><span class="sxs-lookup"><span data-stu-id="46622-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="46622-114">**boottriggertype**</span><span class="sxs-lookup"><span data-stu-id="46622-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="46622-115">Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="46622-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="46622-116">**Calendarausgelöst**</span><span class="sxs-lookup"><span data-stu-id="46622-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="46622-117">**calendartriggertype**</span><span class="sxs-lookup"><span data-stu-id="46622-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="46622-118">Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.</span><span class="sxs-lookup"><span data-stu-id="46622-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="46622-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="46622-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="46622-120">**eventtriggertype**</span><span class="sxs-lookup"><span data-stu-id="46622-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="46622-121">Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="46622-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="46622-122">**Idle-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="46622-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="46622-123">**idletriggertype**</span><span class="sxs-lookup"><span data-stu-id="46622-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="46622-124">Gibt einen-Auslösers an, der einen Task startet, wenn der Computer in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="46622-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="46622-125">**Logonauslöst**</span><span class="sxs-lookup"><span data-stu-id="46622-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="46622-126">**logontriggertype**</span><span class="sxs-lookup"><span data-stu-id="46622-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="46622-127">Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="46622-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="46622-128">**Registration-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="46622-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="46622-129">**registrationtriggertype**</span><span class="sxs-lookup"><span data-stu-id="46622-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="46622-130">Gibt einen-Typ an, der einen Task startet, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="46622-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="46622-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="46622-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="46622-132">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="46622-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="46622-133">Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="46622-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="46622-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46622-134">Remarks</span></span>

<span data-ttu-id="46622-135">Bei der Entwicklung von Skripts wird die Endgrenze mithilfe der "" [**-Eigenschaft von**](trigger-endboundary.md) "" für alle Auslöse Objekte geerbt.</span><span class="sxs-lookup"><span data-stu-id="46622-135">For scripting development, the end boundary is specified using the [**Trigger.EndBoundary**](trigger-endboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="46622-136">Bei der C++-Entwicklung wird die Endgrenze mithilfe der [**i-Funktion:: endboundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) -Eigenschaft angegeben, die von den all-auslöserschnittstellen geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="46622-136">For C++ development, the end boundary is specified using the [**ITrigger::EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="46622-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46622-137">Examples</span></span>

<span data-ttu-id="46622-138">Der folgende XML-Code definiert ein Start-Auslöserelement, das eine Endgrenze von 1. Januar 2007:8:00 Uhr definiert.</span><span class="sxs-lookup"><span data-stu-id="46622-138">The following XML defines a boot trigger element that defines an end boundary of January 1, 2007: 8:00 AM.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="46622-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46622-139">Requirements</span></span>



| <span data-ttu-id="46622-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46622-140">Requirement</span></span> | <span data-ttu-id="46622-141">Wert</span><span class="sxs-lookup"><span data-stu-id="46622-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46622-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46622-142">Minimum supported client</span></span><br/> | <span data-ttu-id="46622-143">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46622-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46622-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46622-144">Minimum supported server</span></span><br/> | <span data-ttu-id="46622-145">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46622-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46622-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46622-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46622-147">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="46622-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="46622-148">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="46622-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





