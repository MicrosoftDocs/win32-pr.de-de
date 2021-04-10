---
title: StartBoundary (triggerbasetype)-Element
description: Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- StartBoundary-Element Taskplaner
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d6adf90de2f3b199f98737996fe732f342787b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103182"
---
# <a name="startboundary-triggerbasetype-element"></a><span data-ttu-id="08498-104">StartBoundary (triggerbasetype)-Element</span><span class="sxs-lookup"><span data-stu-id="08498-104">StartBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="08498-105">Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.</span><span class="sxs-lookup"><span data-stu-id="08498-105">Specifies the date and time when the trigger is activated.</span></span>

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="08498-106">Das **StartBoundary** -Element wird durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="08498-106">The **StartBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="08498-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="08498-107">Parent element</span></span>



| <span data-ttu-id="08498-108">Element</span><span class="sxs-lookup"><span data-stu-id="08498-108">Element</span></span>                                                                                     | <span data-ttu-id="08498-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="08498-109">Derived from</span></span>                                                                               | <span data-ttu-id="08498-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08498-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08498-111">**Boottrigger**</span><span class="sxs-lookup"><span data-stu-id="08498-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="08498-112">**boottriggertype**</span><span class="sxs-lookup"><span data-stu-id="08498-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="08498-113">Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="08498-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="08498-114">**Calendarausgelöst**</span><span class="sxs-lookup"><span data-stu-id="08498-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="08498-115">**calendartriggertype**</span><span class="sxs-lookup"><span data-stu-id="08498-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="08498-116">Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.</span><span class="sxs-lookup"><span data-stu-id="08498-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="08498-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="08498-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="08498-118">**eventtriggertype**</span><span class="sxs-lookup"><span data-stu-id="08498-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="08498-119">Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="08498-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="08498-120">**Idle-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="08498-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="08498-121">**idletriggertype**</span><span class="sxs-lookup"><span data-stu-id="08498-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="08498-122">Gibt einen-Auslösers an, der einen Task startet, wenn der Computer in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="08498-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="08498-123">**Logonauslöst**</span><span class="sxs-lookup"><span data-stu-id="08498-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="08498-124">**logontriggertype**</span><span class="sxs-lookup"><span data-stu-id="08498-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="08498-125">Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="08498-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="08498-126">**Registration-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="08498-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="08498-127">**registrationtriggertype**</span><span class="sxs-lookup"><span data-stu-id="08498-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="08498-128">Gibt einen-Typ an, der einen Task startet, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="08498-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="08498-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="08498-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="08498-130">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="08498-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="08498-131">Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="08498-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="08498-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08498-132">Remarks</span></span>

<span data-ttu-id="08498-133">Das **<StartBoundary>** -Element ist ein erforderliches Element für Zeit-und Kalender Trigger ( [**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) und [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md) ).</span><span class="sxs-lookup"><span data-stu-id="08498-133">The **<StartBoundary>** element is a required element for time and calendar triggers ([**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="08498-134">Bei der Entwicklung von Skripts wird die Endgrenze mithilfe [**der Eigenschaft "" des Typs**](trigger-startboundary.md) "" von "alle Auslöse Objekte" geerbt.</span><span class="sxs-lookup"><span data-stu-id="08498-134">For scripting development, the end boundary is specified using the [**Trigger.StartBoundary**](trigger-startboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="08498-135">Bei der C++-Entwicklung wird die Endgrenze mithilfe der [**i-Funktion:: StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) -Eigenschaft angegeben, die von den all-auslöserschnittstellen geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="08498-135">For C++ development, the end boundary is specified using the [**ITrigger::StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="08498-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08498-136">Examples</span></span>

<span data-ttu-id="08498-137">Der folgende XML-Code definiert ein Start-Auslöserelement, das eine Start Grenze von 1. Januar 2005:8:00 Uhr definiert.</span><span class="sxs-lookup"><span data-stu-id="08498-137">The following XML defines a boot trigger element that defines a start boundary of January 1, 2005: 8:00 AM.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="08498-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08498-138">Requirements</span></span>



| <span data-ttu-id="08498-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08498-139">Requirement</span></span> | <span data-ttu-id="08498-140">Wert</span><span class="sxs-lookup"><span data-stu-id="08498-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="08498-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08498-141">Minimum supported client</span></span><br/> | <span data-ttu-id="08498-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08498-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="08498-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08498-143">Minimum supported server</span></span><br/> | <span data-ttu-id="08498-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08498-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08498-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08498-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08498-146">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="08498-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="08498-147">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="08498-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





