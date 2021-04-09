---
title: Aktiviertes (triggerbasetype)-Element
description: Gibt an, dass der-Wert aktiviert ist.
ms.assetid: 14c98f40-0ec5-4dc1-978e-b02c08ee2384
keywords:
- Aktiviertes Element Taskplaner
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42b495ba1af5f3b9b99034b0d6ca9d02040460c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041001"
---
# <a name="enabled-triggerbasetype-element"></a><span data-ttu-id="b02a0-104">Aktiviertes (triggerbasetype)-Element</span><span class="sxs-lookup"><span data-stu-id="b02a0-104">Enabled (triggerBaseType) Element</span></span>

<span data-ttu-id="b02a0-105">Gibt an, dass der-Wert aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b02a0-105">Specifies that the trigger is enabled.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
 />
```

<span data-ttu-id="b02a0-106">Das **aktivierte** Element wird durch den komplexen Typ [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="b02a0-106">The **Enabled** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b02a0-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="b02a0-107">Parent element</span></span>



| <span data-ttu-id="b02a0-108">Element</span><span class="sxs-lookup"><span data-stu-id="b02a0-108">Element</span></span>                                                                                     | <span data-ttu-id="b02a0-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="b02a0-109">Derived from</span></span>                                                                               | <span data-ttu-id="b02a0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b02a0-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b02a0-111">**Boottrigger**</span><span class="sxs-lookup"><span data-stu-id="b02a0-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="b02a0-112">**boottriggertype**</span><span class="sxs-lookup"><span data-stu-id="b02a0-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="b02a0-113">Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b02a0-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="b02a0-114">**Calendarausgelöst**</span><span class="sxs-lookup"><span data-stu-id="b02a0-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="b02a0-115">**calendartriggertype**</span><span class="sxs-lookup"><span data-stu-id="b02a0-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="b02a0-116">Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.</span><span class="sxs-lookup"><span data-stu-id="b02a0-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="b02a0-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="b02a0-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="b02a0-118">**eventtriggertype**</span><span class="sxs-lookup"><span data-stu-id="b02a0-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="b02a0-119">Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="b02a0-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="b02a0-120">**Idle-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="b02a0-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="b02a0-121">**idletriggertype**</span><span class="sxs-lookup"><span data-stu-id="b02a0-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="b02a0-122">Gibt einen-Auslösers an, der einen Task startet, wenn der Computer in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="b02a0-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="b02a0-123">**Logonauslöst**</span><span class="sxs-lookup"><span data-stu-id="b02a0-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="b02a0-124">**logontriggertype**</span><span class="sxs-lookup"><span data-stu-id="b02a0-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="b02a0-125">Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="b02a0-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="b02a0-126">**Registration-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="b02a0-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="b02a0-127">**registrationtriggertype**</span><span class="sxs-lookup"><span data-stu-id="b02a0-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="b02a0-128">Gibt einen-Typ an, der einen Task startet, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="b02a0-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="b02a0-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="b02a0-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="b02a0-130">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="b02a0-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="b02a0-131">Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="b02a0-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="b02a0-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b02a0-132">Remarks</span></span>

<span data-ttu-id="b02a0-133">Bei der Skripterstellung erfolgt der Zugriff auf diese Informationen über die Eigenschaft "" des ""- [**Auslösers.**](trigger-enabled.md)</span><span class="sxs-lookup"><span data-stu-id="b02a0-133">For scripting development, this information is accessed through the [**Trigger.Enabled**](trigger-enabled.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="b02a0-134">Bei der C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die [**i-Funktion:: aktivierte**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) Eigenschaft, die von den all-auslöserschnittstellen geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="b02a0-134">For C++ development, this information is accessed through the [**ITrigger::Enabled**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="b02a0-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b02a0-135">Requirements</span></span>



| <span data-ttu-id="b02a0-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b02a0-136">Requirement</span></span> | <span data-ttu-id="b02a0-137">Wert</span><span class="sxs-lookup"><span data-stu-id="b02a0-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b02a0-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b02a0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b02a0-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b02a0-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b02a0-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b02a0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b02a0-141">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b02a0-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b02a0-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b02a0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b02a0-143">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="b02a0-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b02a0-144">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="b02a0-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





